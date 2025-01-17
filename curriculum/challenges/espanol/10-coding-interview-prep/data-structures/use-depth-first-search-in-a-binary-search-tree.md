---
id: 587d8257367417b2b2512c7e
title: Usa Primera Búsqueda en Profundidad en un Árbol de Búsqueda Binaria
challengeType: 1
forumTopicId: 301719
dashedName: use-depth-first-search-in-a-binary-search-tree
---

# --description--

Conocemos como buscar un árbol de búsqueda binaria search para un valor específico. Pero qué pasa si solo queremos explorar el árbol entero? O ¿qué pasa si no tenemos un árbol ordenado y necesitamos buscar un valor? Aquí presentaremos algunos métodos de recorrido de árbol que pueden ser usados para explorar estructuras de datos árbol. El primero es búsqueda profundidad-primero (depth-first). En la búsqueda profundidad-primero, un sub árbol dado es explorado profundamente como sea posible antes que la búsqueda continue sobre otro sub árbol. Hay tres formas en las que esto puede hacerse: En orden (In-order): Inicia la búsqueda desde el nodo más a la izquierda y finaliza en el nodo más a la derecha. Pre ordenado (Pre-order): Explora todas las raíces antes que las hojas. Orden posterior (Post-order): Explora todas las hojas antes que las raíces. Como pudiste suponer, puedes escoger diferentes métodos de búsqueda dependiendo de que tipo de dato esta almacenando tu árbol y lo que estés buscando. Para una búsqueda de árbol binario, un recorrido en orden devuelve los nodos de forma ordenada.

# --instructions--

Aquí vamos a crear estos tres métodos de busqueda en nuestro árbol de búsqueda binario. La búsqueda en profundidad ("Depth-first search") es una operación inherentemente recursiva que continúa explorando subárboles más profundos siempre y cuando haya nodos hijos presentes. Una vez que entiendas este concepto básico, puedes simplemente reorganizar el orden en el cual exploras los nodos y subárboles para producir cualquiera de las búsquedas de árbol de arriba. Por ejemplo, en la búsqueda en postorden querríamos recorrer de manera recursiva hasta llegar a un nodo hoja antes de empezar a devolver cualquiera de los propios nodos, mientras que en la búsqueda en preorden querríamos devolver primero los nodos y luego continuar recorriendo de manera recursiva el árbol hacia abajo. Defina los métodos `inorder`, `preorder`y `postorder` en nuestro árbol. Cada uno de estos métodos debe devolver una matriz de elementos que representan el recorrido del árbol. Asegurate de devolver los valores enteros a cada nodo en el arreglo, no los nodos en sí. Finalmente, devuelve `null` si el árbol está vacío.

# --hints--

La estructura de datos `BinarySearchTree` debe exisitr.

```js
assert(
  (function () {
    var test = false;
    if (typeof BinarySearchTree !== 'undefined') {
      test = new BinarySearchTree();
    }
    return typeof test == 'object';
  })()
);
```

El árbol binario de búsqueda debe tener un método llamado `inorder`.

```js
assert(
  (function () {
    var test = false;
    if (typeof BinarySearchTree !== 'undefined') {
      test = new BinarySearchTree();
    } else {
      return false;
    }
    return typeof test.inorder == 'function';
  })()
);
```

El árbol binario de búsqueda debe tener un método llamado `preorder`.

```js
assert(
  (function () {
    var test = false;
    if (typeof BinarySearchTree !== 'undefined') {
      test = new BinarySearchTree();
    } else {
      return false;
    }
    return typeof test.preorder == 'function';
  })()
);
```

El árbol binario de búsqueda debe tener un método llamado `postorder`.

```js
assert(
  (function () {
    var test = false;
    if (typeof BinarySearchTree !== 'undefined') {
      test = new BinarySearchTree();
    } else {
      return false;
    }
    return typeof test.postorder == 'function';
  })()
);
```

El método `inorder` debe retornar una matriz de los valores de los nodos que resultan de un recorrido ordenado.

```js
assert(
  (function () {
    var test = false;
    if (typeof BinarySearchTree !== 'undefined') {
      test = new BinarySearchTree();
    } else {
      return false;
    }
    if (typeof test.inorder !== 'function') {
      return false;
    }
    test.add(7);
    test.add(1);
    test.add(9);
    test.add(0);
    test.add(3);
    test.add(8);
    test.add(10);
    test.add(2);
    test.add(5);
    test.add(4);
    test.add(6);
    return test.inorder().join('') == '012345678910';
  })()
);
```

El método `preorder` debe retornar una matriz de los valores de los nodos que resultan de un recorrido pre-ordenado.

```js
assert(
  (function () {
    var test = false;
    if (typeof BinarySearchTree !== 'undefined') {
      test = new BinarySearchTree();
    } else {
      return false;
    }
    if (typeof test.preorder !== 'function') {
      return false;
    }
    test.add(7);
    test.add(1);
    test.add(9);
    test.add(0);
    test.add(3);
    test.add(8);
    test.add(10);
    test.add(2);
    test.add(5);
    test.add(4);
    test.add(6);
    return test.preorder().join('') == '710325469810';
  })()
);
```

El método `postorder` debe retornar una matriz de los valores de los nodos que resultan de un recorrido post-ordenado.

```js
assert(
  (function () {
    var test = false;
    if (typeof BinarySearchTree !== 'undefined') {
      test = new BinarySearchTree();
    } else {
      return false;
    }
    if (typeof test.postorder !== 'function') {
      return false;
    }
    test.add(7);
    test.add(1);
    test.add(9);
    test.add(0);
    test.add(3);
    test.add(8);
    test.add(10);
    test.add(2);
    test.add(5);
    test.add(4);
    test.add(6);
    return test.postorder().join('') == '024653181097';
  })()
);
```

El método `inorder` debería devolver `null` para un árbol vacío.

```js
assert(
  (function () {
    var test = false;
    if (typeof BinarySearchTree !== 'undefined') {
      test = new BinarySearchTree();
    } else {
      return false;
    }
    if (typeof test.inorder !== 'function') {
      return false;
    }
    return test.inorder() == null;
  })()
);
```

El método `preorder` debería devolver `null` para un árbol vacío.

```js
assert(
  (function () {
    var test = false;
    if (typeof BinarySearchTree !== 'undefined') {
      test = new BinarySearchTree();
    } else {
      return false;
    }
    if (typeof test.preorder !== 'function') {
      return false;
    }
    return test.preorder() == null;
  })()
);
```

El método `postorder` debe retornar `null` para un árbol vacío.

```js
assert(
  (function () {
    var test = false;
    if (typeof BinarySearchTree !== 'undefined') {
      test = new BinarySearchTree();
    } else {
      return false;
    }
    if (typeof test.postorder !== 'function') {
      return false;
    }
    return test.postorder() == null;
  })()
);
```

# --seed--

## --after-user-code--

```js
BinarySearchTree.prototype = Object.assign(
  BinarySearchTree.prototype,
  {
    add: function(value) {
      function searchTree(node) {
        if (value < node.value) {
          if (node.left == null) {
            node.left = new Node(value);
            return;
          } else if (node.left != null) {
            return searchTree(node.left);
          }
        } else if (value > node.value) {
          if (node.right == null) {
            node.right = new Node(value);
            return;
          } else if (node.right != null) {
            return searchTree(node.right);
          }
        } else {
          return null;
        }
      }

      var node = this.root;
      if (node == null) {
        this.root = new Node(value);
        return;
      } else {
        return searchTree(node);
      }
    }
  }
);
```

## --seed-contents--

```js
var displayTree = tree => console.log(JSON.stringify(tree, null, 2));
function Node(value) {
  this.value = value;
  this.left = null;
  this.right = null;
}
function BinarySearchTree() {
  this.root = null;
  // Only change code below this line

  // Only change code above this line
}
```

# --solutions--

```js
var displayTree = tree => console.log(JSON.stringify(tree, null, 2));
function Node(value) {
  this.value = value;
  this.left = null;
  this.right = null;
}
function BinarySearchTree() {
  this.root = null;
  this.result = [];

  this.inorder = function(node) {
    if (!node) node = this.root;
    if (!node) return null;

    if (node.left) this.inorder(node.left);
    this.result.push(node.value);
    if (node.right) this.inorder(node.right);
    return this.result;
  };
  this.preorder = function(node) {
    if (!node) node = this.root;
    if (!node) return null;

    this.result.push(node.value);
    if (node.left) this.preorder(node.left);
    if (node.right) this.preorder(node.right);
    return this.result;
  };
  this.postorder = function(node) {
    if (!node) node = this.root;
    if (!node) return null;

    if (node.left) this.postorder(node.left);
    if (node.right) this.postorder(node.right);
    this.result.push(node.value);

    return this.result;
  };
}
```
