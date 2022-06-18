## Description
簡単なページ運用の操作を記載しています.

## ページの編集
contents/のファイルを編集する.マークダウン記法.

## ページの追加
```
hugo new hoge.md
```

### Newsの追加
```
hugo new news/hoge.md
```

news/hoge.md上部を埋める.

## メニューへのタブの追加
config.tomlの

```
[menu]
```

に

```
[[menu.main]]
  identifier = "hoge"
  name = "Hoge"
  url = "/hoge/"
  weight = fuga
```

を追加する.