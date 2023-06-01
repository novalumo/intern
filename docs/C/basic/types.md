# データ型

数字や文字などのデータをメモリ上に確保する領域やバイト長、確保した領域の扱い方などを指定するもの。

## 型の種類

<table>
<thead>
<tr>
<th>種類</th><th>データ型</th><th>データ型の名称</th><th>バイト長</th><th>値の範囲</th>
</tr>
</thead>
<tbody>
<tr>
<td>型なし</td><td>void</td><td>void型</td><td>ー</td><td>ー</td>
</tr>
<tr>
<td rowspan="2">文字列</td><td>(unsigned) char</td><td>(符号なし)文字型</td><td>1</td><td>0~255</td>
</tr>
<tr>
<td>signed char</td><td>符号付き文字型</td><td>1</td><td>-128~127</td>
</tr>
<tr>
<td rowspan="8">整数型</td><td>unsigned short int</td><td>符号なし短整数型</td><td>2</td><td>0～65535</td>
</tr>
<tr>
<td>(signed) short int</td><td>(符号付き)短整数型</td><td>2</td><td>-32768～32767</td>
</tr>
<tr>
<td>unsigned int</td><td>符号なし整数型</td><td>4</td><td>0～4294967295</td>
</tr>
<tr>
<td>(signed) int</td><td>(符号付き)整数型</td><td>4</td><td>-2147483648～2147483647</td>
</tr>
<tr>
<td>unsigned long int</td><td>符号なし長整数型</td><td>4</td><td>0～4294967295</td>
</tr>
<tr>
<td>(signed) long int</td><td>(符号付き)長整数型</td><td>4</td><td>-2147483648～2147483647</td>
</tr>
<tr>
<td>unsigned long long int</td><td>符号なし長長整数型</td><td>8</td><td>0～18446744073709551615</td>
</tr>
<tr>
<td>(signed) long long int</td><td>(符号付き)長長整数型</td><td>8</td><td>-9223372036854775808<br>
～9223372036854775807</td>
</tr>
<tr>
<td rowspan="2">浮動小数点型</td><td>float</td><td>単精度浮動小数点型</td><td>4</td><td>最小の正の数：1.175494e-38<br>
最大値：3.402823e+38</td>
</tr>
<tr>
<td>double</td><td>倍精度浮動小数点型</td><td>8</td><td>最小の正の数：2.225074e-308<br>
最大値：1.797693e+308</td>
</tr>
</tbody>
</table>

## 変換指定子
 
| 指定子 | 対応する型 | 説明 |
| --- | --- | --- |
| c | char | 文字 |
| s | char * | 文字列 |
| d | int, short | 10進の整数 |
| u | unsigned int, unsigned short | 10進の符号なし整数 |
| o | int, short,<br>unsigned int,<br>unsigned short | 8進の整数 |
| x | int, short,<br>unsigned int,<br>unsigned short | 16進の整数 |
| f | float | 浮動小数点数 |
| e | float | 浮動小数点数の指数表示 |
| g | float | %eもしくは%fのどちらか最適な形式の浮動小数点数 |
| ld | long | 10進の倍精度整数 |
| lu | unsinged long | 10進の符号なし倍精度整数 |
| lo | long, unsinged long | 8進の倍精度整数 |
| lx | long, unsinged long | 16進の倍精度整数 |
| lf | double | 倍精度浮動小数点数 |
| a | double | 16進の倍精度浮動小数点数 |

## `printf`での出力方法

`printf("書式文字列", 変数a, 変数b, ...);`

- 改行は`\n`を使用する。（例：`printf("こんにちは\n");`）
- 出力表示したい文字列の中で変数の値を表示する場合は、上記の表に記載の`変換指定子`を使用する。以下例。
```c
#include <stdio.h>

int main(void) {
  char *myName = "太郎";
  printf("こんにちは、%sさん\n", myName);
  return 0;
}
// 出力：こんにちは、太郎さん
```
