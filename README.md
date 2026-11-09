# kidswork-blocks

Minecraft Education の「めいろでエージェント」教材で使う MakeCode 拡張機能です。

## 使い方

チュートリアルの Markdown に次を記載します。

```package
kidswork-blocks=github:kidsw4w/kidswork-blocks#v0.1.0
```

## ブロック

「めいろ」カテゴリーの「ボタンを おしたら」の中に、エージェントの動きを入れます。ワールドのスイッチを押すと中の処理を実行します。

## ワールド側の約束

ワールドは `0 97 0` にダイヤモンドブロックを置いて実行を知らせ、`0 97 1` にエメラルドブロックを置いてスタートへのリセットを知らせます。拡張機能はそれぞれを検知後、石に戻します。ワールドには `kw/mc_ready`、`kw/mc_reset`、`kw/mc_go`、`kw/mc_done`、`kw/mc_beat` の各ファンクションが必要です。ぶつかり判定、移動、メッセージなどはワールド側が担当します。
