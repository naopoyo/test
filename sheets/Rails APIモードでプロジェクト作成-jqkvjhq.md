---
name: "Rails APIモードでプロジェクト作成"
slug: "jqkvjhq"
tags: ["Ruby"]
---


## プロジェクト作成

```
bundle init
```

Gemfileが作られる

```
vi Gemfile
```

Gemfileを修正する。

```ruby
gem 'rails'
```

Gemfileのコメントをはずす

```
bundle install --path vendor/bundle --jobs=4
```

```
bundle config --local build.mysql2 "--with-ldflags=-L/usr/local/opt/openssl/lib"
```

bundle install mysql2 のために

```
bundle exec rails new . -B --api -d mysql --skip-test
```

APIモードでプロジェクト作成

.gitignore に以下を追記する。

```
vendor/bundle
```

```
bundle exec rails db:setup
```

DBセットアップ


## rails new のオプション

| --skip-test | minitestのスキップ |
| -B | bundle install のスキップ |
| -d mysql | mysql を使用する |

## 関連シート

[Ruby](https://hackersheet.com/rrombjd/sheets/ovxbnoj)

