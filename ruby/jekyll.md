## jekyll

* 環境
  * Mac OS X El Capitan
  * Vagrant 1.9.3
  * Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-91-generic x86_64)

---

```bash
### 動作確認用のディレクトリ
$ mkdir ~/Documents/dev/jekyll-test/ && cd ~/Documents/dev/jekyll-test/
### bundler があることを確認
$ rbenv exec gem list | grep bundler

### Gemfile 作成
$ rbenv exec bundler init
$ cat <<EOF > Gemfile
# frozen_string_literal: true
source "https://rubygems.org"

git_source(:github) {|repo_name| "https://github.com/#{repo_name}" }

gem "jekyll"
EOF

### bundler 実行
$ bundler install --path vendor/bundle
### jekyll 確認
$ bundler exec jekyll -v

### jekyll プロジェクト作成
### カレントディレクトリに作成するため、 -f . とする
$ bundler exec jekyll new -f .

### Gemfile が更新されたので再度 bundler install
bundler install --path vendor/bundle
### サーバ起動
$ bundler exec jekyll server

```

---

* 参考
  * [Jekyll + GitHubページで静的サイトorブログを作る簡単な手順 | 酒と涙とRubyとRailsと](http://morizyun.github.io/blog/jekyll-blog-github-page/)
  * [Jekyllバージョン3.1の導入とGitHub Pagesを試す | 株式会社テクノブレーン](http://www.tbn.co.jp/posts/technology/2016/02/12/jekyll-3.html)

---


