---
id: 594da033de4190850b893874
title: 平均／二乗平均平方根
challengeType: 1
forumTopicId: 302228
dashedName: averagesroot-mean-square
---

# --description--

1 から 10 までの数字の二乗平均平方根 (RMS) を計算します。

<abbr title="Root mean square">RMS</abbr> を計算するには、数値の 2 乗の平均の平方根をとります。

$$x\_{\\mathrm{rms}} = \\sqrt {{{x_1}^2 + {x_2}^2 + \\cdots + {x_n}^2} \\over n}. $$

# --hints--

`rms` という関数です。

```js
assert(typeof rms === 'function');
```

`rms([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])` は `6.2048368229954285` と等しくなります。

```js
assert.equal(rms(arr1), answer1);
```

# --seed--

## --after-user-code--

```js
const arr1 = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const answer1 = 6.2048368229954285;
```

## --seed-contents--

```js
function rms(arr) {

}
```

# --solutions--

```js
function rms(arr) {
  const sumOfSquares = arr.reduce((s, x) => s + x * x, 0);
  return Math.sqrt(sumOfSquares / arr.length);
}
```
