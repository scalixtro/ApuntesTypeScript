# Interfaces

Las interfaces son similares a los tipos de objeto, con las ventajas de que ofrecen mejores tiempos de compilación, mensajes de error más legibles y otras cosas.

La sintaxis de las interfaces es similar que al declarar un tipo de objeto. Las principales diferencias son:

* No se debe incluir el `=`.
* Se tiene la convención de no escribir al final `;`.

```ts
interface Poet {
    born: number;
    name: string;
}
```

Algunas características de las interfaces son:

* Se pueden combinar para añadir características.
* Se pueden utilizar para revisar la estructura de declaraciones de clases.
* Las interfaces se consideran *objetos con nombre*, a diferencia de los tipos de objetos que son *alias* para un objeto literal.

## Propiedades

### Parámetros opcionales

De igual manera se declaran parámetros opcionales utilizando `?`.

```ts
interface Poet {
    name: string;
    born: number;
    death?: number;
}
```

### Parámetros de sólo lectura

Las propiedades de sólo lectura se declaran con la palabra reservada `readonly`. Estos parámetros sólo funcionan dentro de TS y cuando se traspila el código a JS se pueden modificar los parámetros dentro de la ejecución del programa. Esto sólo protege a algunos parámetros de modificar mientras se usa el revisor de tipos de TS.

### Funciones

TS tiene dos formas de declarar funciones como miembros de interfaces.

* *Method syntax*: Es declarar la función con la notación usual de JS.
* *Property syntax*: Es