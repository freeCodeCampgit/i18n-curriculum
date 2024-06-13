---
id: 5900f4b91000cf542c50ffcc
title: 'Завдання 333: особливе розкладання'
challengeType: 1
forumTopicId: 301991
dashedName: problem-333-special-partitions
---

# --description--

Всі натуральні числа можна розкласти таким чином, що кожен член можна представити у вигляді $2^i \times 3^j$, де $i, j ≥ 0$.

Розглянемо лише ті випадки, де жоден з членів не ділиться на будь-який інший член. Наприклад, розкладання $17 = 2 + 6 + 9 = (2^1 \times 3^0 + 2^1 \times 3^1 + 2^0 \times 3^2)$ не підходить, оскільки 6 ділиться на 2. Розкладання $17 = 16 + 1 = (2^4 \times 3^0 + 2^0 \times 3^0)$ також не підходить, оскільки 16 ділиться на 1. Єдиним дійсним розкладанням 17 буде $8 + 9 = (2^3 \times 3^0 + 2^0 \times 3^2)$.

Для багатьох цілих чисел існує декілька варіантів дійсного розкладання, починаючи з 11, для якого можливі два розкладання.

$$\begin{align}   & 11 = 2 + 9 = (2^1 \times 3^0 + 2^0 \times 3^2) \\\\
  & 11 = 8 + 3 = (2^3 \times 3^0 + 2^0 \times 3^1) \end{align}$$

Визначимо $P(n)$ як кількість дійсних розкладань числа $n$. Наприклад, $P(11) = 2$.

Розглянемо лише прості числа $q$, для яких можливе лише одне дійсне розкладання. Наприклад, $P(17)$.

Сума простих чисел $q &lt;100$, за яких $P(q) = 1$, дорівнює 233.

Знайдіть суму простих чисел $q &lt; 1\\,000\\,000$, за яких $P(q) = 1$.

# --hints--

`specialPartitions()` має повернути `3053105`.

```js
assert.strictEqual(specialPartitions(), 3053105);
```

# --seed--

## --seed-contents--

```js
function specialPartitions() {

  return true;
}

specialPartitions();
```

# --solutions--

```js
// solution required
```