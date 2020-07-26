# Casper-ja

A fork of [TryGhost/Casper](http://github.com/tryghost/casper), the default theme for [Ghost](http://github.com/tryghost/ghost/) blogging engine. This solves the issues heppen with Japanese contents, and, adds some minor adjustments for readability.

Note that we decided to use *gothic* (sans-serif) rather than *mincho* (serif) due to limited number of clients which have beautiful serif fonts, while you can use `mincho` branch to use mincho up to your preference.

ブログエンジンGhostの[Ghost](http://github.com/tryghost/ghost/)デフォルトテーマであるCasperを日本語対応させたフォークです。各種フォントに日本語フォントを指定し、日本語に合わせて若干の調整を行っています。

綺麗な日本語の明朝体を表示できる環境がまだ完全に普及しきっていないことを考慮して、オリジナルでは本文はセリフ体であるところを、記事本文はゴシック体に変更しています。明朝体を利用したい場合、`mincho`ブランチを利用することができます。

## 方針

1. できるかぎりオリジナルの雰囲気を尊重する

2. 多くの環境で、高品質なフォントで表示されるようにする

3. Webフォントは新たに追加しない

## 日本語に合わせた調整

1. 日本語フォントを指定しました。

   優先順位:
    - Windows: 游ゴシック → ヒラギノ角ゴ → メイリオ
    - Mac: ヒラギノ角ゴ（-apple-system, BlinkMacSystemFont） → 游ゴシック → メイリオ

   （`mincho`は: 游明朝→ヒラギノ明朝→HGS明朝E。ただし太字部分は上記に従いゴシックになります。）

   ただし見出しはヒラギノ角ゴ→メイリオ→游ゴシックです。これは元々指定されているOpen Sans Boldとの調和を考慮した結果です。

   游ゴシックは、游ゴシック Regularだと細すぎるのでMediumを優先して使うようにしています。（参考: https://wemo.tech/1155）

2. 字間を調整しました。

## 好みが分かれそうなところ

記事本文の欧文には、日本語フォントの従属欧文を利用せず、Open Sans（ゴシック体版）あるいはGeorgia（明朝体版）にしました。これは日本語で使ったフォントとの調和も悪くないように感じたので、方針1に沿ったという理由からです。従属欧文を利用したい場合は、`assets/css/screen.css`内を`Georgia`または`Open Sans`で検索し、日本語フォントと同時に指定されている部分について、当該欧文フォント名を削除してください。

例:

変更前
```
body {
    ...
    font-family: "Open Sans", "游ゴシック体", "Yu Gothic", YuGothic, "ヒラギノ角ゴ Pro", "Hiragino Kaku Gothic Pro", "メイリオ", "Meiryo", sans-serif;
    ...
}
```

変更後
```
body {
    ...
    font-family: "游ゴシック体", "Yu Gothic", YuGothic, "ヒラギノ角ゴ Pro", "Hiragino Kaku Gothic Pro", "メイリオ", "Meiryo", sans-serif;
    ...
}
```

## (v1版との違い)

Casper v1系時代に行っていたいくつかの修正は削除されました。具体的には以下のものです。v1向けの説明は[README-v1.md](./README-v1.md)にあります。

- 任意の合字 (dlig) の無効化: Casper本体で修正されたようです。
- はてなブックマークでシェアリンクの追加: そもそも記事をシェアするリンクが削除されました。

## Copyright & License (for the modifications)

Copyright (c) 2016 @mecab - Released under the MIT License.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

----

Original readme follows:

----

# Casper

The default theme for [Ghost](http://github.com/tryghost/ghost/).

To download, visit the [releases](https://github.com/TryGhost/Casper/releases) page.

## Copyright & License

Copyright (c) 2013-2016 Ghost Foundation - Released under the MIT License.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
