# PSP 05 - SERVIDOR HTTP

## CABECERA DATE

Para la cabecera date se ha creado la función `fechaHora()` en la clase `Paginas`.

Esta función devuelve un String del objeto `Date` formateado con `DateTimeFormatter`.

## MULTIHILO

Se ha creado la clase `HiloDespachador` que extiende la clase `Thread`.

Desde la clase `ServidorHTTP`, cada vez que se atiende a un cliente se crea una instancia de esta nueva clase.  Se inicia el hilo con `start()` y en su método `run()` ejecuta el código que tramita la petición del cliente (este código antes estaba en un método de la clase `ServidorHTTP`).

## PROBANDO LA APP

Ejecutar la aplicaición e ingresar en un navegador: `localhost:8066` para conectarse al servidor. Esta es la página inicial.

Resto de páginas proporcionadas por el servidor:

+ `localhost:8066/quijote` -> muestra un fragmento del Quijote.
+ `localhost:8066/` más cualquier otra cosa -> muestra página de error.