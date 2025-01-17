---
id: 587d7b84367417b2b2512b35
title: Неправильно написані назви змінних та функцій
challengeType: 1
forumTopicId: 301186
dashedName: catch-misspelled-variable-and-function-names
---

# --description--

The `console.log()` and `typeof` methods are the two primary ways to check intermediate values and types of program output. Now it's time to get into the common forms that bugs take. One syntax-level issue that fast typers can commiserate with is the humble spelling error.

Якщо символ у назві змінної чи функції буде перенесений, відсутній, або ж матиме неправильний регістр, браузер виконуватиме пошук неіснуючого об’єкта та надсилатиме скарги у формі посилання на помилку. Назви змінних та функцій у JavaScript чутливі до регістру.

# --instructions--

Виправте дві помилки правопису в коді, щоб розрахунок `netWorkingCapital` працював.

# --hints--

Перевірте правопис двох змінних, використаних у розрахунку netWorkingCapital, щоб вихідні дані консолі показували «Net working capital is: 2».

```js
assert(netWorkingCapital === 2);
```

У коді не повинно бути змінних з орфографічними помилками.

```js
assert(!__helpers.removeJSComments(code).match(/recievables/g));
```

Змінна `receivables` повинна бути правильно оголошеною та використаною.

```js
assert(__helpers.removeJSComments(code).match(/receivables/g).length == 2);
```

У коді не повинно бути змінних з орфографічними помилками.

```js
assert(!__helpers.removeJSComments(code).match(/payable;/g));
```

Змінна `payables` повинна бути правильно оголошеною та використаною.

```js
assert(__helpers.removeJSComments(code).match(/payables/g).length == 2);
```

# --seed--

## --seed-contents--

```js
let receivables = 10;
let payables = 8;
let netWorkingCapital = recievables - payable;
console.log(`Net working capital is: ${netWorkingCapital}`);
```

# --solutions--

```js
let receivables = 10;
let payables = 8;
let netWorkingCapital = receivables - payables;
console.log(`Net working capital is: ${netWorkingCapital}`);
```
