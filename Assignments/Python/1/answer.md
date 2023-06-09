# Answer 1

- 3つ目の引数はタイプ（type）を表しますが、eがないのはtypoではなくPythonには`type`という関数があり予約語のため使えないためです。

```python
'''
Calculator function

@param numA: Number
@param numB: Number
@param typ: String
'''

def calculator(numA, numB, typ):
  if typ == '+':
    return numA + numB
  elif typ == '-':
    return numA - numB
  elif typ == '*':
    return numA * numB
  elif typ == '/':
    return numA / numB
  elif typ == '^':
    return numA ** numB
  else:
    return false

print(calculator(2, 2, '^')) # Output: 4

```
