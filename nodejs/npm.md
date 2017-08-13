## npm

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

* npm
  * [僕がnpm installに-gをつけないわけ - Qiita](http://qiita.com/Mic-U/items/cd456d6bea72937464f8)
  * [コマンドパスを自動で通し npm install -g しない - Qiita](http://qiita.com/Jxck_/items/8f5d1b70b7b5aa6053ee)
```bash
### npm でローカルインストールしたコマンドを使えるようにするためのパス設定
$ echo 'export PATH=./node_modules/.bin:$PATH' >> ~/.bashrc

### 動作確認用のディレクトリ
$ mkdir ~/Documents/dev/react-test/ && cd ~/Documents/dev/react-test/

### package.json 生成
$ npm init

### グローバルインストールされたものの一覧
$ npm list -g
### ローカルインストールされてものの一覧
$ npm list

### npm で必要なものをインストール
$ npm install --save react react-dom
$ npm install --save-dev webpack babel-cli babel-core babel-loader babel-preset-es2015 babel-preset-react
### 内容が反映されているか
$ cat package.json

### npm install したものを削除する場合
$ npm uninstall --save xxx
$ npm uninstall --save-dev xxx

```

---

