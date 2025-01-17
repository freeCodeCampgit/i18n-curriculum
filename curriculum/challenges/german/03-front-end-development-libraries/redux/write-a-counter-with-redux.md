---
id: 5a24c314108439a4d4036157
title: Schreibe einen Zähler mit Redux
challengeType: 6
forumTopicId: 301453
dashedName: write-a-counter-with-redux
---

# --description--

Now you've learned all the core principles of Redux! You've seen how to create actions and action creators, create a Redux store, dispatch your actions against the store, and design state updates with pure reducers. You've even seen how to manage complex state with reducer composition and handle asynchronous actions. These examples are simplistic, but these concepts are the core principles of Redux. If you understand them well, you're ready to start building your own Redux app. The next challenges cover some of the details regarding `state` immutability, but first, here's a review of everything you've learned so far.

# --instructions--

In dieser Lektion wirst du einen einfachen Zähler mit Redux von Grund auf implementieren. Die Grundlagen werden im Code-Editor bereitgestellt, aber du musst die Details ergänzen! Verwende die bereitgestellten Namen und definiere die Action Creator `incAction` und `decAction`, die `counterReducer()`, `INCREMENT` und `DECREMENT` Aktionstypen und schließlich den Redux `store`. Sobald du fertig bist, solltest du `INCREMENT` oder `DECREMENT` Aktionen ausführen können, um den Zustand im `store` zu erhöhen oder zu verringern. Viel Erfolg beim Erstellen deiner ersten Redux-App!

# --hints--

Der Action Creator `incAction` sollte ein Action-Objekt mit `type` gleich dem Wert von `INCREMENT` zurückgeben.

```js
assert(incAction().type === INCREMENT);
```

Der Action Creator `decAction` sollte ein Action-Objekt mit `type` gleich dem Wert von `DECREMENT` zurückgeben

```js
assert(decAction().type === DECREMENT);
```

Die Ausführung von `store.getState()` sollte eine Zahl zurückgeben.

```js
assert(typeof store.getState() === 'number');
```

Der Redux-Store sollte mit einem `state` von 0 initialisieren.

```js
assert(_store.getState() === 0);
```

Das Senden von `incAction` an den Redux-Store sollte den `state` um 1 erhöhen.

```js
assert(
  (function () {
    const initialState = _store.getState();
    _store.dispatch(incAction());
    const incState = _store.getState();
    return initialState + 1 === incState;
  })()
);
```

Das Senden von `decAction` an den Redux-Store sollte den `state` um 1 verringern.

```js
assert(
  (function () {
    const initialState = _store.getState();
    _store.dispatch(decAction());
    const decState = _store.getState();
    return initialState - 1 === decState;
  })()
);
```

`counterReducer` sollte eine Funktion sein

```js
assert(typeof counterReducer === 'function');
```

# --seed--

## --seed-contents--

```js
const INCREMENT = null; // Define a constant for increment action types
const DECREMENT = null; // Define a constant for decrement action types

const counterReducer = null; // Define the counter reducer which will increment or decrement the state based on the action it receives

const incAction = null; // Define an action creator for incrementing

const decAction = null; // Define an action creator for decrementing

const store = null; // Define the Redux store here, passing in your reducers
```

## --after-user-code--

```js
const _store = Redux.createStore(counterReducer)
```

# --solutions--

```js
const INCREMENT = 'INCREMENT';
const DECREMENT = 'DECREMENT';

const counterReducer = (state = 0, action) => {
  switch(action.type) {
    case INCREMENT:
      return state + 1;
    case DECREMENT:
      return state - 1;
    default:
      return state;
  }
};

const incAction = () => {
  return {
    type: INCREMENT
  }
};

const decAction = () => {
  return {
    type: DECREMENT
  }
};

const store = Redux.createStore(counterReducer);
```
