---
id: 587d7dad367417b2b2512b77
title: Визначення функції-конструктора
challengeType: 1
forumTopicId: 16804
dashedName: define-a-constructor-function
---

# --description--

<dfn>Constructors</dfn> are functions that create new objects. They define properties and behaviors that will belong to the new object. Think of them as a blueprint for the creation of new objects.

Ось приклад конструктора:

```js
function Bird() {
  this.name = "Albert";
  this.color = "blue";
  this.numLegs = 2;
}
```

Цей конструктор визначає об’єкт `Bird` із властивостями `name`, `color` та `numLegs` зі значеннями Albert, blue та 2 відповідно. При створенні конструкторів дотримуються кількох умов:

<ul><li>Constructors are defined with a capitalized name to distinguish them from other functions that are not <code>constructors</code>.</li><li>Конструктори використовують ключове слово <code>this</code>, щоб налаштувати властивості створеного об’єкта. <code>this</code> всередині конструктора посилається на новий створений об’єкт.</li><li>Конструктори визначають властивості та поведінку, а не повертають значення, як це можуть робити інші функції.</li></ul>

# --instructions--

Створіть конструктор `Dog` з властивостями `name`, `color` та `numLegs`, а потім налаштуйте їхні значення на рядок, рядок та число відповідно.

# --hints--

`Dog` повинен мати властивість `name` зі значенням рядка.

```js
assert(typeof new Dog().name === 'string');
```

`Dog` повинен мати властивість `color` зі значенням рядка.

```js
assert(typeof new Dog().color === 'string');
```

`Dog` повинен мати властивість `numLegs` зі значенням числа.

```js
assert(typeof new Dog().numLegs === 'number');
```

# --seed--

## --seed-contents--

```js

```

# --solutions--

```js
function Dog (name, color, numLegs) {
  this.name = 'name';
  this.color = 'color';
  this.numLegs = 4;
}
```
