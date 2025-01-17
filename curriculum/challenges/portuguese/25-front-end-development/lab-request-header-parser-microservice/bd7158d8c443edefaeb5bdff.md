---
id: bd7158d8c443edefaeb5bdff
title: Crie um microsserviço conversor de requisição de cabeçalho
challengeType: 4
dashedName: lab-request-header-parser-microservice
---

# --description--

Crie uma aplicação full stack em JavaScript que seja funcionalmente semelhante a esta: <a href="https://request-header-parser-microservice.freecodecamp.rocks/" target="_blank" rel="noopener noreferrer nofollow">https://request-header-parser-microservice.freecodecamp.rocks/</a>. Trabalhar nesse projeto vai fazer com que você escreva o código usando um dos seguintes métodos:

-   Clone <a href="https://github.com/freeCodeCamp/boilerplate-project-headerparser/" target="_blank" rel="noopener noreferrer nofollow">este repositório do GitHub</a> e complete o projeto localmente.
-   Use <a href="https://gitpod.io/?autostart=true#https://github.com/freeCodeCamp/boilerplate-project-headerparser/" target="_blank" rel="noopener noreferrer nofollow">nosso projeto inicial no Gitpod</a> para completar seu projeto.
-   Use um criador de sites de sua escolha para completar o projeto. Certifique-se de incorporar todos os arquivos do nosso repositório no GitHub.

# --hints--

Você deve fornecer seu próprio projeto, não o exemplo de URL.

```js
(getUserInput) => {
  assert(
    !/.*\/request-header-parser-microservice\.freecodecamp\.rocks/.test(
      getUserInput('url')
    )
  );
};
```

Uma solicitação a `/api/whoami` deve retornar um objeto JSON com o seu endereço IP na chave `ipaddress`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/whoami').then(
    (data) => assert(data.ipaddress && data.ipaddress.length > 0),
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Uma solicitação a `/api/whoami` deve retornar um objeto JSON com o seu idioma preferido na chave `language`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/whoami').then(
    (data) => assert(data.language && data.language.length > 0),
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Uma solicitação a `/api/whoami` deve retornar um objeto JSON com o seu software na chave `software`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/whoami').then(
    (data) => assert(data.software && data.software.length > 0),
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

