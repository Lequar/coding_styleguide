# Lequar Guia de Estilo en Codificación.
Esta es la forma en que deberíamos escribir código.

## Generalidades

* Usar comillas sencillas '' para las cadenas de texto.
* Utilizar CamelCase como modo de creacion de variables, clases y funciones. Preferiblemente "lowerCamelCase" (https://es.wikipedia.org/wiki/CamelCase)

### Mensajes "Commit"

* Para los mensajes de "commit" importante escribir una cabecera entendible, junto a una pequeña descripcion, Ejemplo: "Backend: modificacion 'archivo.php' se agregaron 12 clases..."
- Las cabeceras a utilizar serian:
   * Backend.
   * Frontend.
   * Solucion Error.
- El enviar los commits pueden empezar junto a un Emoji:
   * :art: `:art:` -> Para realizar cambios visuales
   * :bug: `:bug:` -> Para arreglar errores
   * :recycle: `:recycle:` -> Para limpiar codigo 
   * :white_check_mark: `:white_check_mark:` -> Para confirmar arreglo de error
   * :book: `:book:` -> Para escribir documentación
   * :laughing: `:laughing:` -> Para agregar cambio completado y funcionando

### Comentarios

Preferiblemente escribir solamente "strings" (Cadenas de texto)

> Mal ejemplo

```php
class Test {
  /* Creating class num 212 */
}
```

> Buen ejemplo

```php
class Test {
  // Creating class Test
}
```

## HTML

* Utilizar 4 espacios de tabulador
* Dejar elementos comentados para mayor legibilidad.

### Declaraciones de plantilla

Para una mayor legibilidad, hemos decidio incluir de una manera organizada y facil la interoretacion del PHP para indexarlo en el HTML.

> Mal ejemplo

```php
<div class="header">
    <div class="container">
        <?php 
        if(i=0) { ?>
          <p>Hola</p>
        <?php 
        } 
        ?>
    </div>
</div>
```

> Buen ejemplo

```php
<div class="header">
    <div class="container">
        <?php if ($i = 0) : ?>
          <p>Hola</p>
        <?php endif; ?>
    </div>
</div>
```

** Esto es para que cuando el encargado del frontend lea la plantilla le sea mucho mas entendible y posteriormente su tiempo de analisis sea menor.
** Al abrir el PHP de esta manera y cerrarlo en la misma linea permite que sea entendido inmediatamente.

```php
<?php if ($i = 0) : ?>
```

### Indexacion

Asegúrese de que los elementos están organizados de la mejor forma.

> Mal ejemplo

```html
<div class="header">
   <div class="container">
   <div class="row">
   <h1>Lequar</h1>
   </div>
   </div>
</div>
```
> Buen ejemplo

```html
<div class="header">
   <div class="container">
        <div class="row">
            <h1>Lequar</h1>
        </div>
    </div>
</div>
```

### Atributos

No utilizar espacion antes y despues de los '='

> Mal ejemplo

```html
<div class = "header"></div>
```

> Buen ejemplo

```html
<div class="header"></div>
```

## JavaScript

### Declaracion de variables

Usar CamelCase con el tipo "lowerCamelCase" para las declaraciones.

> Mal ejemplo

```js
var stars_counter = 10;
```

> Buen ejemplo

```js
var starsCounter = 10;
```

### Palabras reservadas

Evitar el uso de estas palabras en las variables y funciones:

event, native, class y otras palabras reservadas en JavaScript. (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Reserved_keywords_as_of_ECMAScript_6)

### Declaracion de funciones

Añadir un espacio después del paréntesis de la función de cierre.

> Mal ejemplo


```js
function baz(fum, bar){
    // Resto de codigo...
}
```

> Buen ejemplo

```js
function baz(fum, bar) {
    // Resto de codigo...
}
```
### JQuery

Utilice esta dentro de las devoluciones de llamada jQuery para referirse al elemento actual.

> Mal ejemplo 

```js
$('a').click(function(e) {
    $(e.target).hide();
});
```
> Buen ejemplo

```js
$('a').on('click', function() {
    $(this).hide();
});
```

