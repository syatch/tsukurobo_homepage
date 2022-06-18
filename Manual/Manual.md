## Description
このマニュアルは,tsukurobo_homepageの管理を始めるにあたって必要な環境構築手順を記載したものです.

## Hugoのインストール
以下のページに従い,HUGOをインストールする.

[Install HUGO](https://gohugo.io/getting-started/installing/)

### UbuntuへのHUGOのインストール
以下Ubuntu20.04で操作を確認(2022/06)

brewをインストール
参考　[Homebrew](https://brew.sh/)

brewがインストールされていなかった場合,以下のコマンドを実行する.
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"' >> /home/syatch/.profile
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
```

Hugoをインストールする.
```
brew install hugo
```

hugoがインストールされたことを確認.
```
hugo version
```

## HUGO Themes : Tellaの導入
すでに済んでいる.備忘のため,以下にURLを記載する.

[HUGO Themes:Tella](https://themes.gohugo.io/themes/tella/)

## npmのインストール
tsukurobo/で以下のコマンドを実行.

```
npm install
```

## ローカルで作成したサイトを確認
```
npm run start
```

ここで,以下のようなエラーが出る場合がある.
```
Error: yargs parser supports a minimum Node.js version of 12. Read our(以下略
```

node.jsのバージョンが古いのが原因.
以下のコマンドでnode.jsのバージョンを確認.

```
node --version
```

[nodejs](https://nodejs.org/ja/)
で最新版を確認.

```
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt-get install -y nodejs
```
再度実行.
```
npm run start
```

ブラウザで[http://localhost:1313/](http://localhost:1313/)を開く.

## サイトのビルド
```
npm run build
```

tsukurobo/public/にビルドされる.