## anyenv

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

* install
  * [anyenvでモダンな開発環境構築。PHP,NodeJS,Ruby,Perl,Python - Qiita](http://qiita.com/pfavill/items/f500e46444c86a6f8e6a#anyenv%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)
  * [anyenvで開発環境を整える - Qiita](http://qiita.com/luckypool/items/f1e756e9d3e9786ad9ea)
  * ([anyenvをHomebrewでインストールできるようにしてみた - Qiita](http://qiita.com/mumoshu/items/7cdc57de120d75d18b30))

```bash
$ git clone https://github.com/riywo/anyenv ~/.anyenv
$ echo 'export PATH="$HOME/.anyenv/bin:$PATH"' >> ~/.your_profile
$ echo 'eval "$(anyenv init -)"' >> ~/.your_profile
$ exec $SHELL -l
$ anyenv versions
```

---

