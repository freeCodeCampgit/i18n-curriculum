---
id: 587d778f367417b2b2512aad
title: >-
  Щоб уникнути проблем, пов'язаних із дальтонізмом, ретельно добирайте кольори, що передають інформацію
challengeType: 0
videoUrl: 'https://scrimba.com/c/c437as3'
forumTopicId: 301011
dashedName: >-
  avoid-colorblindness-issues-by-carefully-choosing-colors-that-convey-information
---

# --description--

There are various forms of colorblindness. These can range from a reduced sensitivity to a certain wavelength of light to the inability to see color at all. The most common form is a reduced sensitivity to detect greens.

Наприклад, якщо подібні між собою зелені кольори є на передньому та задньому планах вашого контенту, користувач із дальтонізмом може їх не розрізнити. Подібні один до одного кольори вважаються сусідніми на спектральному колі, тож не слід використовувати їхні комбінації для передачі важливої інформації.

**Примітка:** деякі онлайн-інструменти вибору кольорів мають візуальні симуляції того, як бачать кольори люди з різними видами дальтонізму. Це чудові ресурси на додачу до онлайн-калькуляторів для перевірки контрасту.

# --instructions--

Кіт Кампер тестує різні стилі для важливої кнопки, проте жовтий (`#FFFF33`) колір фону `background-color` і зелений (`#33FF33`) колір тексту `color` розташовані по сусідству на спектральному колі, і їх майже не розрізнити користувачам із дальтонізмом. (Їхня схожа освітленість також зане проходитьперевірку на коефіцієнт контрасності). Замініть колір тексту `color` на темно-блакитний (`#003366`), щоб вирішити обидві проблеми.

# --hints--

Ваш код має змінити колір тексту `color` для кнопки `button` на темно-блакитний.

```js
const button = document.querySelector('button');
const buttonColor = window.getComputedStyle(button).color; 
assert.equal(buttonColor, 'rgb(0, 51, 102)');
```

# --seed--

## --seed-contents--

```html
<head>
  <style>
  button {
    color: #33FF33;
    background-color: #FFFF33;
    font-size: 14px;
    padding: 10px;
  }
  </style>
</head>
<body>
  <header>
    <h1>Danger!</h1>
  </header>
  <button>Delete Internet</button>
</body>
```

# --solutions--

```html
<head>
  <style>
    button {
      color: #003366;
      background-color: #FFFF33;
      font-size: 14px;
      padding: 10px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Danger!</h1>
  </header>
  <button>Delete Internet</button>
</body>
```
