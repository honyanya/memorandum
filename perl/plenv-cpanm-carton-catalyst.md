## plenv-cpanm-carton-catalyst

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

* anyenv を用いて plenv をインストール
```bash
$ anyenv install plenv
$ exec $SHELL -l
$ anyenv versions
$ which plenv
```

* plenv を用いて perl をインストール 
```bash
### perl-build があるか確認
$ ls ~/.anyenv/envs/plenv/plugins/ | grep perl-build

$ plenv install 5.20.3
$ plenv versions
$ plenv global 5.20.3
$ plenv rehash
$ perl --version
```

* plenv を用いて cpanminus(cpanm) をインストール
```bash
$ plenv install-cpanm
$ plenv exec cpanm -v

### モジュール確認
$ plenv list-modules
```

* cpanmを用いて carton をインストール
```bash
$ plenv exec cpanm Module::Install
$ plenv exec cpanm Carton
$ plenv rehash
```

* carton を用いて catalyst のインストール
```bash
### 動作確認用のディレクトリ
$ mkdir ~/Documents/dev/perl-cpanm-carton-catalyst-test/ && cd ~/Documents/dev/perl-cpanm-carton-catalyst-test/

$ touch cpanfile
$ echo "requires 'Catalyst::Runtime';" >> cpanfile
$ echo "requires 'Catalyst::Devel';" >> cpanfile

$ plenv exec carton install
$ carton exec catalyst.pl
```


* carton を用いて catalyst アプリ作成 & 実行
```bash
$ carton exec catalyst.pl Test::App
$ carton exec ./Test-App/script/test_app_server.pl -r
```

---

* 参考
  * [plenv + cpanm + carton でPerlの開発環境を構築する | Act as Professional](https://hiroki.jp/2013/02/18/6684/)
  * [plenvの基本メモ書き - Qiita](http://qiita.com/laikuaut/items/82c9b402920e30c2c4eb)
  * [【perl】Perl module 依存マネージャーcartonをmac × plenv × cpanm環境で使うメモ - tweeeetyのぶろぐ的めも](http://tweeeety.hateblo.jp/entry/2015/06/21/203144)
  * [【perl】plenvでperl x cpanm x carton環境を作る - mac編 - tweeeetyのぶろぐ的めも](http://tweeeety.hateblo.jp/entry/2015/05/06/022937)

---


