---
id: 587d781d367417b2b2512ac8
title: 調整錨標籤的懸停狀態
challengeType: 0
videoUrl: 'https://scrimba.com/c/cakRGcm'
forumTopicId: 301035
dashedName: adjust-the-hover-state-of-an-anchor-tag
---

# --description--

This challenge will touch on the usage of pseudo-classes. A pseudo-class is a keyword that can be added to selectors, in order to select a specific state of the element.

比如，可以使用 `:hover` 僞類選擇器來選取錨標籤的懸停狀態。 下面的代碼可以在鼠標懸停在錨標籤上時將其 `color` 變成紅色：

```css
a:hover {
  color: red;
}
```

# --instructions--

代碼編輯器裏面已經有了一個 CSS 規則把所有的 `a` 標籤定義成了黑色。 請添加一個規則，使得用戶懸停在 `a` 標籤時，標籤的 `color` 變成藍色。

# --hints--

錨標籤的 `color` 應該保持黑色，應只添加 `:hover` CSS 規則。

```js
const anchorElement = document.querySelector("a"); 
const anchorStyle = window.getComputedStyle(anchorElement);
assert.equal(anchorStyle?.color, 'rgb(0, 0, 0)');
```

懸停錨標籤時它的 `color` 應該變成藍色。

```js
assert.match(code,
    /a:hover\s*?{\s*?color:\s*?(blue|rgba\(\s*?0\s*?,\s*?0\s*?,\s*?255\s*?,\s*?1\s*?\)|#00F|rgb\(\s*?0\s*?,\s*?0\s*?,\s*?255\s*?\))\s*?;\s*?}/gi
  );
```

# --seed--

## --seed-contents--

```html
<style>
  a {
    color: #000;
  }



</style>
<a href="https://freecatphotoapp.com/" target="_blank">CatPhotoApp</a>
```

# --solutions--

```html
<style>
  a {
    color: #000;
  }
  a:hover {
    color: rgba(0,0,255,1);
  }
</style>
<a href="https://freecatphotoapp.com/" target="_blank">CatPhotoApp</a>
```
