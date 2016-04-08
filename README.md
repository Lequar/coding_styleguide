# Lequar Guia de Estilo en Codificación.
Esta es la forma en que deberíamos escribir código.

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
