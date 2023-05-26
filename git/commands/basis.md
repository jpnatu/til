# Gitの基本的なコマンド

## 初期設定を行う
```
$ git config --global user.name "jpnatu"

$ git config --global user.email "jpnatu@hoge.com"
```

### 設定の確認
```
$ git config --list
```

## リポジトリの作成
```
$ git init
```
リポジトリの初期化。

## ファイルをステージングする
```
$git add <filename>
$git add .
```
`<filename>`を指定することで指定したファイルを上げることができるが、`git add .` でディレクトリ下のファイルすべてをステージングできる。

## ファイルのコミット
```
$ git commit
```
ステージングエリアからローカルリポジトリへ上げる。
```
$ git commit -m "first commit"
```
`git commit` の後に `-m "message"` でメッセージを残すことができる。

## リモートにプッシュする
```
$ git remote add origin https://github.com/jpnatu/XXXXX.git
$ git push -u origin main
```
`-u`を指定することで、ブランチの関連づけがされる。次回以降のプッシュ時に単に`git push`コマンドを実行するだけで済む。

### ローカルにリポジトリを作成してリモートにプッシュする流れ
```
$ git init
$ git add .
$ git commit -m "Initial commit"
$ git remote add origin https://github.com/XXXX/XXXXXX.git
$ git push -u origin main
```
