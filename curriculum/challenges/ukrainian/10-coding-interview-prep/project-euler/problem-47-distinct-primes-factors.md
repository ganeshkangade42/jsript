---
id: 5900f39c1000cf542c50feae
title: 'Завдання 47: різні прості множники'
challengeType: 5
forumTopicId: 302145
dashedName: problem-47-distinct-primes-factors
---

# --description--

Першими двома послідовними числами, які мають два різні прості множники, є:

<div style='padding-left: 4em;'>
  14 = 2 × 7<br>
  15 = 3 × 5
</div>

Першими трьома послідовними числами, які мають три різні прості множники, є:

<div style='padding-left: 4em;'>
  644 = 2<sup>2</sup> × 7 × 23<br>
  645 = 3 × 5 × 43<br>
  646 = 2 × 17 × 19
</div>

Знайдіть перші чотири послідовні цілі числа, які мають чотири різні прості множники. Яким є перше з цих чисел?

# --hints--

`distinctPrimeFactors(2, 2)` має повернути число.

```js
assert(typeof distinctPrimeFactors(2, 2) === 'number');
```

`distinctPrimeFactors(2, 2)` має повернути число 14.

```js
assert.strictEqual(distinctPrimeFactors(2, 2), 14);
```

`distinctPrimeFactors(3, 3)` має повернути число 644.

```js
assert.strictEqual(distinctPrimeFactors(3, 3), 644);
```

`distinctPrimeFactors(4, 4)` має повернути число 134043.

```js
assert.strictEqual(distinctPrimeFactors(4, 4), 134043);
```

# --seed--

## --seed-contents--

```js
function distinctPrimeFactors(targetNumPrimes, targetConsecutive) {

  return true;
}

distinctPrimeFactors(4, 4);
```

# --solutions--

```js
function distinctPrimeFactors(targetNumPrimes, targetConsecutive) {
  function numberOfPrimeFactors(n) {
    let factors = 0;

    //  Considering 2 as a special case
    let firstFactor = true;
    while (n % 2 == 0) {
      n = n / 2;
      if (firstFactor) {
        factors++;
        firstFactor = false;
      }
    }
    // Adding other factors
    for (let i = 3; i < Math.sqrt(n); i += 2) {
      firstFactor = true;
      while (n % i == 0) {
        n = n / i;
        if (firstFactor) {
          factors++;
          firstFactor = false;
        }
      }
    }

    if (n > 1) { factors++; }

    return factors;
  }

  let number = 0;
  let consecutive = 0;

  while (consecutive < targetConsecutive) {
    number++;
    if (numberOfPrimeFactors(number) >= targetNumPrimes) {
      consecutive++;
    } else {
      consecutive = 0;
    }
  }
  return number - targetConsecutive + 1;
}
```
