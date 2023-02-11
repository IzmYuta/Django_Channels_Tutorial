# Django_Channels_Tutorial
## 環境構築(Win版)
＊Macは1,2が若干異なる可能性あり
### 1. 仮想マシンの構築

```powershell
python -m venv venv
```

### 2. 仮想マシンの起動

```powershell
venv\Scripts\activate
```


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
 
