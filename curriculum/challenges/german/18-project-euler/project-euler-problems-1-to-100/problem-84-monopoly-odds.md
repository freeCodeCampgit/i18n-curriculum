---
id: 5900f3c11000cf542c50fed3
title: 'Problem 84: Monopoly-Gewinnchancen'
challengeType: 1
forumTopicId: 302198
dashedName: problem-84-monopoly-odds
---

# --description--

Im Spiel *Monopoly* ist das Standardspielbrett folgendermaßen aufgebaut:

<div style="text-align: center;">
  <table cellspacing="1" cellpadding="5" border="0" style="background-color: black; color: black;" align="center">
    <tbody>
      <tr>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">GO</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">A1</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">CC1</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">A2</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">T1</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">R1</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">B1</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">CH1</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">B2</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">B3</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">GEFÄNGNIS</td>
      </tr>
      <tr>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">H2</td>
        <td colspan="9">&nbsp;</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">C1</td>
      </tr>
      <tr>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">T2</td>
        <td colspan="9">&nbsp;</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">U1</td>
      </tr>
      <tr>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">H1</td>
        <td colspan="9">&nbsp;</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">C2</td>
      </tr>
      <tr>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">CH3</td>
        <td colspan="9">&nbsp;</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">C3</td>
      </tr>
      <tr>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">R4</td>
        <td colspan="9">&nbsp;</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">R2</td>
      </tr>
      <tr>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">G3</td>
        <td colspan="9">&nbsp;</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">D1</td>
      </tr>
      <tr>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">CC3</td>
        <td colspan="9">&nbsp;</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">CC2</td>
      </tr>
      <tr>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">G2</td>
        <td colspan="9">&nbsp;</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">D2</td>
      </tr>
      <tr>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">G1</td>
        <td colspan="9">&nbsp;</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">D3</td>
      </tr>
      <tr>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">G2J</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">F3</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">U2</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">F2</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">F1</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">R3</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">E3</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">E2</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">CH2</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">E1</td>
        <td style="background-color: #ffffff; color: black; padding: 5px; border: 1px solid black;">FP</td>
      </tr>
    </tbody>
  </table>
</div><br>

Ein Spieler beginnt auf dem Feld LOS und addiert die Punkte auf zwei 6-seitigen Würfeln, um die Anzahl der Felder zu bestimmen, um die er im Uhrzeigersinn vorrückt. Ohne weitere Regeln würden wir erwarten, dass jedes Feld mit der gleichen Wahrscheinlichkeit besucht wird: 2,5 %. Die Landung auf G2J (Go to Jail - Gehe ins Gefängnis), CC (Community Chest - Gemeinschaftskasse) und CH (Chance) ändert diese Verteilung jedoch.

Zusätzlich zu G2J und je einer Karte aus CC und CH, die den Spieler direkt ins Gefängnis bringt, wird das Ergebnis des dritten Wurfs nicht vorverlegt, wenn ein Spieler drei aufeinanderfolgende Paschs würfelt. Stattdessen kommen sie direkt ins Gefängnis.

Zu Beginn des Spiels werden die CC- und CH-Karten gemischt. Wenn ein Spieler auf CC oder CH landet, nimmt er eine Karte von der Oberseite des jeweiligen Stapels und legt sie, nachdem er die Anweisungen befolgt hat, wieder auf den Boden des Stapels zurück. Es gibt sechzehn Karten in jedem Stapel, aber zum Zweck dieses Problems befassen wir uns nur mit Karten, die eine Bewegung anordnen; jede Anweisung, die sich nicht auf eine Bewegung bezieht, wird ignoriert und der Spieler bleibt auf dem CC/CH-Feld.

<ul>
  <li>Community-Truhe (2/16 Karten):</li>
  <ol>
    <li>Vorrücken zu LOS</li>
    <li>Gehe ins GEFÄNGNIS</li>
  </ol>

  <li>Ereigniskarten (10/16 Karten):</li>
  <ol>
    <li>Vorrücken zu LOS</li>
    <li>Gehe ins GEFÄNGNIS</li>
    <li>Gehe zu C1</li>
    <li>Gehe zu E3</li>
    <li>Gehe zu H2</li>
    <li>Gehe zu R1</li>
    <li>Gehe zum nächsten R (Eisenbahngesellschaft)</li>
    <li>Gehe zum nächsten R</li>
    <li>Gehe zur nächsten U (Versorgungsunternehmen)</li>
    <li>Gehe 3 Felder zurück.</li>
  </ol>
</ul>

Der Kern dieses Problems betrifft die Wahrscheinlichkeit, einen bestimmten Platz zu besuchen. Das heißt, die Wahrscheinlichkeit, nach einem Wurf auf diesem Feld zu landen. Aus diesem Grund sollte klar sein, dass mit Ausnahme von G2J, bei dem die Wahrscheinlichkeit auf diesem Feld zu enden gleich Null ist, die CH-Felder die niedrigsten Wahrscheinlichkeiten haben, da 5/8 eine Bewegung auf ein anderes Feld verlangen, und es ist das letzte Feld, auf dem der Spieler bei jedem Wurf endet, das uns interessiert. Wir machen keinen Unterschied zwischen "Nur zu Besuch" und "Ins Gefängnis", und wir ignorieren auch die Regel, dass man ein Pasch braucht, um "aus dem Gefängnis zu kommen", wenn man davon ausgeht, dass er in seinem nächsten Zug für die Entlassung bezahlt.

Indem wir bei LOS beginnen und die Quadrate fortlaufend von 00 bis 39 nummerieren, können wir diese zweistelligen Zahlen verketten, um Strings zu erzeugen, die mit Gruppen von Quadraten übereinstimmen.

Statistisch lässt sich zeigen, dass die drei beliebtesten Quadrate in dieser Reihenfolge GEFÄNGNIS (6,24 %) = Quadrat 10, E3 (3,18 %) = Quadrat 24 und LOS (3,09 %) = Quadrat 00 sind. Diese drei beliebtesten Quadrate können also mit dem sechsstelligen modalen String `102400` aufgeführt werden.

Wenn anstelle von zwei 6-seitigen Würfeln zwei `n`-seitige Würfel verwendet werden, findest du den sechsstelligen Modal-String.

# --hints--

`monopolyOdds(8)` sollte einen String zurückgeben.

```js
assert(typeof monopolyOdds(8) === 'string');
```

`monopolyOdds(8)` sollte einen String `102400` zurückgeben.

```js
assert.strictEqual(monopolyOdds(8), '102400');
```

`monopolyOdds(10)` sollte einen String `100024` zurückgeben.

```js
assert.strictEqual(monopolyOdds(10), '100024');
```

`monopolyOdds(20)` sollte einen String `100005` zurückgeben.

```js
assert.strictEqual(monopolyOdds(20), '100005');
```

`monopolyOdds(4)` sollte einen String `101524` zurückgeben.

```js
assert.strictEqual(monopolyOdds(4), '101524');
```

# --seed--

## --seed-contents--

```js
function monopolyOdds(n) {

  return true;
}

monopolyOdds(8);
```

# --solutions--

```js
const GO = 0;
const JAIL = 10;
const GO_TO_JAIL = 30;

const C1 = 11;
const E3 = 24;
const H2 = 39;

const R1 = 5;
const R2 = 15;
const R3 = 25;

const U1 = 12;
const U2 = 28;

const SPECIAL_CARDS = 16;
const GAME_SQUARES = 40;

const CC1 = 2;
const CC2 = 17;
const CC3 = 33;
const CHESTS = [CC1, CC2, CC3];
const chestCardsMoves = [GO, JAIL];

const CH1 = 7;
const CH2 = 22;
const CH3 = 36;
const CHANCES = [CH1, CH2, CH3];
const chanceCardsMoves = [GO, JAIL, C1, E3, H2, R1];
const chanceToRailroad = { [CH1]: R2, [CH2]: R3, [CH3]: R1 };
const chanceToUtility = { [CH1]: U1, [CH2]: U2, [CH3]: U1 };

function multiplyMatrix(matrix1, matrix2) {
  const multiplied = [];

  for (let row = 0; row < matrix1.length; row++) {
    const newRow = [];
    for (let col = 0; col < matrix1[row].length; col++) {
      let newCell = 0;
      for (let i = 0; i < matrix1[row].length; i++) {
        const value1 = matrix1[row][i];
        const value2 = matrix2[i][col];
        newCell += value1 * value2;
      }
      newRow.push(newCell);
    }
    multiplied.push(newRow);
  }
  return multiplied;
}

function normalizeRow(row) {
  const sum = row.reduce((total, value) => total + value, 0);
  if (sum > 0) {
    for (let j = 0; j < row.length; j++) {
      const value = row[j];
      row[j] = value / sum;
    }
  }
}

function sortByProbability(board) {
  return board
    .map((probability, squareNo) => [squareNo, probability])
    .sort((a, b) => a[1] - b[1])
}

function getTopThree(board) {
  return sortByProbability(board)
    .slice(-3)
    .reverse()
    .map(([squareNo, _]) => squareNo.toString().padStart(2, '0')
    )
    .join('');
}

function didConverge(matrix1, matrix2, precision) {
  return matrix1.every((row, rowNo) => row.every((value1, colNo) => Math.abs(value1 - matrix2[rowNo][colNo]) <= precision))
}

function monopolyOdds(diceSides) {
  // Based on https://github.com/ByteThisCoding/project-euler/blob/master/problems/0084/0084.ts

  const timesRolled = new Array(diceSides * 2 + 1).fill(0);
  for (let dice1 = 1; dice1 <= diceSides; dice1++) {
    for (let dice2 = 1; dice2 <= diceSides; dice2++) {
      timesRolled[dice1 + dice2]++;
    }
  }

  // Transitions matrix contain probabilities of reaching each square (row values)
  // from each starting square (row no.).
  let transitions = [];
  for (let startSquare = 0; startSquare < GAME_SQUARES; startSquare++) {
    const row = new Array(GAME_SQUARES).fill(0);
    for (let rollResult = 2; rollResult <= diceSides * 2; rollResult++) {
      const rollChance = timesRolled[rollResult]
      const position = (startSquare + rollResult) % GAME_SQUARES;

      if (CHANCES.includes(position)) {
        // Chance cards ordering movement.
        for (let i = 0; i < chanceCardsMoves.length; i++) {
          const nextSquare = chanceCardsMoves[i];
          row[nextSquare] += rollChance / SPECIAL_CARDS;
        }
        row[chanceToRailroad[position]] += 2 * rollChance / SPECIAL_CARDS;
        row[chanceToUtility[position]] += rollChance / SPECIAL_CARDS;
        row[position - 3] += rollChance / SPECIAL_CARDS;

        // Rest non-moving Chance cards.
        row[position] += (SPECIAL_CARDS - chanceCardsMoves.length) * rollChance / SPECIAL_CARDS;
      } else if (CHESTS.includes(position)) {
        // Community Chest cards ordering movement.
        for (let i = 0; i < chestCardsMoves.length; i++) {
          const nextSquare = chestCardsMoves[i];
          row[nextSquare] += rollChance / SPECIAL_CARDS;
        }
        // Rest non-moving Community Chest cards.
        row[position] += (SPECIAL_CARDS - chestCardsMoves.length) * rollChance / SPECIAL_CARDS
      } else if (position === GO_TO_JAIL) {
        row[JAIL] += rollChance;
      } else {
        row[position] += rollChance;
      }
    }
    normalizeRow(row)
    transitions.push(row);
  }

  const precision = 0.000001;
  for (let i = 0; i < GAME_SQUARES; i++) {
    const next = multiplyMatrix(transitions, transitions);
    if (didConverge(transitions, next, precision)) {
      break;
    }
    transitions = next;
  }

  // All rows converge to the same values.
  return getTopThree(transitions[0]);
}
```
