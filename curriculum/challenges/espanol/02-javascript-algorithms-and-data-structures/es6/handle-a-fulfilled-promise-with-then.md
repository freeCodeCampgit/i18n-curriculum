---
id: 5cdafbd72913098997531681
title: Maneja una promesa cumplida usando then
challengeType: 1
forumTopicId: 301203
dashedName: handle-a-fulfilled-promise-with-then
---

# --description--

Las promesas son muy útiles, cuando tu tienes un proceso que toma una cantidad de tiempo desconocida en tu código (algo asíncrono por ejemplo), a menudo una petición de servidor. Cuando tu haces una petición a un servidor, toma algo de tiempo, después de que termina, normalmente quieres hacer algo con la respuesta del servidor. Esto se puede lograr utilizando el método `then`.

```js
Promise.prototype.then(onFulfilled, onRejected)
```

El método `then` agenda funciones de devolución para el cumplimiento de una Promesa - sea logro o rechazo. Uno de los controladores `onFulfilled` y `onRejected` será ejecutado para manejar el cumplimiento o el rechazo de la promesa actual. Cuando la promesa se cumple con `resolve` se llama al manejador `onFulfilled`.

```js
myPromise.then(result => {

});
```

`result` viene con el argumento proporcionado al método `resolve`.

# --instructions--

Añade el método `then` a tu promesa. Usa `result` como parámetro de tu función callback, asimismo imprime `result` en la consola.

# --hints--

Debes llamar al método `then` en la promesa.

```js
assert(
  __helpers.removeWhiteSpace(__helpers.removeJSComments(code)).match(/(makeServerRequest|\))\.then\(/g)
);
```

El método `then`, debe tener una función callback con `result` como parámetro.

```js
assert(resultIsParameter);
```

Debes imprimir `result` en la consola.

```js
assert(
  resultIsParameter &&
    __helpers
      .removeWhiteSpace(__helpers.removeJSComments(code))
      .match(/\.then\(.*?result.*?console.log\(result\).*?\)/)
);
```

# --seed--

## --after-user-code--

```js
const resultIsParameter = /\.then\((function\(result\){|result|\(result\)=>)/.test(__helpers.removeWhiteSpace(__helpers.removeJSComments(code)));
```

## --seed-contents--

```js
const makeServerRequest = new Promise((resolve, reject) => {
  // responseFromServer is set to true to represent a successful response from a server
  let responseFromServer = true;

  if(responseFromServer) {
    resolve("We got the data");
  } else {  
    reject("Data not received");
  }
});
```

# --solutions--

```js
const makeServerRequest = new Promise((resolve, reject) => {
  // responseFromServer is set to true to represent a successful response from a server
  let responseFromServer = true;

  if(responseFromServer) {
    resolve("We got the data");
  } else {  
    reject("Data not received");
  }
});

makeServerRequest.then(result => {
  console.log(result);
});
```
