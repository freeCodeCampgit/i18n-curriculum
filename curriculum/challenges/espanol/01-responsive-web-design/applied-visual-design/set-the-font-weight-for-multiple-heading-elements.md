---
id: 587d781c367417b2b2512ac3
title: Establece el font-weight para varios elementos de títulos
challengeType: 0
videoUrl: 'https://scrimba.com/c/crVWRHq'
forumTopicId: 301069
dashedName: set-the-font-weight-for-multiple-heading-elements
---

# --description--

Se establece el `font-size` de cada etiqueta de título en el último desafío, aquí podrás ajustar el `font-weight`.

La propiedad `font-weight` establece que tan gruesos o delgados son los caracteres en una sección de texto.

# --instructions--

<ul><li>Establece el <code>font-weight</code> de la etiqueta <code>h1</code> en 800.</li><li>Establece el <code>font-weight</code> de la etiqueta <code>h2</code> en 600.</li><li>Establece el <code>font-weight</code> de la etiqueta <code>h3</code> en 500.</li><li>Establece el <code>font-weight</code> de la etiqueta <code>h4</code> en 400.</li><li>Establece el <code>font-weight</code> de la etiqueta <code>h5</code> en 300.</li><li>Establece <code>font-weight</code> de la etiqueta <code>h6</code> en 200.</li></ul>

# --hints--

Tu código debe establecer la propiedad `font-weight` para la etiqueta `h1` en 800.

```js
const h1Element =document.querySelector('h1')
const h1Style = window.getComputedStyle(h1Element);
assert.equal(h1Style?.fontWeight, '800');
```

Tu código debe establecer la propiedad `font-weight` para la etiqueta `h2` en 600.

```js
const h2Element =document.querySelector('h2')
const h2Style = window.getComputedStyle(h2Element);
assert.equal(h2Style?.fontWeight, '600');
```

Tu código debe establecer la propiedad `font-weight` para la etiqueta `h3` en 500.

```js
const h3Element =document.querySelector('h3')
const h3Style = window.getComputedStyle(h3Element);
assert.equal(h3Style?.fontWeight, '500');
```

Tu código debe establecer la propiedad `font-weight` para la etiqueta `h4` en 400.

```js
const h4Element =document.querySelector('h4')
const h4Style = window.getComputedStyle(h4Element);
assert.equal(h4Style?.fontWeight, '400');
```

Tu código debe establecer la propiedad `font-weight` para la etiqueta `h5` en 300.

```js
const h5Element =document.querySelector('h5')
const h5Style = window.getComputedStyle(h5Element);
assert.equal(h5Style?.fontWeight, '300');
```

Tu código debe establecer la propiedad `font-weight` para la etiqueta `h6` en 200.

```js
const h6Element =document.querySelector('h6')
const h6Style = window.getComputedStyle(h6Element);
assert.equal(h6Style?.fontWeight, '200');
```

# --seed--

## --seed-contents--

```html
<style>
  h1 {
    font-size: 68px;

  }
  h2 {
    font-size: 52px;

  }
  h3 {
    font-size: 40px;

  }
  h4 {
    font-size: 32px;

  }
  h5 {
    font-size: 21px;

  }
  h6 {
    font-size: 14px;

  }
</style>
<h1>This is h1 text</h1>
<h2>This is h2 text</h2>
<h3>This is h3 text</h3>
<h4>This is h4 text</h4>
<h5>This is h5 text</h5>
<h6>This is h6 text</h6>
```

# --solutions--

```html
<style>
  h1 {
    font-size: 68px;
    font-weight: 800;
  }
  h2 {
    font-size: 52px;
    font-weight: 600;
  }
  h3 {
    font-size: 40px;
    font-weight: 500;
  }
  h4 {
    font-size: 32px;
    font-weight: 400;
  }
  h5 {
    font-size: 21px;
    font-weight: 300;
  }
  h6 {
    font-size: 14px;
    font-weight: 200;
  }
</style>
<h1>This is h1 text</h1>
<h2>This is h2 text</h2>
<h3>This is h3 text</h3>
<h4>This is h4 text</h4>
<h5>This is h5 text</h5>
<h6>This is h6 text</h6>
```
