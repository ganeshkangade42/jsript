---
id: 5900f3db1000cf542c50feec
title: 'Завдання 109: Дартс'
challengeType: 5
forumTopicId: 301733
dashedName: problem-109-darts
---

# --description--

У грі дартс гравець кидає три дротики у мішень, розділену на двадцять рівних секторів, пронумерованих від одного до двадцяти.

<img class="img-responsive center-block" alt="Мішень для дартс" src="https://cdn.freecodecamp.org/curriculum/project-euler/darts.png" style="background-color: white; padding: 10px;" />

Кількість очків визначається номером сектору, у який потрапив дротик. Влучення дротика за межами червоного/зеленого зовнішнього кільця очок не приносить. Кожному чорному та білому сектору всередині цього кільця привласнене окреме число. Червоне/зелене зовнішнє та середнє кільця подвоюють чи потроюють числа сектора відповідно.

У центрі дошки – два кола, їх називають "яблучко" або "бичаче око". Влучання у центральне зелене кільце приносить 25 очок, а у червоне – 50 очок.

Існує чимало різновидів гри, зокрема, у найпопулярнішій з них гравці починають з рахунку 301 (варіант 501). Перемагає гравець, який перший зменшить рахунок до нуля. Також можна грати в "подвоєну" систему: гравець повинен потрапити у зону подвоєння (включно з бичачим оком у центрі мішені) під час останнього метання; попадання в інший сектор, що привів рахунок до перебору або одиниці, означає, що очки серії не зараховуються.

"Чекаут" – коли гравець може завершити гру при поточному рахунку; найвищий чекаут – 170: T20 T25 D25 (два попадання у потрійне 20 та в яблучко). Існує одинадцять різних варіантів чекауту при рахунку 6:

$$\початок{array} \text{D3} &    &    \\\\ D1        & D2 &    \\\\ S2        & D2 &    \\\\ D2        & D1 &    \\\\ S4        & D1 &    \\\\ S1        & S1 & D2 \\\\ S1        & T1 & D1 \\\\ S1        & S3 & D1 \\\\ D1        & D1 & D1 \\\\ D1        & S2 & D1 \\\\ S2        & S2 & D1 \кінець{array}$$

Зверніть увагу, що D1 D2 відрізняється від D2 D1, оскільки вони закінчуються різними подвоєннями. Однак, комбінація S1 T1 D1 вважається такою ж, як і T1 S1 D1. До того ж, не потрібно вказувати промахи у комбінаціях; наприклад, D3 це те саме, що й 0 D3 і 0 0 D3. Неймовірно, що загалом існує 42336 різних способів чекауту. Скільки різних способів чекауту має гравець з балом меншим за 100?

# --hints--

`darts()` повинен повертатися як `38182`.

```js
assert.strictEqual(darts(), 38182);
```

# --seed--

## --seed-contents--

```js
function darts() {

  return true;
}

darts();
```

# --solutions--

```js
// solution required
```
