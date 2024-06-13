---
id: 5900f4fc1000cf542c51000e
title: 'Завдання 399: безквадратні числа Фібоначчі'
challengeType: 1
forumTopicId: 302064
dashedName: problem-399-squarefree-fibonacci-numbers
---

# --description--

Першими 15-тьма числами Фібоначчі є:

$$1,1,2,3,5,8,13,21,34,55,89,144,233,377,610.$$

Можна помітити, що 8 та 144 не є безквадратними: 8 ділиться на 4, а 144 ділиться на 4 і 9.

Тому першими 13-тьма безквадратними числами Фібоначчі є:

$$1,1,2,3,5,13,21,34,55,89,233,377 \text{ та } 610.$$

$200$-им безквадратним числом Фібоначчі є 971183874599339129547649988289594072811608739584170445. Останніми шістнадцятьма цифрами цього числа є 1608739584170445, а в експоненційному записі це число можна записати як `9.7e53`.

Знайдіть $100\\,000\\,000$-не безквадратне число Фібоначчі. Надайте відповідь у вигляді рядка з останніх шістнадцяти цифр, після яких йде кома та число в експоненційному записі (округліть до однієї цифри після коми). Для $200$-ого безквадратного числа відповіддю буде `1608739584170445,9.7e53`

**Примітка:** для цього завдання припускайте, що перше число Фібоначчі, яке ділиться на просте число $p$, не ділиться на $p^2$ (згідно з гіпотезою Волла). Це доведено для простих чисел $≤ 3 \times {10}^{15}$, але не доведено загалом.

Якщо гіпотеза виявиться хибною, то прийнятною відповіддю до цього завдання необов’язково буде $100\\,000\\,000$-не безквадратне число Фібоначчі, а лише межа цього числа.

# --hints--

`squarefreeFibonacciNumbers()` має повернути рядок.

```js
assert(typeof squarefreeFibonacciNumbers() === 'string');
```

`squarefreeFibonacciNumbers()` має повернути рядок `1508395636674243,6.5e27330467`.

```js
assert.strictEqual(squarefreeFibonacciNumbers(), '1508395636674243,6.5e27330467');
```

# --seed--

## --seed-contents--

```js
function squarefreeFibonacciNumbers() {

  return true;
}

squarefreeFibonacciNumbers();
```

# --solutions--

```js
// solution required
```