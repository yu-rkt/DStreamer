# DStreamer

# README

## 前提条件
- pyenvがインストールされている
- ↑のpathがbashprofileに通っている
- pipがインストールされている

以下の記事の前半に諸々が書いてあるので、必要なら参照。
https://qiita.com/SE_AmericanFootball/items/8e2af2da9cabddb87bb3

# 仮想環境の構築

1. 仮想環境を作る
`python -m venv [仮想環境名]`

2. アクティブにする
`source [仮想環境名]/bin/activate `

3. 仮想環境内で、djangoをインストールする
`pip install Django==2.2.6`

4. 確認する。
`python -m django --version`


# DB接続
以下記事参考。
https://qiita.com/salvage0707/items/2713d062971d528ab211

以下、仮想環境内で行う。

1. mysqlをインストール
`brew install mysql`

2. mysqlサーバーの起動
` mysql.server start`

3. mysql接続
`mysql -u root`

4. databaseの確認
`show databases`

5. 試しにdb作る。（やらなくても良い）
`create database sample`で作る。（作成時のみ）

6. mysqlclientのインストール
`pip install mysqlclient`

7. 確認
`pip freeze -l`

8. マイグレート
`python manage.py migrate`

9. 確認
` mysql -u root`
`use ~~`
`show tables`
