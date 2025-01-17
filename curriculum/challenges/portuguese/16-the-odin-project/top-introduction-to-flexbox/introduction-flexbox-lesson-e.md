---
id: 6571b300cc1de61d7b4dd383
title: Lição E de Introdução ao Flexbox
challengeType: 15
dashedName: introduction-flexbox-lesson-e
---

# --description--

A declaração `flex` é na verdade uma abreviação para 3 propriedades que você pode definir em um item flex. Essas propriedades afetam como os itens flex dimensionam a si mesmos dentro de seu contêiner. Você já viu algumas propriedades abreviadas antes, mas ainda não as definiu oficialmente.

> Propriedades abreviadas são propriedades do CSS que permitem definir os valores de múltiplas outras propriedades do CSS simultaneamente. Usando uma propriedade abreviada, você pode escrever folhas de estilo mais concisas (e muitas vezes mais legíveis), economizando tempo e energia.

Neste caso, `flex` é, na verdade, uma abreviação para `flex-grow`, `flex-shrink` e `flex-basis`.

<img src="https://cdn.freecodecamp.org/curriculum/odin-project/flex-box/flexbox-04.png" alt="Código em CSS definindo a propriedade flex para 1 em um elemento div." />

Na captura de tela acima, `flex: 1` equivale a: `flex-grow: 1`, `flex-shrink: 1`, `flex-basis: 0`.

Muito frequentemente, você vê a abreviação de flex definida com apenas um valor. Nesse caso, esse valor é aplicado a `flex-grow`. Então, quando você colocou `flex: 1` nas divs, você estava, na verdade, especificando uma abreviação de `flex: 1 1 0`.

# --questions--

## --text--

Quais propriedades são definidas pela abreviação `flex`?

## --answers--

`flex-grow`, `flex-shrink` e `flex`

---

`flex-basis`, `flex-wrap` e `flex-direction`

---

`flex-grow`, `flex-shrink` e `flex-basis`

---

`flex-direction`, `flex` e `flex-wrap`

## --video-solution--

3
