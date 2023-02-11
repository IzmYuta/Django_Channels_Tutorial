# Django_Channels_Tutorial
## 環境構築

### 1. 仮想マシンの構築

```powershell
python -m venv venv
```

### 2. 仮想マシンの起動

```powershell
venv\Scripts\activate
```

**補足：**
Windows 10では、`execution of scripts is disabled on this system`というエラーがWindows PowerShellに出ることがあります。 その場合は、Windows PowerShellを「管理者として開く」で、管理者権限で新しくウィンドウを開いてください。 そして、仮想環境を起動する前に、以下のコマンドを入力してください。

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
```

次の表示が出るので`A`を入力する。

```powershell
Execution Policy Change
    The execution policy helps protect you from scripts that you do not trust. Changing the execution policy might expose you to the security risks described in the about_Execution_Policies help topic at http://go.microsoft.com/fwlink/?LinkID=135170. Do you want to change the execution policy? [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N")
```

**~~補足：** 人気のあるエディタであるVS Codeを使っている方は、VS CodeはWindows Powershellベースの統合ターミナルが一緒になっているので、統合ターミナルを使う場合、仮想環境を有効にするために下記のコマンドを実行してください：~~

```
$ . myvenv\Scripts\activate.ps1

```

~~エディタのウィンドウとコマンドラインのウィンドウを行き来する必要がなくなるのが利点です。~~

### 3. Djangoのインストール

**3.1 pipのインストール**

最新バージョンの `pip` がインストールされていることを確認すべきです。pipはDjangoのインストールに使うソフトウェアです。

```
python -m pip install --upgrade pip
```

****3.2 requirementsファイルによってパッケージをインストールする****

```
pip install -r requirements.txt
```
### 4. Redisの起動
```
docker run -p 6379:6379 -d redis:5
```


### 5. データベースの立ち上げ

```powershell
python manage.py migrate
```


### 6. ローカルサーバの起動

```powershell
python manage.py runserver
```
 http://127.0.0.1:8000/chat/ でルーム名を入力して、チャットルームの作成ができる。遷移先は http://127.0.0.1:8000/chat/ルーム名/ 。
 
