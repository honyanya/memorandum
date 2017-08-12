## activator

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

* install
  * [Lightbend Activator and sbt get you started with the Lightbend Reactive Platform | @lightbend](https://www.lightbend.com/community/core-tools/activator-and-sbt) 
  * https://downloads.typesafe.com/typesafe-activator/1.3.12/typesafe-activator-1.3.12.zip
  * ypesafe-activator-1.3.12.zip
  * https://downloads.typesafe.com/typesafe-activator/1.3.12/typesafe-activator-1.3.12-minimal.zip
  * typesafe-activator-1.3.12-minimal.zip
  * [typesafe activatorを使わずにPlay Frameworkを使う方法 - Qiita](http://qiita.com/twdxm/items/ba7e09af8cf8fbc17d94#comment-6b6d50c4fd9530f0f8b9)
    * Typesafe Activatorは2017年5月24日でサポートが終了
    * sbt-0.13.13以上 `$ sbt new playframework/play-scala-seed.g8` で作成
  * [ScalaとActivatorを入れてはじめてみた - Qiita](http://qiita.com/jumjamjohn/items/2e3820fbc54820b34ee2)
  * [【PlayFramework】Cloud9(ubuntu14.04)にPlayFramework2.5（typesafe activator）を導入する方法](https://www.deep-rain.com/programming/play-framework/294)
```bash
$ cd ~/Documents/tmp/
$ wget https://downloads.typesafe.com/typesafe-activator/1.3.12/typesafe-activator-1.3.12.zip
$ unzip typesafe-activator-1.3.12.zip -d ~/Documents/bin/

$ echo 'export PATH="$HOME/Documents/bin/activator-dist-1.3.12/bin/:$PATH"' >> ~/.bashrc
$ source ~/.bashrc
$ activator -help
```

---


