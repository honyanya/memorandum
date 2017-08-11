## ndenv

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

* install
```bash
$ anyenv install ndenv
$ anyenv versions
$ exec $SHELL -l
$ which anyenv
```

```bash
$ mkdir -p $(anyenv root)/plugins
$ git clone https://github.com/znz/anyenv-update.git $(anyenv root)/plugins/anyenv-update
$ anyenv update
```

* [ndenv で Node.js をインストールする際、同時に Yarn もインストールする方法 - Qiita](http://qiita.com/pine613/items/d758aede73e388c7b57a)
```bash
$ echo $(ndenv root)
$ git clone https://github.com/pine/ndenv-yarn-install.git "$(ndenv root)/plugins/ndenv-yarn-install"
$ exec $SHELL -l
$ ndenv hooks install
```

* [anyenvのndenvを使ってnode.jsのバージョンを管理する - Qiita](http://qiita.com/0084ken/items/22ca33032773c6d2f9f4)
* [Node.jsのバージョンを自動で切り替えられるndenvが超便利 - Qiita](http://qiita.com/tonkotsuboy_com/items/5322d226b6783d25b5df)
```bash
$ ndenv install -l
$ ndenv install v7.10.1
$ ndenv versions
$ ndenv global v7.10.1
$ node -v
$ npm -v
```

---

