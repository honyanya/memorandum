## Vagrant で Ubuntu1604 を使う

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3

---

### Vagrant で Ubuntu1604 を用意

* 参考
  * [Ubuntu16.04のVagrant Boxを取得する - Qiita](http://qiita.com/shirakiya/items/517d10a227a9326568ad)


```bash
$ cd ~/Documents/dev/vagrant/bento/ubuntu-16.04
$ vagrant box add ubuntu-16.04 https://atlas.hashicorp.com/bento/boxes/ubuntu-16.04/versions/2.3.0/providers/virtualbox
$ vagrant box list
$ vagrant init ubuntu-16.04
```

```bash
$ vim Vagrantfile
```

```Vagrantfile
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-16.04"

  # ローカルへのポート3000アクセスをvmのポート3000に転送（Web開発で必要な場合）
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 9000, host: 9000

  # Windowsローカル環境から、192.168.33.10で接続
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    # vb.memory = "2048" # メモリは2GB
    vb.memory = "4096" # メモリは4GB

    vb.customize [
      "modifyvm", :id,
      "--vram", "256", # ビデオメモリ確保（フルスクリーンモードにするため）
      "--clipboard", "bidirectional", # クリップボードの共有
      "--draganddrop", "bidirectional", # ドラッグアンドドロップ可能に
    ]
  end
end
```

```bash
$ vagrant up
```

---

### GUI 環境

* 参考
  * [Windows環境にVagrant+Ubuntuデスクトップ環境をインストール - Qiita](http://qiita.com/mhagita/items/8f339106c3b48eb098ca)

```bash
$ sudo apt-get update
$ sudo apt-get upgrade

$ sudo apt-get -y install ubuntu-desktop
$ sudo reboot
```

---

### もろもろ設定

* 日本語化
  * [Ubuntuの言語設定を日本語に変更する。 - Qiita](http://qiita.com/KAZUKI1994/items/68e90244c2aa901e34ff)
```bash
$ sudo apt-get -y install \
    language-pack-ja-base \
    language-pack-ja \
    ibus-mozc
$ sudo update-locale LANG=ja_JP.UTF-8 LANGUAGE=”ja_JP:ja”
$ source /etc/default/locale
$ sudo reboot
```

* 日本語入力 ↑の日本語化を行えばいらないかも
  * [ubuntuで日本語入力を行う - Qiita](http://qiita.com/shishamo_dev/items/238f6e5060fb838827f6)
```bash
$ sudo apt-get -y install ibus-mozc
$ killall ibus-daemon
$ ibus-daemon -d -x &
```

* GUI は下記
  * [Ubuntu 16.04 LTS : 日本語環境にする ： Server World](https://www.server-world.info/query?os=Ubuntu_16.04&p=japanese)

* US キーボード設定(確認)
  * [Ubuntu 16.04で英語キーボードを使えるようにする方法 - Qiita](http://qiita.com/SUZUKI_Masaya/items/2f2ef9fdb63fe017c6d2)

* システム設定　テキスト入力
  * 次のソースの切り替え
    * 左 Shift キー などにしておく


* 時刻設定
  * [Ubuntu 16.04 LTS : システムのタイムゾーンを設定する ： Server World](https://www.server-world.info/query?os=Ubuntu_16.04&p=timezone)
```bash
$ sudo timedatectl set-timezone Asia/Tokyo
$ timedatectl
$ date
```


---

