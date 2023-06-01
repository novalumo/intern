# 関数

任意の関数を作成し、プログラム中に使用することができる。

## 定義する方法

```javascript
// 方法1
function 関数名 () {
  // 処理
}

// 方法2（アロー関数）
const 関数名 = () => {
  // 処理
}
```

## 関数の実行

```javascript
function redirect () {
  alert('Googleへ移動します')
  location.href = 'https://www.google.com/'
}

// 呼び出し
redirect()
```

結果：「Googleへ移動します」というアラートを表示、OKをクリックするとGoogleに移動する

## 返値 `return`

関数を実行する際、その結果を返す為には`return`を使う。

```javascript
// 数字を3つ与えて、その和を返すだけの関数
// ここでいうカッコ内のx, y, zは「引数（ひきすう）」という
function sum(x, y, z) {
  return x + y + z
}

// 変数に関数の実行結果（返値）を代入することもできる
let answer = sum(3, 5, 7)
console.log(answer)
```
結果：`15`
