# jekyllを使用してHPを作成しました．

- `about.md` : このHPの概要
- `_posts/` : ゼミや勉強会を1単位としたページ


# usage

### このリポジトリに対してwrite権限を持っている方 (原則として手塚研と若林研)

##### まずcloneします

```
$ git clone git@github.com:slis-ml/slis-ml.github.io.git
$ cd git@github.com:slis-ml/slis-ml.github.io.git
```

##### 必要なgemをインストールします

```
$ bundle install --path vendor/bundle # jekyllに必要なgemをbundleを使ってインストール
$ bundle exec jekyll server # localhostを立ち上げて確認
```

立ち上げると [http://localhost:4000/](http://localhost:4000/) からアクセスができます．


##### 編集してから反映させます

```
$ git add .
$ git commit -m "編集内容をここに書く"
$ git push
```

### write権限がない，いきなりpushしたくない方

やり方はいくつかありますがここでは1例を紹介します．

##### まずforkします

[github](https://github.com/slis-ml/slis-ml.github.io)のforkというボタンをクリックして，自分のアイコンを選んでください．

##### cloneします

```
$ git clone git@github.com:slis-ml/slis-ml.github.io.git
$ cd slis-ml.github.io
```

##### remoteとしてforkした方を追加します

```
git remote add local git@github.com:YOUR-github-account-id/slis-ml.github.io.git
```

- `local` の部分は何でもよいです．
- `YOUR-github-account-id`は自分のアカウント名 (あるいは `git@~~~.git` はforkしたリポジトリのcloneボタンででてくるリンクを貼り付けるだけでよいです)

##### 編集してから反映させます

```
$ git add .
$ git commit -m "編集内容をここに書く"
$ git push local master # 2回目以降はgit push -f local master
```

##### PRを送る

forkした方のリポジトリから `[New pull request]` を出します．

##### 2回目以降

最新版のslis-ml.github.ioのページをもってくる

```
$ git fetch origin master
$ git reset --hard origin/master
```

[編集してから反映させます]&[PRを送る]と同じです．


# その他

管理者は若林研の野沢ですのでご不明な点は野沢さんまで
