---
id: 5900f4d51000cf542c50ffe8
title: 'Завдання 361: підпослідовність послідовності Морзе-Туе'
challengeType: 1
forumTopicId: 302022
dashedName: problem-361-subsequence-of-thue-morse-sequence
---

# --description--

Послідовність Морзе-Туе $\\{T_n\\}$ є бінарною послідовністю, яка задовільняє наступне:

- $T_0 = 0$
- $T_{2n} = T_n$
- $T_{2n + 1} = 1 - T_n$

Першими декількома членами послідовності $\\{T_n\\}$ є: $01101001\color{red}{10010}1101001011001101001\ldots$.

Визначимо $\\{A_n\\}$ як відсортовану послідовність цілих чисел, бінарний запис елементів якої з’являється як підпослідовність в $\\{T_n\\}$. Наприклад, десяткове число 18 записується як 10010 в бінарній системі. 10010 з’являється в $\\{T_n\\}$ (від $T_8$ до $T_{12}$), тому 18 є елементом $\\{A_n\\}$. Десяткове число 14 записується як 1110 в бінарній системі. 1110 ніколи не з’являється в $\\{T_n\\}$, тому 14 не є елементом $\\{A_n\\}$.

Першими декількома членами підпослідовності $A_n$ є:

$$\begin{array}{cr}   n   & 0 & 1 & 2 & 3 & 4 & 5 & 6 & 7 &  8 &  9 & 10 & 11 & 12 & \ldots \\\\
  A_n & 0 & 1 & 2 & 3 & 4 & 5 & 6 & 9 & 10 & 11 & 12 & 13 & 18 & \ldots \end{array}$$

Ми також можемо довести, що $A_{100} = 3251$ та $A_{1000} = 80\\,852\\,364\\,498$.

Знайдіть останні 9 цифр в $\displaystyle\sum_{k = 1}^{18} A_{{10}^k}$.

# --hints--

`subsequenceOfThueMorseSequence()` має повернути `178476944`.

```js
assert.strictEqual(subsequenceOfThueMorseSequence(), 178476944);
```

# --seed--

## --seed-contents--

```js
function subsequenceOfThueMorseSequence() {

  return true;
}

subsequenceOfThueMorseSequence();
```

# --solutions--

```js
// solution required
```