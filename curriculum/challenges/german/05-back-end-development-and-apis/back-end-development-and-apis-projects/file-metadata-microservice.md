---
id: bd7158d8c443edefaeb5bd0f
title: Datei-Metadaten-Microservice
challengeType: 4
forumTopicId: 301506
dashedName: file-metadata-microservice
---

# --description--

Build a full stack JavaScript app that is functionally similar to this: <a href="https://file-metadata-microservice.freecodecamp.rocks" target="_blank" rel="noopener noreferrer nofollow">https://file-metadata-microservice.freecodecamp.rocks</a>. Working on this project will involve you writing your code using one of the following methods:

-   Clone <a href="https://github.com/freeCodeCamp/boilerplate-project-filemetadata/" target="_blank" rel="noopener noreferrer nofollow">this GitHub repo</a> and complete your project locally.
-   Verwende <a href="https://gitpod.io/?autostart=true#https://github.com/freeCodeCamp/boilerplate-project-filemetadata/" target="_blank" rel="noopener noreferrer nofollow">unser Gitpod-Starteprojekt</a>, um dein Projekt abzuschließen.
-   Benutze einen Website-Builder deiner Wahl, um das Projekt abzuschließen. Achte darauf, alle Dateien von unserem GitHub-Repo zu integrieren.

# --instructions--

**HINT:** You can use the `multer` npm package to handle file uploading.

# --hints--

Du solltest dein eigenes Projekt bereitstellen, nicht die Beispiel-URL.

```js
(getUserInput) => {
  assert(
    !/.*\/file-metadata-microservice\.freecodecamp\.rocks/.test(
      getUserInput('url')
    )
  );
};
```

You can submit a form that includes a file upload.

```js
async (getUserInput) => {
  const site = await fetch(getUserInput('url'));
  const data = await site.text();
  const doc = new DOMParser().parseFromString(data, 'text/html');
  assert(doc.querySelector('input[type="file"]'));
};
```

The form file input field has the `name` attribute set to `upfile`.

```js
async (getUserInput) => {
  const site = await fetch(getUserInput('url'));
  const data = await site.text();
  const doc = new DOMParser().parseFromString(data, 'text/html');
  assert(doc.querySelector('input[name="upfile"]'));
};
```

When you submit a file, you receive the file `name`, `type`, and `size` in bytes within the JSON response.

```js
async (getUserInput) => {
  const formData = new FormData();
  const fileData = await fetch(
    'https://cdn.freecodecamp.org/weather-icons/01d.png'
  );
  const file = await fileData.blob();
  formData.append('upfile', file, 'icon');
  const data = await fetch(getUserInput('url') + '/api/fileanalyse', {
    method: 'POST',
    body: formData
  });
  const parsed = await data.json();
  assert.property(parsed, 'size');
  assert.equal(parsed.name, 'icon');
  assert.equal(parsed.type, 'image/png');
};
```

