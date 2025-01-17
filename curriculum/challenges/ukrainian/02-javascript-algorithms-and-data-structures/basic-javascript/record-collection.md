---
id: 56533eb9ac21ba0edf2244cf
title: Колекція музичних альбомів
challengeType: 1
forumTopicId: 18261
dashedName: record-collection
---

# --description--

You are creating a function that aids in the maintenance of a musical album collection. The collection is organized as an object that contains multiple albums which are also objects. Each album is represented in the collection with a unique `id` as the property name. Within each album object, there are various properties describing information about the album. Not all albums have complete information.

Функція `updateRecords` приймає 4 аргументи, представлені такими параметрами функції:

-   `records` - an object containing several individual albums
-   `id` - a number representing a specific album in the `records` object
-   `prop` - a string representing the name of the album’s property to update
-   `value` - a string containing the information used to update the album’s property

Завершіть функцію, використовуючи правила нижче, щоб змінити об’єкт, переданий до функції.

-   Your function must always return the entire `records` object.
-   Якщо `value` є пустим рядком, видаліть дану властивість `prop` з альбому.
-   Якщо `prop` не є `tracks` та `value` не є пустим рядком, призначте `value` до `prop` альбому.
-   Якщо `prop` є `tracks` та `value` не є пустим рядком, але альбом не має властивості `tracks`, створіть порожній масив та додайте `value` до нього.
-   Якщо `prop` є `tracks` та `value` не є пустим рядком, додайте `value` в кінець наявного масиву `tracks`.

**Примітка:** копія об’єкту `recordCollection` використовується для тестів. Ви не повинні напряму змінювати об’єкт `recordCollection`.

# --hints--

Після `updateRecords(recordCollection, 5439, "artist", "ABBA")`, `artist` має стати рядком `ABBA`

```js
assert(
  updateRecords(_recordCollection, 5439, 'artist', 'ABBA')[5439]['artist'] ===
    'ABBA'
);
```

Після `updateRecords(recordCollection, 5439, "tracks", "Take a Chance on Me")`, `tracks` повинен мати рядок `Take a Chance on Me` як останній та єдиний елемент.

```js
assert(
  updateRecords(_recordCollection, 5439, 'tracks', 'Take a Chance on Me') &&
  _recordCollection[5439]['tracks'].length === 1 &&
  _recordCollection[5439]['tracks'].pop() === 'Take a Chance on Me'
);
```

Після `updateRecords(recordCollection, 2548, "artist", "")`, `artist` не має бути налаштованим

```js
updateRecords(_recordCollection, 2548, 'artist', '');
assert(!_recordCollection[2548].hasOwnProperty('artist'));
```

Після `updateRecords(recordCollection, 1245, "tracks", "Addicted to Love")`, `tracks` повинен мати рядок `Addicted to Love` як останній елемент.

```js
assert(
  updateRecords(_recordCollection, 1245, 'tracks', 'Addicted to Love')[1245][
    'tracks'
  ].pop() === 'Addicted to Love'
);
```

Після `updateRecords(recordCollection, 2468, "tracks", "Free")`, `tracks` повинен мати рядок `1999` як перший елемент.

```js
assert(
  updateRecords(_recordCollection, 2468, 'tracks', 'Free')[2468][
    'tracks'
  ][0] === '1999'
);
```

Після `updateRecords(recordCollection, 2548, "tracks", "")`, `tracks` не має бути налаштованим

```js
updateRecords(_recordCollection, 2548, 'tracks', '');
assert(!_recordCollection[2548].hasOwnProperty('tracks'));
```

Після `updateRecords(recordCollection, 1245, "albumTitle", "Riptide")`, `albumTitle` має стати рядком `Riptide`

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
