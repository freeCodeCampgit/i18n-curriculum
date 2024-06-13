---
id: 5900f4f11000cf542c510003
title: '問題 387: ハーシャッド数'
challengeType: 1
forumTopicId: 302051
dashedName: problem-387-harshad-numbers
---

# --description--

ハーシャッド数またはニーベン数とは、その各位の和によって整除できる数のことです。

201 は 3 (各位の和) で整除できるのでハーシャッド数です。

201 の最下位の桁を切り詰めると 20 になり、これはハーシャッド数です。

20 の最下位の桁を切り詰めると 2 になり、これもハーシャッド数です。

最下位の桁を再帰的に切り詰めても結果が常にハーシャッド数になるようなハーシャッド数を、右桁切り詰め可能なハーシャッド数と呼ぶことにします。

また、

$\frac{201}{3} = 67$ は素数です。

各位の和で割ると素数になるハーシャッド数を、強ハーシャッド数と呼ぶことにします。

ここでは素数 2011 を取り上げます。 最下位の桁を切り詰めると 201 になります。これは強ハルシャッド数であり、右桁が切り詰め可能でもあります。 このような素数を、右桁切り詰め可能な強ハーシャッド素数と呼ぶことにします。

10000 未満の右桁切り詰め可能な強ハーシャッド素数の和は 90619 です。

${10}^{14}$ 未満の右桁切り詰め可能な強ハーシャッド素数の和を求めなさい。

# --hints--

`harshadNumbers()` は `696067597313468` を返す必要があります。

```js
assert.strictEqual(harshadNumbers(), 696067597313468);
```

# --seed--

## --seed-contents--

```js
function harshadNumbers() {

  return true;
}

harshadNumbers();
```

# --solutions--

```js
// solution required
```