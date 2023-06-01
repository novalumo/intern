# コンソール

## 開発者ツール

Chromeなどのブラウザで`F12`キーもしくは`Ctrl`+`Alt`+`I`(macOSの場合は`Cmd`+`Opt`+`I`)で開発者ツールが開く。

開発者ツールのConsoleタブを開くと、JavaScriptのWarning, Error, ログなどの確認ができ、対話型でJavaScriptを使用することができる。

主にデバッグなどで使用することができ、ソースコードの中に`debugger`を記述していると、その処理が実行されるタイミングで処理が一時停止しブラウザ機能のデバッグツールが開く。

### 使用例

```javascript
let isLoading = false
< undefined
console.log(isLoading)
false
< undefined
isLoading = true
true
console.log(isLoading)
true
< undefined
```

## `console.log()`

`console.log()`を使って、変数の中身を確認したり、処理中のログを表示させることができる。

### 使用例

```javascript
console.log('Hello, world')
```
結果：`Hello, world`

```javascript
let name = 'John'
console.log('Welcome, ' + name)
```
結果：`Welcome, John`
