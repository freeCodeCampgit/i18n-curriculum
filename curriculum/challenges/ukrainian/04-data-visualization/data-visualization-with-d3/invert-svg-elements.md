---
id: 587d7fa9367417b2b2512bd0
title: Переверніть елементи SVG
challengeType: 6
forumTopicId: 301488
dashedName: invert-svg-elements
---

# --description--

You may have noticed the bar chart looked like it's upside-down, or inverted. This is because of how SVG uses (x, y) coordinates.

Початком координат у SVG виступає точка, розташована у верхньому лівому куті. Вісь координат `x` зі значенням 0 розміщує фігуру в лівій частині площини SVG. Вісь координат `y` зі значенням 0 розміщує фігуру у верхній частині площини SVG. Більше значення `x` зміщує прямокутник праворуч. Більше значення `y` зміщує прямокутник вниз.

Щоб розмістити стовпчик лицьовим боком наверх, необхідно змінити обчислення координати `y`. Потрібно враховувати як висоту стовпчика, так і загальну висоту площини SVG.

Висота площини SVG дорівнює 100. Якщо в наборі є точка даних 0, стовпчик має починатись знизу площини SVG (не зверху). Для цього значенням координати `y` має бути 100. Якби значенням точки даних було 1, ми б почали з координати `y` зі значенням 100, щоб встановити стовпчик знизу. Потім потрібно врахувати висоту стовпчика 1, тому кінцевою координатою `y` буде 99.

Координата `y`, знайдена за допомогою `y = heightOfSVG - heightOfBar`, розміщує стовпчики лицьовим боком наверх.

# --instructions--

Змініть функцію зворотного виклику для атрибута `y`, щоб вона встановила стовпчики лицьовим боком наверх. Пам’ятайте, що значення `height` стовпчика у 3 рази більше за значення даних `d`.

**Примітка:** зазвичай відношенням є `y = h - m * d`, де `m` — це константа, яка масштабує точки даних.

# --hints--

Перший `rect` повинен мати `y` зі значенням `64`.

```js
assert($('rect').eq(0).attr('y') == h - dataset[0] * 3);
```

Другий `rect` повинен мати `y` зі значенням `7`.

```js
assert($('rect').eq(1).attr('y') == h - dataset[1] * 3);
```

Третій `rect` повинен мати `y` зі значенням `34`.

```js
assert($('rect').eq(2).attr('y') == h - dataset[2] * 3);
```

Четвертий `rect` повинен мати `y` зі значенням `49`.

```js
assert($('rect').eq(3).attr('y') == h - dataset[3] * 3);
```

П’ятий `rect` повинен мати `y` зі значенням `25`.

```js
assert($('rect').eq(4).attr('y') == h - dataset[4] * 3);
```

Шостий `rect` повинен мати `y` зі значенням `46`.

```js
assert($('rect').eq(5).attr('y') == h - dataset[5] * 3);
```

Сьомий `rect` повинен мати `y` зі значенням `13`.

```js
assert($('rect').eq(6).attr('y') == h - dataset[6] * 3);
```

Восьмий `rect` повинен мати `y` зі значенням `58`.

```js
assert($('rect').eq(7).attr('y') == h - dataset[7] * 3);
```

Дев’ятий `rect` повинен мати `y` зі значенням `73`.

```js
assert($('rect').eq(8).attr('y') == h - dataset[8] * 3);
```

# --seed--

## --seed-contents--

```html
<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

    const w = 500;
    const h = 100;

    const svg = d3.select("body")
                  .append("svg")
                  .attr("width", w)
                  .attr("height", h);

    svg.selectAll("rect")
       .data(dataset)
       .enter()
       .append("rect")
       .attr("x", (d, i) => i * 30)
       .attr("y", (d, i) => {
         // Add your code below this line



         // Add your code above this line
       })
       .attr("width", 25)
       .attr("height", (d, i) => 3 * d);
  </script>
</body>
```

# --solutions--

```html
<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

    const w = 500;
    const h = 100;

    const svg = d3.select("body")
                  .append("svg")
                  .attr("width", w)
                  .attr("height", h);

    svg.selectAll("rect")
       .data(dataset)
       .enter()
       .append("rect")
       .attr("x", (d, i) => i * 30)
       .attr("y", (d, i) => h - 3 * d)
       .attr("width", 25)
       .attr("height", (d, i) => 3 * d);
  </script>
</body>
```
