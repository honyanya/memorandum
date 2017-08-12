oftware

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

* Google Chrome
  * [Ubuntu 16.04にGoogle Chromeをインストール - Symfoware](http://symfoware.blog68.fc2.com/blog-entry-1874.html)
  * [UbuntuにChromeをインストールする - YoshinoriN's Memento](https://yoshinorin.net/2017/07/24/install-chrome-to-ubuntu/)
  * [Ubuntu 16.04にChromeをインストール: xor](http://alga.moe-nifty.com/xor/2016/09/ubuntu-1604chro.html)
  * https://www.google.com/intl/ja/chrome/browser/desktop/index.html
  * google-chrome-stable_current_amd64.deb

```bash
$ sudo apt-get update
$ sudo apt-get install libappindicator1
$ sudo apt-get -f install

$ cd ~/Documents/tmp/
$ sudo curl -O https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
$ sudo dpkg -i google-chrome-stable_current_amd64.deb
```


* IntelliJ IDEA Community Edition 
  * https://www.jetbrains.com/idea/download/#section=linux
  * https://download-cf.jetbrains.com/idea/ideaIC-2017.2.1.tar.gz
  * ideaIC-2017.2.1.tar.gz

```bash
$ cd ~/Documents/tmp/
$ sudo curl -O https://download-cf.jetbrains.com/idea/ideaIC-2017.2.1.tar.gz
$ tar zxvf ideaIC-2017.2.1.tar.gz -C ~/Documents/bin/

$ cd ~/Documents/bin/idea-IC-172.3544.35/bin/
$ ./idea.sh &
```
ランチャー登録、プライグインインストール


* MySQL Wrokbench
  * [Ubuntu(serversman@vps) に mysql をインストールしつつ、MySQL Workbench を導入してみる](http://zaka-think.com/linux/ubuntu/mysql-workbench/)
  * https://dev.mysql.com/downloads/workbench/
  * https://dev.mysql.com/get/Downloads/MySQLGUITools/mysql-workbench-community-6.3.9-1ubuntu16.04-amd64.deb
  * mysql-workbench-community-6.3.9-1ubuntu16.04-amd64.deb

```bash
$ cd ~/Documents/tmp/

### 事前にブラウザからダウンロードリンク押して Cookie を取得しておく（Oracle JDK と同じ方式）
$ sudo curl -OL --header "MySQL_S=xxx; s_cc=true; s_nr=xxx; gpName=xxx; gpChannel=xxx; gpServer=xxx; s_sq=xxx" https://dev.mysql.com/get/Downloads/MySQLGUITools/mysql-workbench-community-6.3.9-1ubuntu16.04-amd64.deb
$ sudo dpkg -i mysql-workbench-community-6.3.9-1ubuntu16.04-amd64.deb

$ sudo apt-get install -f
$ sudo dpkg -i mysql-workbench-community-6.3.9-1ubuntu16.04-amd64.deb
```
ランチャー登録
 

* Atom
  * https://github.com/atom/atom/releases/download/v1.19.0/atom-amd64.deb
  * atom-amd64.deb

```bash
$ cd ~/Documents/tmp/
$ sudo wget https://github.com/atom/atom/releases/download/v1.19.0/atom-amd64.deb
$ sudo dpkg -i atom-amd64.deb
```
ランチャー登録


* Visual Studio Code
  * [Ubuntu16.04にVisual Studio Codeをインストールする - Desktop Linux のススメ](http://desktop-linux.namakemono345.com/visual-studio-code-ubuntu-gnome-16-04/)
  * https://code.visualstudio.com/download
  * https://go.microsoft.com/fwlink/?LinkID=760868
  * code_1.15.0-1502309460_amd64.deb

```bash
$ cd ~/Documents/tmp/
$ sudo wget https://go.microsoft.com/fwlink/?LinkID=760868 -O code_1.15.0-1502309460_amd64.deb
$ sudo dpkg -i code_1.15.0-1502309460_amd64.deb
```
ランチャー登録


* FileZilla

```bash
$ sudo apt-get update
$ sudo apt-get -y install filezilla
```
ランチャー登録


* (Oracle VirtualBox)
  * [Ubuntu 16.04 LTS に最新の VirtualBox をインストールする - CUBE SUGAR CONTAINER](http://blog.amedama.jp/entry/2017/06/07/223547)
  * https://www.virtualbox.org/wiki/Linux_Downloads
  * http://download.virtualbox.org/virtualbox/5.1.26/virtualbox-5.1_5.1.26-117224~Ubuntu~xenial_amd64.deb
  * virtualbox-5.1_5.1.26-117224~Ubuntu~xenial_amd64.deb
```bash
$ cd ~/Documents/tmp/
$ sudo curl -O http://download.virtualbox.org/virtualbox/5.1.26/virtualbox-5.1_5.1.26-117224~Ubuntu~xenial_amd64.deb
$ sudo dpkg -i virtualbox-5.1_5.1.26-117224~Ubuntu~xenial_amd64.deb

$ sudo apt-get install -f
$ sudo dpkg -i virtualbox-5.1_5.1.26-117224~Ubuntu~xenial_amd64.deb
```
ランチャー登録



* (Vagrant)
  * [Ubuntu 15.04にVirtualbox、Vagrantをインストール](https://inexio.jp/20150707-944/)
  * https://www.vagrantup.com/downloads.html
  * https://releases.hashicorp.com/vagrant/1.9.7/vagrant_1.9.7_x86_64.deb
  * https://releases.hashicorp.com/vagrant/
  * https://releases.hashicorp.com/vagrant/1.9.1/vagrant_1.9.1_x86_64.deb
  * vagrant_1.9.1_i686.deb

```bash
$ cd ~/Documents/tmp/
$ sudo curl -O https://releases.hashicorp.com/vagrant/1.9.1/vagrant_1.9.1_x86_64.deb
$ sudo dpkg -i vagrant_1.9.1_x86_64.deb
$ vagrant -v
```

```bash
$ mkdir ~/Documents/dev/vagrant/
$ cd  ~/Documents/dev/vagrant/
$ vagrant box add centos67 https://github.com/CommanderK5/packer-centos-template/releases/download/0.6.7/vagrant-centos-6.7.box
$ vagrant box list
$ vagrant init centos67
$ vagrant up
$ vagrant ssh
$ vagrant halt
```

---

