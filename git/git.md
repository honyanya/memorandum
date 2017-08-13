## git

* 環境
  * Mac OS X El Capitan

---

* git
  * [Gitのコミットメッセージの書き方 - Qiita](http://qiita.com/itosho/items/9565c6ad2ffc24c09364)
```bash
### git の設定
$ git config --list
$ git config --global user.name "sample"
$ git config --global user.email "sample@example.com"
$ git config --list

$ cd ~/Documents/dev/project-name/

### git 管理下にする
$ git init
### 空コミット
$ git commit --allow-empty -m "create repository"
### リモートリポジトリとの紐付け
$ git remote add origin https://xxx/yyy/zzz.git
### リモートリポジトリの master ブランチへ push
$ git push -u origin master

### feature ブランチへ切り替え
$ git checkout -b feature/xxx
### 空コミット
$ git commit --allow-empty -m "create branch"
### リモートリポジトリの feature ブランチへ push
$ git push origin feature/xxx

### .gitignore 作成
$ vim .gitignore
$ git add .
$ git commit -m "[xxx] xxx (#1)" # メッセージは "[コミット種別] 要約 (#issue番号)"
$ git push origin feature/xxx

```

---

