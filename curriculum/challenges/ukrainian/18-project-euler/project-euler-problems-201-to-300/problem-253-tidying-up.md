---
id: 5900f4691000cf542c50ff7c
title: 'Завдання 253: прибирання'
challengeType: 1
forumTopicId: 301901
dashedName: problem-253-tidying-up
---

# --description--

Дитина має «числову гусеницю», що складається з сорока пронумерованих кусочків, які при з’єднанні утворюють числовий ряд від 1 до 40.

Кожного вечора тато повинен зібрати розкидані по всій ігровій кімнаті кусочки гусениці. Він навмання підіймає кусочки та складає їх у правильному порядку.

В процесі такого збирання гусениці спочатку формуються окремі відрізки, які поступово об’єднуються. Кількість відрізків починається з нуля (жодного кусочка), загалом збільшується до 11 або 12, потім знову зменшується поки не завершиться одним відрізком (усі кусочки зібрано).

Наприклад:

| Підібраний кусочок | Поточна кількість відрізків |
| ------------------ | --------------------------- |
| 12                 | 1                           |
| 4                  | 2                           |
| 29                 | 3                           |
| 6                  | 4                           |
| 34                 | 5                           |
| 5                  | 4                           |
| 35                 | 4                           |
| …                  | …                           |

Нехай $M$ буде максимальною кількістю відрізків, отриманих під час прибирання. Кількість варіантів для кожного значення $M$ для гусениці з 10 кусочків становить

| M | Варіанти |
| - | -------- |
| 1 | 512      |
| 2 | 250912   |
| 3 | 1815264  |
| 4 | 1418112  |
| 5 | 144000   |

Отже, найімовірнішим значенням $M$ є 3, а середнє значення $\frac{385\\,643}{113\\,400} = 3.400732$, заокруглене до шести знаків після коми.

Найімовірнішим значенням $M$ для гусениці з 40 кусочків є 11. Чому дорівнює середнє значення $M$? Дайте відповідь, заокруглену до шести знаків після коми.

# --hints--

`tidyingUp()` має повернути `11.492847`.

```js
assert.strictEqual(tidyingUp(), 11.492847);
```

# --seed--

## --seed-contents--

```js
function tidyingUp() {

  return true;
}

tidyingUp();
```

# --solutions--

```js
// solution required
```