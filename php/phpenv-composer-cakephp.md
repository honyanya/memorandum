## phpenv-composer-cakephp

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

* anyenv を用いて phpenv をインストール
```bash
$ anyenv install phpenv
$ exec $SHELL -l
$ anyenv versions
$ which phpenv
```

* phpenv を用いて php をインストール 
```bash
### php-build があるか確認
$ ls ~/.anyenv/envs/phpenv/plugins/ | grep php-build
### phpenv-composer があるか確認
$ ls ~/.anyenv/envs/phpenv/plugins/ | grep phpenv-composer

$ phpenv install 5.6.31

### UBILD ERROR が出力されるので、足りないのものを apt-get でインストール
$ sudo apt-get install -y \
    libxml2-dev \
    libbz2-dev \
    libcurl4-openssl-dev \
    libjpeg-dev \
    libpng12-dev \
    libmcrypt-dev 
    libtidy-dev \
    libxslt1-dev \
    autoconf \
    automake

$ phpenv install 5.6.31
$ phpenv versions
$ phpenv global 5.6.31
$ phpenv rehash
$ php --version
$ composer --version
```


* composer を用いて cakephp アプリ作成 & 実行
```bash
### 動作確認用のディレクトリ
$ mkdir ~/Documents/dev/php-composer-cakephp-test/ && cd ~/Documents/dev/php-composer-cakephp-test/

### composer を用いて cakephp のインストール
$ composer self-update && composer create-project --prefer-dist cakephp/app .
### cake コマンド確認
$ ./bin/cake
### ホストとポートを指定して、開発用サーバーの起動
$ ./bin/cake server -H 0.0.0.0 -p 3000
```

---

* 参考
  * [PHP開発でComposerを使わないなんてありえない！基礎編 - Qiita](http://qiita.com/niisan-tokyo/items/8cccec88d45f38171c94)
  * [phpbrew installでビルド関係のエラーが出るとき - Qiita](http://qiita.com/daikiojm/items/0c89656eb934ae279bf0)
  * [anyenvでphpenvをインストールしてphp5.6系をインストールするまで - Qiita](http://qiita.com/kikunantoka/items/3a8de0ca9dd6edda0942)
  * [anyenvで入れたphpenvに対して、composerを使う - Screaming Loud](http://yuutookun.hatenablog.com/entry/2015/09/29/114039)
  * [https://mistymagich.wordpress.com/2015/06/05/ubuntuにphpenvからphpをインストールした時のエラー/](https://mistymagich.wordpress.com/2015/06/05/ubuntu%E3%81%ABphpenv%E3%81%8B%E3%82%89php%E3%82%92%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%81%97%E3%81%9F%E6%99%82%E3%81%AE%E3%82%A8%E3%83%A9%E3%83%BC/)
  * [Ubuntu に phpenv を入れて複数バージョンのPHP管理しようとした - Qiita](http://qiita.com/qurage/items/70f3341a18a5172288f7#2-%E4%BE%9D%E5%AD%98%E3%83%91%E3%83%83%E3%82%B1%E3%83%BC%E3%82%B8%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)
  * [phpenv + php-build + composer で開発環境作ってみた | 69log](https://blog.kazu69.net/2013/02/06/phpenv-php-build-composer/)

---



