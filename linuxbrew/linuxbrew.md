## linuxbrew

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

* install
  * [Ubuntu 15.10 に Linuxbrew をインストールしてみる - らくがきちょう](http://sig9.hatenablog.com/entry/2016/04/05/235753)
  * [環境変数の確認とパスの追加](http://qiita.com/comsqHoshi/items/c847ad51af388d2dbb4a)

```bash
### 必要なものをインストール
$ sudo apt-get -y install \
    build-essential \
    curl \
    git \
    python-setuptools \
    ruby
### linuxbrew インストール
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Linuxbrew/linuxbrew/go/install)"
### パスの設定
$ echo 'export PATH="$HOME/.linuxbrew/bin:$PATH"' >> ~/.bashrc
$ echo 'export MANPATH="$HOME/.linuxbrew/share/man:$MANPATH"' >> ~/.bashrc
$ echo 'export INFOPATH="$HOME/.linuxbrew/share/info:$INFOPATH"' >> ~/.bashrc
$ source ~/.bashrc
### チェック
$ brew doctor
$ brew update
$ brew -v
```

---

