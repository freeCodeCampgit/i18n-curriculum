---
id: 56533eb9ac21ba0edf2244cf
title: 记录集合
challengeType: 1
forumTopicId: 18261
dashedName: record-collection
---

# --description--

You are creating a function that aids in the maintenance of a musical album collection. The collection is organized as an object that contains multiple albums which are also objects. Each album is represented in the collection with a unique `id` as the property name. Within each album object, there are various properties describing information about the album. Not all albums have complete information.

`updateRecords` 函数有 4 个参数，即以下参数：

-   `records` - an object containing several individual albums
-   `id` - a number representing a specific album in the `records` object
-   `prop` - a string representing the name of the album’s property to update
-   `value` - a string containing the information used to update the album’s property

使用下面的规则完成函数来修改传递给函数的对象。

-   Your function must always return the entire `records` object.
-   如果 `value` 是空字符串，从专辑里删除指定的 `prop`。
-   如果 `prop` 不是 `tracks`，并且 `value` 不是一个空字符串，将 `value` 赋给那个专辑的 `prop`。
-   如果 `prop` 是 `tracks` 并且 `value` 不是空字符串，但是专辑没有 `tracks` 属性，为该属性创建一个空数组并添加 `value` 作为其元素。
-   如果 prop 是 `tracks` 并且 `value` 不是一个空字符串，将 `value` 添加到专辑现有 `tracks` 数组的末尾。

**注意：** 将 `recordCollection` 对象的副本用于测试。 你不应该直接修改 `recordCollection` 对象。

# --hints--

执行 `updateRecords(recordCollection, 5439, "artist", "ABBA")` 后，`artist` 的值应该是字符串 `ABBA`。

```js
assert(
  updateRecords(_recordCollection, 5439, 'artist', 'ABBA')[5439]['artist'] ===
    'ABBA'
);
```

执行 `updateRecords(recordCollection, 5439, "tracks", "Take a Chance on Me")` 后，`tracks` 的最后一个和唯一一个元素应该为字符串 `Take a Chance on Me`。

```js
assert(
  updateRecords(_recordCollection, 5439, 'tracks', 'Take a Chance on Me') &&
  _recordCollection[5439]['tracks'].length === 1 &&
  _recordCollection[5439]['tracks'].pop() === 'Take a Chance on Me'
);
```

执行 `updateRecords(recordCollection, 2548, "artist", "")` 后，`artist` 不应被设置为任何值。

```js
updateRecords(_recordCollection, 2548, 'artist', '');
assert(!_recordCollection[2548].hasOwnProperty('artist'));
```

执行 `updateRecords(recordCollection, 1245, "tracks", "Addicted to Love")` 后，`tracks` 的最后一个元素应该为字符串 `Addicted to Love`。

```js
assert(
  updateRecords(_recordCollection, 1245, 'tracks', 'Addicted to Love')[1245][
    'tracks'
  ].pop() === 'Addicted to Love'
);
```

执行 `updateRecords(recordCollection, 2468, "tracks", "Free")` 后，`tracks` 的第一个元素应该为字符串 `1999`。

```js
assert(
  updateRecords(_recordCollection, 2468, 'tracks', 'Free')[2468][
    'tracks'
  ][0] === '1999'
);
```

执行 `updateRecords(recordCollection, 2548, "tracks", "")` 后，`tracks` 不应被设置为任何值。

```js
updateRecords(_recordCollection, 2548, 'tracks', '');
assert(!_recordCollection[2548].hasOwnProperty('tracks'));
```

执行 `updateRecords(recordCollection, 1245, "albumTitle", "Riptide")` 后，`albumTitle` 的值应该是字符串 `Riptide`。

```js
assert(
  updateRecords(_recordCollection, 1245, 'albumTitle', 'Riptide')[1245][
    'albumTitle'
  ] === 'Riptide'
);
```

# --seed--

## --before-user-code--

```js
const _recordCollection = {
  2548: {
    albumTitle: 'Slippery When Wet',
    artist: 'Bon Jovi',
    tracks: ['Let It Rock', 'You Give Love a Bad Name']
  },
  2468: {
    albumTitle: '1999',
    artist: 'Prince',
    tracks: ['1999', 'Little Red Corvette']
  },
  1245: {
    artist: 'Robert Palmer',
    tracks: []
  },
  5439: {
    albumTitle: 'ABBA Gold'
  }
};
```

## --seed-contents--

```js
// Setup
const recordCollection = {
  2548: {
    albumTitle: 'Slippery When Wet',
    artist: 'Bon Jovi',
    tracks: ['Let It Rock', 'You Give Love a Bad Name']
  },
  2468: {
    albumTitle: '1999',
    artist: 'Prince',
    tracks: ['1999', 'Little Red Corvette']
  },
  1245: {
    artist: 'Robert Palmer',
    tracks: []
  },
  5439: {
    albumTitle: 'ABBA Gold'
  }
};

// Only change code below this line
function updateRecords(records, id, prop, value) {
  return records;
}

updateRecords(recordCollection, 5439, 'artist', 'ABBA');
```

# --solutions--

```js
const recordCollection = {
  2548: {
    albumTitle: 'Slippery When Wet',
    artist: 'Bon Jovi',
    tracks: ['Let It Rock', 'You Give Love a Bad Name']
  },
  2468: {
    albumTitle: '1999',
    artist: 'Prince',
    tracks: ['1999', 'Little Red Corvette']
  },
  1245: {
    artist: 'Robert Palmer',
    tracks: []
  },
  5439: {
    albumTitle: 'ABBA Gold'
  }
};

// Only change code below this line
function updateRecords(records, id, prop, value) {
  if (value === '') delete records[id][prop];
  else if (prop === 'tracks') {
    records[id][prop] = records[id][prop] || [];
    records[id][prop].push(value);
  } else {
    records[id][prop] = value;
  }

  return records;
}
```
