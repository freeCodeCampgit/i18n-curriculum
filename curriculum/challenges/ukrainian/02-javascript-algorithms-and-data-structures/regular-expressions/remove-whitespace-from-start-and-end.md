---
id: 587d7dbb367417b2b2512bac
title: Видалення пробілу з початку та кінця
challengeType: 1
forumTopicId: 301362
dashedName: remove-whitespace-from-start-and-end
---

# --description--

Sometimes whitespace characters around strings are not wanted but are there. Typical processing of strings is to remove the whitespace at the start and end of it.

# --instructions--

Напишіть регулярний вираз та використайте відповідні методи рядків, щоб видалити пробіли на початку та в кінці рядків.

**Примітка:** метод `String.prototype.trim()` не спрацює, але вам потрібно використати регулярні вирази у цьому завданні.

# --hints--

`result` має дорівнювати рядку `Hello, World!`

```js
assert(result === 'Hello, World!');
```

Не використовуйте метод `String.prototype.trim()` у розв’язку.

```js
assert(!__helpers.removeJSComments(code).match(/\.?[\s\S]*?trim/));
```

Не налаштовуйте змінну `result` на рядок напряму

```js
assert(!__helpers.removeJSComments(code).match(/result\s*=\s*["'`].*?["'`]/));
```

Не змінюйте значення змінної `hello`.

```js
assert(hello === '   Hello, World!  ');
```

# --seed--

## --seed-contents--

```js
let hello = "   Hello, World!  ";
let wsRegex = /change/; // Change this line
let result = hello; // Change this line
```

# --solutions--

```js
let hello = "   Hello, World!  ";
let wsRegex = /^(\s+)(.+[^\s])(\s+)$/;
let result = hello.replace(wsRegex, '$2');
```
