---
name: "Rails APIモードでプロジェクト作成"
slug: "pghugkk"
tags: ["Ruby"]
---

# Rails APIモードでプロジェクト作成

## bundle init

```
bundle init
```

Gemfileが作られる

## Gemfileを修正する

```ruby
gem 'rails'
```

上記のコメントをはずす

## bundle install

```
bundle install --path vendor/bundle --jobs=4
```

## mysql2用の設定

```
bundle config --local build.mysql2 "--with-ldflags=-L/usr/local/opt/openssl/lib"
```

## rails new

```
bundle exec rails new . -B --api -d mysql --skip-test
```

### rails new のオプション

| オプション | 説明 |
| - | - |
| --skip-test | minitestのスキップ |
| -B | bundle install のスキップ |
| -d mysql | mysql を使用する |

## .gitignore に以下を追記

```
vendor/bundle
```

## DBセットアップ

```
bundle exec rails db:setup
```





