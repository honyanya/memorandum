## Mastdon

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)
  * Docker version 17.06.0-ce, build 02c1d87
  * docker-compose version 1.14.0, build c7bdf9e

---

* setup
  * [DockerでMastodonをローカルで動かしてみた！ ので、その方法をご紹介。 | AKITA SOLUTION MAGAZINE](https://ai-create.net/magazine/2017/04/15/mastodonをdockerでローカルに構築してみた！-ので、その方/)
```bash
$ cd ~/Documents/dev/repo/
$ git clone https://github.com/tootsuite/mastodon.git
$ cd mastdon/
$ cp .env.production.sample .env.production
$ mkdir postgress
$ mkdir radis
$ docker-compose build
$ docker-compose run --rm web rake secret
$ docker-compose run --rm web rake secret
$ docker-compose run --rm web rake secret
```

```bash
$ vim .env.production
```
```.env.production
LOCAL_DOMAIN=localhost:3000
LOCAL_HTTPS=false

PAPERCLIP_SECRET=xxx
SECRET_KEY_BASE=yyy
OTP_SECRET=zzz
```

```bash
$ docker-compose run --rm web rails db:migrate
$ docker-compose run --rm web rails assets:precompile
$ docker-compose up -d
```
ブラウザにアクセス

```bash
$ docker-compose run --rm web rails mastodon:confirm_email USER_EMAIL=example@example.com
$ docker-compose stop
```

---

