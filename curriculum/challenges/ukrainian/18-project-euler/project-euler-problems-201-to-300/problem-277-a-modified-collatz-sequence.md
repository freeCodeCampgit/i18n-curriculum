---
id: 5900f4811000cf542c50ff94
title: 'Завдання 277: модифікована послідовність Коллатца'
challengeType: 1
forumTopicId: 301927
dashedName: problem-277-a-modified-collatz-sequence
---

# --description--

Модифіковану послідовність Коллатца з цілих чисел отримують від початкового значення $a_1$ таким чином:

$a_{n + 1} = \frac{a_n}{3}$, якщо $a_n$ ділиться на 3 без остачі. Позначимо це великим кроком вниз, «D».

$a_{n + 1} = \frac{4a_n + 2}{3}$, якщо $a_n$ при діленні на 3 дає залишок 1. Позначимо це великим кроком вверх, «U».

$a_{n + 1} = \frac{2a_n - 1}{3}$, якщо $a_n$ при діленні на 3 дає залишок 2. Позначимо це малим кроком вниз, «d».

Послідовність припиняється, коли деякі $a_n = 1$.

Для будь-якого цілого числа можна сформувати послідовність кроків. Наприклад, якщо $a_1 = 231$, то послідовність $\\{a_n\\} = \\{231, 77, 51, 17, 11, 7, 10, 14, 9, 3, 1\\}$ відповідає крокам «DdDddUUdDD».

Звичайно, існують й інші послідовності, які починаються з тієї ж послідовності «DdDddUUdDD....».

Наприклад, якщо $a_1 = 1004064$, то послідовністю буде DdDddUUdDDDdUDUUUdDdUUDDDUdDD.

Фактично, 1004064 є найменшим можливим значенням $a_1 > {10}^6$, що починається з послідовності DdDddUUdDD.

Яким є найменше значення $a_1 > {10}^{15}$, що починається з послідовності «UDDDUdddDDUDDddDdDddDDUDDdUUDd»?

# --hints--

`modifiedCollatzSequence()` має повернути `1125977393124310`.

```js
assert.strictEqual(modifiedCollatzSequence(), 1125977393124310);
```

# --seed--

## --seed-contents--

```js
function modifiedCollatzSequence() {

  return true;
}

modifiedCollatzSequence();
```

# --solutions--

```js
// solution required
```