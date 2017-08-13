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
ランチャー登録、プラグインインストール
[Atomにインストールしているパッケージたち（フロントエンド用） - diwao日記](http://diwao.com/2017/01/atom-installed-packages.html)
[Atomのterminal-plusが動かないトラブル - 数弱プログラマのいろいろ](http://namedpython.hatenablog.com/entry/2017/01/01/192739)
[Atomのインストール済みパッケージリストを出力する方法 - Qiita](http://qiita.com/n-oshiro/items/2cad3876468c8d078ae6)
```bash
$ apm list --installed --bare
atom-beautify@0.30.5
autoclose-html@0.23.0
autocomplete-paths@2.4.0
busy-signal@1.4.3
color-picker@2.2.5
editorconfig@2.2.2
emmet@2.4.3
file-icons@2.1.10
highlight-line@0.12.0
highlight-selected@0.13.1
intentions@1.1.5
linter@2.2.0
linter-csslint@1.3.4
linter-eslint@8.2.1
linter-scss-lint@3.1.0
linter-ui-default@1.6.4
platformio-ide-terminal@2.5.5
pretty-json@1.6.4
project-manager@3.3.5
regex-railroad-diagram@0.19.3
script@3.15.0
split-diff@1.4.3
terminal-plus@0.14.5
trailing-spaces@0.4.0
```




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

$ sudo apt-get -y install \
    linux-headers-4.4.0-91-generic \
    linux-headers-generic
$ sudo /sbin/vboxconfig
$ VBoxManage --version
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

$ vagrant box add boxcutter/centos67-i386
$ vagrant box list

$ mkdir -p boxcutter/centos67-i386/ && boxcutter/centos67-i386/
$ vagrant init boxcutter/centos67-i386
$ vagrant up
$ vagrant ssh
$ vagrant halt
```

---

