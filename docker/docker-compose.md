## docker

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)
  * Docker version 17.06.0-ce, build 02c1d87
  * docker-compose version 1.14.0, build c7bdf9e

---

* install
  * [Docker Compose - インストール - Qiita](http://qiita.com/zembutsu/items/dd2209a663cae37dfa81)
  * [Install Docker Compose | Docker Documentation](https://docs.docker.com/compose/install/)
```bash
$ sudo apt-get -y install curl
$ sudo -i
# curl -L https://github.com/docker/compose/releases/download/1.14.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
# exit
$ sudo chmod +x /usr/local/bin/docker-compose
$ docker-compose --version
```

---

