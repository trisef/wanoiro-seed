# Wanoiro（和の色）

Wanoiro（和の色）は、日本の伝統色を表示するサイト/アプリです。

RustのWebフレームワーク・Seedの勉強の一環として作成しました。

# 使い方

[動くデモページはここにあります](https://trisef.github.io/wanoiro-seed/)。

- 「無作為選択」ボタンを押すと、ランダムに色が表示されます。

以上。

# 手元での動かし方

Seedを使って動かすので、[公式の動かし方](https://github.com/seed-rs/seed-quickstart)を参考にするのが良いですが、メモとして簡単に書いておきます。

1. [Rust](https://www.rust-lang.org)の実行環境を作る。

	- Gitのインストールも必要です。

1. `cargo-make`をインストールする。 `cargo install cargo-make` を実行します。

1. このリポジトリをローカルにコピーする。以下のいずれかです。

	- Zipでダウンロードして解凍する。
	- `git clone https://github.com/trisef/wanoiro-seed.git` を実行する。

1. フォルダ内で `cargo make build` でビルドする。

1. `cargo make serve` でサーバを実行する。

1. Webブラウザで [localhost:8000](http://localhost:8000) へアクセスする。

	- 環境によっては「0.0.0.0:8000 にアクセスしてね」と表示されますが、嘘です。

## ちょっとしたメモ

- HTMLやCSSだけの変更なら、ビルドし直さなくてもブラウザのリロードだけで反映される。

- 公式の記述では、 `cargo make watch` を実行しておくとコードの変更を検知して自動的にコンパイルしてくれることになっているけど、Windows環境ではうまく動作しなかった。どうもファイルの保存タイミングと変更検知のタイミングが重なると以後ダメっぽい。

- Rustのコードを書き換えたあと、もう一回ビルドしてからブラウザでページをリロードするとき、キャッシュを使わない更新（WindowsならCtrl+F5）をしないと反映されないことが多い。
