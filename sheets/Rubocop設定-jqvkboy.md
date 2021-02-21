---
name: "Rubocop設定"
slug: "jqvkboy"
tags: ["ruby"]
---

プロジェクトルートに .rubocp.yml を作る。

```yaml
AllCops:
  Exclude:
    - bin/**/*
    - db/schema.rb
    - db/migrate/*.rb
    - node_modules/**/*
    - tmp/**/*
    - vendor/**/*
```

```
AllCops:
  DisplayStyleGuide: true
  ExtraDetails: true
  TargetRubyVersion: 2.6
  NewCops: enable
```

```yaml
Style/Documentation:
  Enabled: false
```

コメントの無いクラスを許可する

```yaml
Style/FrozenStringLiteralComment:
  Enabled: false
```


## 関連シート

[Ruby](https://hackersheet.com/rrombjd/sheets/ovxbnoj)

