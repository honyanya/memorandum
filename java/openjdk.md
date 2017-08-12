## openjdk

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

* anyenv jenv install
```bash
$ anyenv install jenv
$ exec $SHELL -l
$ anyenv versions
$ which jenv
```

* OpenJDK
  * [java - How do I install openjdk 7 on Ubuntu 16.04 or higher? - Ask Ubuntu](https://askubuntu.com/questions/761127/how-do-i-install-openjdk-7-on-ubuntu-16-04-or-higher)
  * [Ubuntu 14.xにOpenJDK 8環境を構築 - Qiita](http://qiita.com/ytkumasan/items/0a6b9e512e3dd5c08a31)
```bash
$ sudo add-apt-repository ppa:openjdk-r/ppa
$ sudo apt-get update
$ sudo apt-cache search openjdk
$ sudo apt-get -y install \
    openjdk-7-jdk \
    openjdk-8-jdk
```


* jenv
  * [brew で Java をインストールして、jenv で管理する - Qiita](http://qiita.com/take-ookubo/items/031688a521fccce93f9e)
  * [Amazon Linux に jenv を入れる - Qiita](http://qiita.com/rysk92/items/7cf4018adde3b8c4f5b8)
  * [複数バージョンのJavaを切り替えて使用できるようにする。 - Qiita](http://qiita.com/takuya71/items/8d670d8f216af87cfe01)
  * [jenv のインストール - 雨駆動開発](http://rainydaidoh.hatenablog.com/entry/2014/10/05/121630)
  * [MacでJavaをインストール | IT屋さんの備忘録](http://geisterhacker.com/index.php/2017/05/09/mac-java-install/)
```bash
$ jenv add /usr/lib/jvm/java-7-openjdk-amd64/
$ jenv add /usr/lib/jvm/java-8-openjdk-amd64/
$ jenv versions
$ jenv global openjdk64-1.8.0.131
$ jenv versions
$ jenv rehash

$ java -version
$ javac -version

$ readlink -f /usr/bin/javac | sed "s:/bin/javac::"
$ which java

$ jenv enable-plugin export
$ source ~/.bashrc
$ echo $JAVA_HOME
```

---


