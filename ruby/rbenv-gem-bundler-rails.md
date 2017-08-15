## rbenv-gem-bundler-rails

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

* anyenv を用いて rbenv をインストール
```bash
$ anyenv install rbenv
$ exec $SHELL -l
$ anyenv versions
$ which rbenv
```

* rbenv を用いて ruby をインストール 
```bash
### ruby-build があるか確認
$ ls ~/.anyenv/envs/rbenv/plugins/ | grep ruby-build

$ rbenv install 2.4.1
$ rbenv versions
$ rbenv global 2.4.1
$ rbenv rehash
$ ruby --version
```

* gem 確認
```bash
$ rbenv exec gem environment
$ rbenv exec gem list
```

* bundler のインストール
```bash
$ rbenv exec gem install bundler
$ rbenv rehash
$ rbenv exec gem list | grep bundler
$ rbenv exec bundler -v
```

* bundler を用いて rails のインストール
```bash
### 動作確認用のディレクトリ
$ mkdir ~/Documents/dev/ruby-gem-bundler-rails-test/ && cd ~/Documents/dev/ruby-gem-bundler-rails-test/

$ rbenv exec bundle init
$ bundler init
$ vim Gemfile
$ bundler install --path vendor/bundle
$ bundler exec rails -v
$ bundler exec rails new .

Gem::Ext::BuildError: ERROR: Failed to build gem native extension.

    current directory: /home/vagrant/Documents/dev/test/ruby-gem-bundler-rails-test/vendor/bundle/ruby/2.4.0/gems/sqlite3-1.3.13/ext/sqlite3
/home/vagrant/.anyenv/envs/rbenv/versions/2.4.1/bin/ruby -r ./siteconf20170814-9098-glz3mp.rb extconf.rb
checking for sqlite3.h... no
sqlite3.h is missing. Try 'brew install sqlite3',
'yum install sqlite-devel' or 'apt-get install libsqlite3-dev'
and check your shared library search path (the
location where your sqlite3 shared library is located).
*** extconf.rb failed ***



### 上記のようなメッセージが出力され、エラーとなるため、sqlite3関連をインストール
$ sudo apt-get install libsqlite3-dev
### 再度 bundler install を実行
$ bundler install --path vendor/bundle
### rails 起動
$ bundler exec rails s
```


---

* 参考
  * [rubyを超高速でインストールする方法 - Qiita](http://qiita.com/yn-misaki/items/23ff4e0f1268511aed41)
  * [【Rails】ruby、gem、rbenv、rails、bundler関係等適当まとめ。特にbundler - Qiita](http://qiita.com/Azunyan1111/items/e22f1e9f2ba238bc72d0)
  * [rbenv や Bundler を用いた Ruby環境構築 - Qiita](http://qiita.com/HayneRyo/items/d493a2b3cec2322f167c)
  * [Bundlerの使い方 - Qiita](http://qiita.com/oshou/items/6283c2315dc7dd244aef)
  * [【CentOS7(+Ubuntu16)】Ruby / Rails のインストールから Rails サーバの起動までの(ほぼ)完全ガイド - Qiita](http://qiita.com/noraworld/items/d92cca9bb449b48a97aa#rails%E3%82%B5%E3%83%BC%E3%83%90%E3%82%92%E7%AB%8B%E3%81%A1%E4%B8%8A%E3%81%92%E3%82%8B)

---


