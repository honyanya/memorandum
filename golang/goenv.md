## goenv

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

* anyenv を用いて goenv をインストール
```bash
$ anyenv install goenv
$ exec $SHELL -l
$ anyenv versions
$ which goenv
```

* goenv を用いて golang をインストール 
```bash
$ goenv install --list
$ goenv install 1.8.4
$ goenv versions
$ goenv global 1.8.4
$ go version
```

* hello world
```bash
$ cat <<EOF > hello.go
package main

import "fmt"

func main() {
  fmt.Printf("Hello World\n")
}
EOF


$ go run hello.go
Hello World

```

---

* 参考
  * [AnyenvでGoのバージョン管理 - Melchior](http://suguru03.hatenablog.com/entry/2017/03/28/130849)
  * [Golangをgoenvを使ってインストールしてみた - Qiita](https://qiita.com/walkers/items/761b2a5e58849176a633)
  * [Go言語のHello Worldを3分で試す - Qiita](https://qiita.com/techys/items/44a712a76859fe0a9dea)

---


