---
id: 587d8254367417b2b2512c6f
title: 对两组数据执行子集检查
challengeType: 1
forumTopicId: 301707
dashedName: perform-a-subset-check-on-two-sets-of-data
---

# --description--

In this exercise, we are going to perform a subset test on 2 sets of data. We will create a method on our `Set` data structure called `isSubsetOf`. This will compare the first set against the second, and if the first set is fully contained within the second, it will return `true`.

例如，如果 `setA = ['a','b']` 和 `setB = ['a','b','c','d']`，那么 `setA` 是 `setB` 的子集，所以 `setA.isSubsetOf(setB)` 应该返回 `true`。

# --hints--

你的 `Set` 类应该有一个 `isSubsetOf` 方法。

```js
assert(
  (function () {
    var test = new Set();
    return typeof test.isSubsetOf === 'function';
  })()
);
```

第一个 Set  应该包含在第二个  Set 中。

```js
assert(
  (function () {
    var setA = new Set();
    var setB = new Set();
    setA.add('a');
    setB.add('b');
    setB.add('c');
    setB.add('a');
    setB.add('d');
    var aIsSubsetOfB = setA.isSubsetOf(setB);
    return aIsSubsetOfB === true;
  })()
);
```

[‘ a’，‘ b’] . isSubsetOf ([‘ a’，‘ b’，‘ c’，‘ d’]) 应该返回  true  。

```js
assert(
  (function () {
    var setA = new Set();
    var setB = new Set();
    setA.add('a');
    setA.add('b');
    setB.add('a');
    setB.add('b');
    setB.add('c');
    setB.add('d');
    var aIsSubsetOfB = setA.isSubsetOf(setB);
    return aIsSubsetOfB === true;
  })()
);
```

[‘ a’，‘ b’，‘ c’] . isSubsetOf ([‘ a’，‘ b’])  应该返回  false 。

```js
assert(
  (function () {
    var setA = new Set();
    var setB = new Set();
    setA.add('a');
    setA.add('b');
    setA.add('c');
    setB.add('a');
    setB.add('b');
    var aIsSubsetOfB = setA.isSubsetOf(setB);
    return aIsSubsetOfB === false;
  })()
);
```

IsSubsetOf ([]) 应该返回true 。

```js
assert(
  (function () {
    var setA = new Set();
    var setB = new Set();
    var aIsSubsetOfB = setA.isSubsetOf(setB);
    return aIsSubsetOfB === true;
  })()
);
```

[‘ a’，‘ b’] . isSubsetOf ([‘ c’，‘ d’])  应该返回  false 。

```js
assert(
  (function () {
    var setA = new Set();
    var setB = new Set();
    setA.add('a');
    setA.add('b');
    setB.add('c');
    setB.add('d');
    var aIsSubsetOfB = setA.isSubsetOf(setB);
    return aIsSubsetOfB === false;
  })()
);
```

# --seed--

## --seed-contents--

```js
class Set {
  constructor() {
    // This will hold the set
    this.dictionary = {};
    this.length = 0;
  }
  // This method will check for the presence of an element and return true or false
  has(element) {
    return this.dictionary[element] !== undefined;
  }
  // This method will return all the values in the set
  values() {
    return Object.keys(this.dictionary);
  }
  // This method will add an element to the set
  add(element) {
    if (!this.has(element)) {
      this.dictionary[element] = true;
      this.length++;
      return true;
    }

    return false;
  }
  // This method will remove an element from a set
  remove(element) {
    if (this.has(element)) {
      delete this.dictionary[element];
      this.length--;
      return true;
    }

    return false;
  }
  // This method will return the size of the set
  size() {
    return this.length;
  }
  // This is our union method 
  union(set) {
    const newSet = new Set();
    this.values().forEach(value => {
      newSet.add(value);
    })
    set.values().forEach(value => {
      newSet.add(value);
    })

    return newSet;
  }
  // This is our intersection method
  intersection(set) {
    const newSet = new Set();

    let largeSet;
    let smallSet;
    if (this.dictionary.length > set.length) {
      largeSet = this;
      smallSet = set;
    } else {
      largeSet = set;
      smallSet = this;
    }

    smallSet.values().forEach(value => {
      if (largeSet.dictionary[value]) {
        newSet.add(value);
      }
    })

    return newSet;
  }

  difference(set) {
    const newSet = new Set();

    this.values().forEach(value => {
      if (!set.dictionary[value]) {
        newSet.add(value);
      }
    })

    return newSet;
  }
  // Only change code below this line

  // Only change code above this line
}
```

# --solutions--

```js
class Set {
  constructor() {
    this.dictionary = {};
    this.length = 0;
  }

  has(element) {
    return this.dictionary[element] !== undefined;
  }

  values() {
    return Object.keys(this.dictionary);
  }

  add(element) {
    if (!this.has(element)) {
      this.dictionary[element] = true;
      this.length++;
      return true;
    }

    return false;
  }

  remove(element) {
    if (this.has(element)) {
      delete this.dictionary[element];
      this.length--;
      return true;
    }

    return false;
  }

  size() {
    return this.length;
  }

  union(set) {
    const newSet = new Set();
    this.values().forEach(value => {
      newSet.add(value);
    })
    set.values().forEach(value => {
      newSet.add(value);
    })

    return newSet;
  }

  intersection(set) {
    const newSet = new Set();

    let largeSet;
    let smallSet;
    if (this.dictionary.length > set.length) {
      largeSet = this;
      smallSet = set;
    } else {
      largeSet = set;
      smallSet = this;
    }

    smallSet.values().forEach(value => {
      if (largeSet.dictionary[value]) {
        newSet.add(value);
      }
    })

    return newSet;
  }  

  difference(set) {
    const newSet = new Set();

    this.values().forEach(value => {
      if (!set.dictionary[value]) {
        newSet.add(value);
      }
    })

    return newSet;
  }

  isSubsetOf(set) {
    for(const value of this.values()){
      if(!set.dictionary[value]) return false;
    }
    return true
  }
}
```
