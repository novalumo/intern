# HTMLタグ

HTMLで使用するタグ。基本的には閉じタグ（スラッシュのついたもの）が必要になるが、そうでないものもある。

以下にはHTMLのソースのみが記載されているため、実際の表示はそれぞれのブラウザで確かめてほしい。

言語仕様の変更によって特定のタグが非推奨等になったり、閉じタグが不要になるなどの変更が加えられる場合があるため、
[MDN](https://developer.mozilla.org/ja/docs/Web)などで常によく確認しておく。

VSCodeなどの[Emmet](https://emmet.io/)が使えるエディタでは、
山カッコ`<`を打たずともタグの種類をタイプして`Enter`や`Tab`を押すことで自動補完してくれる。

※例：VSCodeで`p`と打って`Enter`を押すと`<p>カーソルがここに移動</p>`

Emmetの使い方に関しては[公式ドキュメント](https://docs.emmet.io/)等を参照。


## 基本形

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

- `doctype`宣言

HTMLを記述するために必要な宣言。HTML5の場合は上記に記載のような`<!DOCTYPE html>`のみの表記で問題ない。小文字でも可。

- `html`タグ

HTML文書のルート要素。一応必須。言語を指定する際は`lang`属性を使用する。

- `head`タグ

ブラウザなどでファイルを読み込んだ際には表示されない情報（`meta`など）を記述する枠。文書のヘッダ。

- `body`タグ

ブラウザなどに表示されるコンテンツ部分。文書の本文。

- `<meta charset="UTF-8">`

使用する文字コードがUTF-8であることを明示する。適切な文字コードを記述しないと文字化けすることがあるので必ず記述する。
表記の仕方に誤りがなければ小文字でも可。なお、`<meta ~>`はメタ情報のためのタグ。

- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`

[Viewport](https://developer.mozilla.org/ja/docs/Glossary/Viewport)を定義するもの。レスポンシブなサイトを作る際には最低限この通りに書いておくひ必要がある。

## コメントアウト

`<!--`と`-->`で括ることで、その間の文字列がコメントになる。
VSCodeなどでは、`Ctrl` + `/`（macOSの場合は`Cmd` + `/`）で今いる行をコメントアウトすることが可能。

```html
<!-- このように括った部分がコメントになります -->
<!--
    こうした改行も可能
    ２行目
    ３行目...
-->
```

## 見出し

`<h数字>`タグを使う。`heading`のh。1~6までの数字が入り、`h1`から`h6`にかけて大見出しから小見出しになっていく。
文字の大きさを変更するものではなく、あくまで文書構造に意味をもたせるためのタグであることに注意（SEOに影響することもある）。

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
...
```

## 文章の段落

主に`<p>`タグを使う。`paragraph`のp。閉じタグは省略可能となった。また、段落内での改行は`br`タグで可能。

```html
<p>これは１段落目です</p>
<p>これは２段落目です</p>
<p>このように閉じタグを省略可能
<p>改行をします<br>改行されました</p>
...
```

## 箇条書き

点の箇条書きは`ul`、数字の箇条書きは`ol`タグを使う。項目はそれぞれ`li`タグを使い、閉じタグは省略可能となった。

```html
<!-- 
    ・項目１
    ・項目２
    ...
 -->
<ul>
    <li>項目１</li>
    <li>項目２</li>
    <li>項目３<!-- 閉じタグの省略も可能 -->
</ul>

<!-- 
    1. 項目１
    2. 項目２
    ...
 -->
<ol>
    <li>項目１</li>
    <li>項目２</li>
    <li>項目３<!-- 閉じタグの省略も可能 -->
</ol>
```

## 画像

画像を表示するためには`img`タグを使う。表示する画像のパス（場所）を`src`属性で指定する。
環境によっても異なるが、相対パスと絶対パスのどちらかで指定が可能。
以下の例はHTMLファイルがあるディレクトリにある`images`フォルダ内の`example.jpg`を読み込んでいる。

```html
<img src="images/example.jpg">
```

## スクリプトの記述 / 読み込み

JavaScriptなどを記述したり読み込む際は`script`を使用する。

```html
<!-- 読み込む場合 -->
<script src="index.js"></script>

<!-- HTMLファイル内にJavaScriptを記述する場合 -->
<script>
let message = 'Welcome to HTML!'
console.log(message)
</script>
```