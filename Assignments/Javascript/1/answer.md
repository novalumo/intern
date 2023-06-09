# Answer 1

これはあくまでサンプルなので、似たようなことができればOKです。サンプルの書き方は以下の通りです。

- アロー関数式
- switch文で演算記号の条件分岐（ifでも可）
- 文末のセミコロンは省略している（省略できるがなるべく付けた方が良い、Lintを使うと引っかかることも...）

```javascript
/*
  Calculator function
  
  @param numA Number
  @param numB Number
  @param type String
*/
const calculator = (numA, numB, type) => {
  switch (type) {
    case '+':
      return numA + numB
    case '-':
      return numA - numB
    case '*':
      return numA * numB
    case '/':
      return numA / numB
    case '^':
      return numA ** numB
    default:
      return false
  }
}

console.log(calculator(1, 2, '+')) // Output: 3
```
