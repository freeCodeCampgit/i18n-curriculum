---
id: bad82fee1348bd9aedf08721
title: 使用 RGB 混合顏色
challengeType: 0
videoUrl: 'https://scrimba.com/c/cm24JU6'
forumTopicId: 18368
dashedName: use-rgb-to-mix-colors
---

# --description--

Just like with hex code, you can mix colors in RGB by using combinations of different values.

# --instructions--

將 `style` 標籤裏面中的十六進制編碼替換爲正確的 RGB 值。

<table><tbody><tr><th>Color</th><th>RGB</th></tr><tr><td>Blue</td><td><code>rgb(0, 0, 255)</code></td></tr><tr><td>Red</td><td><code>rgb(255, 0, 0)</code></td></tr><tr><td>Orchid</td><td><code>rgb(218, 112, 214)</code></td></tr><tr><td>Sienna</td><td><code>rgb(160, 82, 45)</code></td></tr></tbody></table>

# --hints--

文本內容爲 `I am red!` 的 `h1` 元素的 `color` 值應爲紅色。

```js
assert($('.red-text').css('color') === 'rgb(255, 0, 0)');
```

紅色應使用 `rgb` 值來表示。

```js
assert(
  code.match(
    /\.red-text\s*{\s*color\s*:\s*rgb\(\s*255\s*,\s*0\s*,\s*0\s*\)\s*;?\s*}/gi
  )
);
```

文本內容爲 `I am orchid!` 的 `h1` 元素的 `color` 應爲淡紫色。

```js
assert($('.orchid-text').css('color') === 'rgb(218, 112, 214)');
```

淡紫色應使用 `rgb` 值來表示。

```js
assert(
  code.match(
    /\.orchid-text\s*{\s*color\s*:\s*rgb\(\s*218\s*,\s*112\s*,\s*214\s*\)\s*;?\s*}/gi
  )
);
```

文本內容爲 `I am blue!` 的 `h1` 元素的 `color` 應爲藍色。

```js
assert($('.blue-text').css('color') === 'rgb(0, 0, 255)');
```

藍色應使用 `rgb` 值來表示。

```js
assert(
  code.match(
    /\.blue-text\s*{\s*color\s*:\s*rgb\(\s*0\s*,\s*0\s*,\s*255\s*\)\s*;?\s*}/gi
  )
);
```

文本內容爲 `I am sienna!` 的 `h1` 元素的 `color` 應爲赭黃色。

```js
assert($('.sienna-text').css('color') === 'rgb(160, 82, 45)');
```

赭黃色應使用 `rgb` 值來表示。

```js
assert(
  code.match(
    /\.sienna-text\s*{\s*color\s*:\s*rgb\(\s*160\s*,\s*82\s*,\s*45\s*\)\s*;?\s*}/gi
  )
);
```

# --seed--

## --seed-contents--

```html
<style>
  .red-text {
    color: #000000;
  }
  .orchid-text {
    color: #000000;
  }
  .sienna-text {
    color: #000000;
  }
  .blue-text {
    color: #000000;
  }
</style>

<h1 class="red-text">I am red!</h1>

<h1 class="orchid-text">I am orchid!</h1>

<h1 class="sienna-text">I am sienna!</h1>

<h1 class="blue-text">I am blue!</h1>
```

# --solutions--

```html
<style>
  .red-text {
    color: rgb(255, 0, 0);
  }
  .orchid-text {
    color: rgb(218, 112, 214);
  }
  .sienna-text {
    color: rgb(160, 82, 45);
  }
  .blue-text {
    color:rgb(0, 0, 255);
  }
</style>

<h1 class="red-text">I am red!</h1>

<h1 class="orchid-text">I am orchid!</h1>

<h1 class="sienna-text">I am sienna!</h1>

<h1 class="blue-text">I am blue!</h1>
```
