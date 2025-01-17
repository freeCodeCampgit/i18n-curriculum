---
id: 587d7b87367417b2b2512b41
title: Оголошення змінної для читання з ключовим словом const
challengeType: 1
forumTopicId: 301201
dashedName: declare-a-read-only-variable-with-the-const-keyword
---

# --description--

The keyword `let` is not the only new way to declare variables. In ES6, you can also declare variables using the `const` keyword.

`const` має ті ж круті функції, що й `let`, але з бонусом: тепер змінні, оголошені за допомогою `const`, доступні лише для читання. Вони мають константне значення, тобто після присвоєння змінної з `const`, її неможливо присвоїти знову:

```js
const FAV_PET = "Cats";
FAV_PET = "Dogs";
```

Консоль показуватиме помилку через повторне присвоєння значення `FAV_PET`.

Змінні, які не передбачають повторного присвоєння, потрібно називати, використовуючи ключове слово `const`. Це може знадобитися, якщо ви випадково спробуєте повторно присвоїти змінну, яка повинна залишатись константною.

**Примітка:** зазвичай розробники використовують ідентифікатори змінних у верхньому регістрі для незмінних значень та у нижньому регістрі чи верблюдячомуРегістрі для змінних значень (об’єктів чи масивів). Ви дізнаєтесь більше про об’єкти, масиви, а також змінні та незмінні значення в наступних завданнях. Також ви побачите приклади ідентифікаторів змінних у верхньому регістрі, нижньому регістрі та верблюдячомуРегістрі.

# --instructions--

Змініть код так, щоб усі змінні були оголошені за допомогою `let` або `const`. Використайте `let` для змінних значень, а `const` для незмінних значень. Крім того, перейменуйте змінні, оголошені за допомогою `const`, щоб відповідати загальним практикам. Не змінюйте рядки, які присвоєні змінним.

# --hints--

`var` повинне бути відсутнім у коді.

```js
assert.notMatch(code, /var/g);
```

Ви повинні змінити `fCC` на верхній регістр.

```js
assert.match(code, /(FCC)/);
assert.notMatch(code, /(fCC)/);
```

`FCC` повинна бути константною змінною, оголошеною з `const`.

```js
assert.match(code, /const\s+FCC/);
```

Не потрібно змінювати рядок, присвоєний до `FCC`.

```js
assert.equal(FCC, 'freeCodeCamp');
```

`fact` повинна бути оголошеною із `let`.

```js
assert.match(code, /(let\s+fact)/g);
```

`console.log` потрібно змінити так, щоб виводились змінні `FCC` та `fact`.

```js
assert.match(code, /console\.log\(\s*FCC\s*\,\s*fact\s*\)\s*;?/g);
```

# --seed--

## --seed-contents--

```js
var fCC = "freeCodeCamp"; // Change this line
var fact = "is cool!"; // Change this line
fact = "is awesome!";
console.log(fCC, fact); // Change this line
```

# --solutions--

```js
const FCC = "freeCodeCamp";
let fact = "is cool!";

fact = "is awesome!";
console.log(FCC, fact);
```
