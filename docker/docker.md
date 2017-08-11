## docker

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)
  * Docker version 17.06.0-ce, build 02c1d87

---

* install
* [[Docker] ubuntu 14.04/16.04にDockerをインストール - Qiita](http://qiita.com/koara-local/items/ee887bab8c7186d00a88)
* [Get Docker CE for Ubuntu | Docker Documentation](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/#install-from-a-package)
```bash
$ sudo apt-get remove \
    docker \
    docker-engine \
    docker.io

$ sudo apt-get update
$ sudo apt-get -y install \
    linux-image-extra-$(uname -r) \
    linux-image-extra-virtual
$ sudo apt-get update
$ sudo apt-get -y install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo apt-key fingerprint 0EBFCD88
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
$ sudo apt-get update
$ sudo apt-get -y install docker-ce
$ apt-cache madison docker-ce
$ sudo apt-get -y install docker-ce=17.06.0~ce-0~ubuntu
$ sudo docker run hello-world

### sudo 無しでも使えるよう docker グループに追加
$ sudo groupadd docker
$ sudo gpasswd -a $USER docker

$ docker -v
```

---

