---
id: 587d781d367417b2b2512ac8
title: Mudar o estilo de um link ao passar o mouse
challengeType: 0
videoUrl: 'https://scrimba.com/c/cakRGcm'
forumTopicId: 301035
dashedName: adjust-the-hover-state-of-an-anchor-tag
---

# --description--

This challenge will touch on the usage of pseudo-classes. A pseudo-class is a keyword that can be added to selectors, in order to select a specific state of the element.

Por exemplo, o estilo de um link pode ser alterado quando o cursor do mouse está sobre ele usando o seletor de pseudo-classe `:hover`. O código CSS para alterar a propriedade `color` de um link para vermelho quando o mouse está sobre ele é este:

```css
a:hover {
  color: red;
}
```

# --instructions--

O editor de código tem uma declaração de estilo CSS que estiliza todas as tags `a` com a cor preta. Adicione uma declaração de estilo para que, quando o usuário passar o mouse sobre a tag `a`, a propriedade `color` mude para azul.

# --hints--

A propriedade `color` do link deve permanecer preta. A cor do texto deve mudar apenas no estado `:hover`.

```js
const anchorElement = document.querySelector("a"); 
const anchorStyle = window.getComputedStyle(anchorElement);
assert.equal(anchorStyle?.color, 'rgb(0, 0, 0)');
```

O link deve ter a propriedade `color` de valor azul ao passar o mouse sobre ele.

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
