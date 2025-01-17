---
id: 587d7b88367417b2b2512b47
title: Використання залишкового параметра із параметрами функції
challengeType: 1
forumTopicId: 301221
dashedName: use-the-rest-parameter-with-function-parameters
---

# --description--

In order to help us create more flexible functions, ES6 introduces the <dfn>rest parameter</dfn> for function parameters. With the rest parameter, you can create functions that take a variable number of arguments. These arguments are stored in an array that can be accessed later from inside the function.

Погляньте на цей код:

```js
function howMany(...args) {
  return "You have passed " + args.length + " arguments.";
}
console.log(howMany(0, 1, 2));
console.log(howMany("string", null, [1, 2, 3], { }));
```

Консоль показуватиме рядки `You have passed 3 arguments.` та `You have passed 4 arguments.`.

Залишковий параметр усуває потребу використовувати об’єкт `arguments` та дозволяє нам використовувати методи масиву на масиві параметрів, переданих до функції `howMany`.

# --instructions--

Змініть функцію `sum`, використавши залишковий параметр, щоб функція `sum` могла прийняти будь-яку кількість аргументів і повернути їхню суму.

# --hints--

Результатом `sum(0,1,2)` має бути 3

```js
assert(sum(0, 1, 2) === 3);
```

Результатом `sum(1,2,3,4)` має бути 10

```js
assert(sum(1, 2, 3, 4) === 10);
```

Результатом `sum(5)` має бути 5

```js
assert(sum(5) === 5);
```

Результатом `sum()` має бути 0

```js
assert(sum() === 0);
```

`sum` повинна бути стрілковою функцією, яка використовує синтаксис залишкового параметра (`...`) на параметрі `args`.

```js
assert(__helpers.removeWhiteSpace(__helpers.removeJSComments(code)).match(/sum=\(\.\.\.args\)=>/));
```

# --seed--

## --seed-contents--

```js
const sum = (x, y, z) => {
  const args = [x, y, z];
  let total = 0;
  for (let i = 0; i < args.length; i++) {
    total += args[i];
  }
  return total;
}
```

# --solutions--

```js
const sum = (...args) => {
  let total = 0;
  for (let i = 0; i < args.length; i++) {
    total += args[i];
  }
  return total;
}
```
