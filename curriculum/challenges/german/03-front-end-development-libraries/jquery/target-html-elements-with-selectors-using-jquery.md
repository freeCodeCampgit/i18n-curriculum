---
id: bad87fee1348bd9bedc08826
title: HTML-Elemente mithilfe von Selektoren mit jQuery auswählen
challengeType: 6
forumTopicId: 18319
required:
  - 
    link: 'https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.2.0/animate.css'
dashedName: target-html-elements-with-selectors-using-jquery
---

# --description--

Now we have a `document ready` function.

Jetzt schreiben wir unsere erste jQuery-Anweisung. Alle jQuery-Funktionen beginnen mit einem `$`, der normalerweise als Dollarzeichen-Operator oder als Bling bezeichnet wird.

Oft wählt jQuery ein HTML-Element mit einem <dfn>Selektor</dfn> aus und macht dann etwas mit diesem Element.

Lass zum Beispiel alle deine `button`-Elemente hüpfen. Füge diesen Code einfach in deine document ready-Funktion ein:

```js
$("button").addClass("animated bounce");
```

Beachte, dass wir sowohl die jQuery-Bibliothek als auch die Animate.css-Bibliothek bereits im Hintergrund eingebunden haben, damit du sie im Editor verwenden kannst. Du benutzt also jQuery, um die Animate.css Klasse `bounce` auf deine `button`-Elemente anzuwenden.

# --hints--

Du solltest die jQuery Funktion `addClass()` verwenden, um deinen `button`-Elementen die Klassen `animated` und `bounce` zu geben.

```js
assert($('button').hasClass('animated') && $('button').hasClass('bounce'));
```

Du solltest nur jQuery verwenden, um diese Klassen zu dem Element hinzuzufügen.

```js
assert(!code.match(/class.*animated/g));
```

Dein jQuery-Code sollte innerhalb der `$(document).ready();`-Funktion stehen.

```js
assert(
  code.replace(/\s/g, '').match(/\$\(document\)\.ready\(function\(\)\{\$/g)
);
```

# --seed--

## --seed-contents--

```html
<script>
  $(document).ready(function() {

  });
</script>

<!-- Only change code above this line -->

<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <h4>#left-well</h4>
      <div class="well" id="left-well">
        <button class="btn btn-default target" id="target1">#target1</button>
        <button class="btn btn-default target" id="target2">#target2</button>
        <button class="btn btn-default target" id="target3">#target3</button>
      </div>
    </div>
    <div class="col-xs-6">
      <h4>#right-well</h4>
      <div class="well" id="right-well">
        <button class="btn btn-default target" id="target4">#target4</button>
        <button class="btn btn-default target" id="target5">#target5</button>
        <button class="btn btn-default target" id="target6">#target6</button>
      </div>
    </div>
  </div>
</div>
```

# --solutions--

```html
<script>
  $(document).ready(function() {
    $("button").addClass("animated bounce");
  });
</script>

<!-- Only change code above this line -->

<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <h4>#left-well</h4>
      <div class="well" id="left-well">
        <button class="btn btn-default target" id="target1">#target1</button>
        <button class="btn btn-default target" id="target2">#target2</button>
        <button class="btn btn-default target" id="target3">#target3</button>
      </div>
    </div>
    <div class="col-xs-6">
      <h4>#right-well</h4>
      <div class="well" id="right-well">
        <button class="btn btn-default target" id="target4">#target4</button>
        <button class="btn btn-default target" id="target5">#target5</button>
        <button class="btn btn-default target" id="target6">#target6</button>
      </div>
    </div>
  </div>
</div>
```
