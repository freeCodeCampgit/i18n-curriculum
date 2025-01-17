---
id: 587d7b87367417b2b2512b42
title: Мутація масиву, оголошеного з const
challengeType: 1
forumTopicId: 301206
dashedName: mutate-an-array-declared-with-const
---

# --description--

If you are unfamiliar with `const`, check out <a href="/learn/javascript-algorithms-and-data-structures/basic-javascript/declare-a-read-only-variable-with-the-const-keyword" target="_blank" rel="noopener noreferrer nofollow">this challenge about the <code>const</code> keyword</a>.

У сучасному JavaScript існує багато випадків оголошень з `const`.

Деякі розробники надають перевагу присвоєнню усіх змінних за допомогою `const`, якщо їм не потрібно повторно присвоїти значення. Тоді вони використовують `let`.

Однак варто розуміти, що об’єкти (включно з масивами та функціями), присвоєні змінній за допомогою `const`, всеодно можна змінити. Оголошення `const` всього лиш запобігає повторному присвоєнню ідентифікатора змінної.

```js
const s = [5, 6, 7];
s = [1, 2, 3];
s[2] = 45;
console.log(s);
```

`s = [1, 2, 3]` призведе до помилки. Після коментування цього рядка, `console.log` показуватиме значення `[5, 6, 45]`.

Як ви помітили, об’єкт `[5, 6, 7]` можна змінювати, але змінна `s` всеодно вказуватиме на змінений масив `[5, 6, 45]`. Як і усі масиви, елементи масиву в `s` є змінними, але оскільки було використано `const`, ви не можете використати ідентифікатор змінної `s`, щоб вказати на інший масив за допомогою оператора присвоєння.

# --instructions--

Масив оголошений як `const s = [5, 7, 2]`. Змініть масив на `[2, 5, 7]`, використовуючи різні присвоєння елементів.

# --hints--

Ви не повинні замінювати ключове слово `const`.

```js
assert(__helpers.removeJSComments(code).match(/const/g));
```

`s` повинна бути константною змінною (використовуйте `const`).

```js
assert(__helpers.removeJSComments(code).match(/const\s+s/g));
```

Ви не повинні змінювати оголошення масиву.

```js
assert(__helpers.removeJSComments(code).match(
/const\s+s\s*=\s*\[\s*5\s*,\s*7\s*,\s*2\s*\]\s*;?/g
));
```

`s` повинна дорівнювати `[2, 5, 7]`.

```js
assert.deepEqual(s, [2, 5, 7]);
```

# --seed--

## --seed-contents--

```js
const s = [5, 7, 2];
function editInPlace() {
  // Only change code below this line

  // Using s = [2, 5, 7] would be invalid

  // Only change code above this line
}
editInPlace();
```

# --solutions--

```js
const s = [5, 7, 2];
function editInPlace() {
  s[0] = 2;
  s[1] = 5;
  s[2] = 7;
}
editInPlace();
```
