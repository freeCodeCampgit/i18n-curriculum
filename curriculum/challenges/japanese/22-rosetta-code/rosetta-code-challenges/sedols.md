---
id: 59d9c6bc214c613ba73ff012
title: SEDOLコード
challengeType: 1
forumTopicId: 302305
dashedName: sedols
---

# --description--

<abbr title="Stock Exchange Daily Official List">SEDOL</abbr> は、ロンドン証券取引所が発行する証券識別番号のリストです。

6 桁の <abbr title="Stock Exchange Daily Official List">SEDOL コード</abbr>の数字リストごとに、チェックディジットを計算して追加します。 つまり、左辺の入力文字列に対して、関数は対応する右辺の文字列を返す必要があります。

<pre>
710889 => 7108899
B0YBKJ => B0YBKJ7
406566 => 4065663
B0YBLH => B0YBLH2
228276 => 2282765
B0YBKL => B0YBKL9
557910 => 5579107
B0YBKR => B0YBKR5
585284 => 5852842
B0YBKT => B0YBKT7
B00030 => B000300
</pre>

各入力が正しい形式であるか、特に、SEDOL 文字列で許可されている有効な文字であるかについて確認を行います。 無効な入力に対して関数は `null` を返す必要があります。

# --hints--

`sedol` は関数とします。

```js
assert(typeof sedol === 'function');
```

`sedol('a')` は null を返す必要があります。

```js
assert(sedol('a') === null);
```

`sedol('710889')` は '7108899' を返す必要があります。

```js
assert(sedol('710889') === '7108899');
```

`sedol('BOATER')` は null を返す必要があります。

```js
assert(sedol('BOATER') === null);
```

`sedol('228276')` は '2282765' を返す必要があります。

```js
assert(sedol('228276') === '2282765');
```

# --seed--

## --seed-contents--

```js
function sedol(input) {
  const checkSum = 0

  return checkSum;
}
```

# --solutions--

```js
function sedol(input) {
  const checkDigit = sedolCheckDigit(input);
  if (checkDigit !== null) {
    return input + checkDigit;
  }
  return null;
}

const weight = [1, 3, 1, 7, 3, 9, 1];
function sedolCheckDigit(char6) {
  if (char6.search(/^[0-9BCDFGHJKLMNPQRSTVWXYZ]{6}$/) === -1) {
    return null;
  }

  let sum = 0;
  for (let i = 0; i < char6.length; i++) {
    sum += weight[i] * parseInt(char6.charAt(i), 36);
  }
  const checkSum = (10 - (sum % 10)) % 10;
  return checkSum.toString();
}
```
