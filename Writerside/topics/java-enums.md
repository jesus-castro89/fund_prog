# Tipos Enumerados en Java

Los tipos enumerados (o enums) en Java son una forma de definir un conjunto fijo de constantes con nombre. Esto permite
crear un tipo de dato que puede tomar un número limitado de valores, lo que facilita la lectura y el mantenimiento del
código.

## Declaración de un Enum

Para declarar un tipo enumerado en Java, se utiliza la palabra clave `enum` seguida del nombre del enum y las constantes
que lo componen. Por ejemplo:

```java
enum DiaSemana {
    LUNES, MARTES, MIERCOLES, JUEVES, VIERNES, SABADO, DOMINGO
}
```

En este caso, se ha declarado un enum `DiaSemana` con las constantes `LUNES`, `MARTES`, `MIERCOLES`, `JUEVES`,
`VIERNES`, `SABADO` y `DOMINGO`.

## Enums con Atributos y Métodos

Los enums en Java pueden tener atributos y métodos asociados a cada constante. Por ejemplo:

```java
enum DiaSemana {
    LUNES("Lunes", 1),
    MARTES("Martes", 2),
    MIERCOLES("Miércoles", 3),
    JUEVES("Jueves", 4),
    VIERNES("Viernes", 5),
    SABADO("Sábado", 6),
    DOMINGO("Domingo", 7);

    final String nombre;
    final int numero;

    DiaSemana(String nombre, int numero) {
        this.nombre = nombre;
        this.numero = numero;
    }

    String getNombre() {
        return nombre;
    }

    int getNumero() {
        return numero;
    }
}
```

En este caso, se ha añadido un atributo `nombre` y un atributo `numero` a cada constante del enum `DiaSemana`, así como
un constructor que inicializa estos atributos. También se han añadido métodos `getNombre()` y `getNumero()` para obtener
el nombre y el número de cada día de la semana.

## Uso de Enums

Los enums en Java se utilizan de la misma forma que cualquier otro tipo de dato. Por ejemplo, para obtener el nombre y
el número de un día de la semana:

```java
DiaSemana dia = DiaSemana.LUNES;
System.out.println("Nombre: " + dia.getNombre());
System.out.println("Número: " + dia.getNumero());
```

En este caso, se ha creado una variable `dia` de tipo `DiaSemana` y se ha asignado la constante `LUNES`. Luego, se
imprime el nombre y el número del día de la semana utilizando los métodos `getNombre()` y `getNumero()`.

## Ventajas de los Enums

Los enums en Java ofrecen varias ventajas, entre las que se incluyen:

* **Legibilidad**: Al utilizar enums, se hace más claro y legible el código, ya que se utilizan nombres descriptivos en
  lugar de valores numéricos.
* **Seguridad**: Los enums permiten restringir los valores que puede tomar una variable, evitando errores de asignación
  de valores incorrectos.
* **Mantenimiento**: Al definir un conjunto fijo de constantes en un enum, se facilita el mantenimiento del código, ya
  que cualquier cambio en las constantes se reflejará automáticamente en todo el código que las utilice.
* **Funcionalidad**: Los enums pueden tener atributos y métodos asociados, lo que permite añadir funcionalidad adicional
  a
  las constantes.
* **Compatibilidad**: Los enums son compatibles con otras características de Java, como switch-case, lo que facilita su
  uso en estructuras de control.
* **Tipado seguro**: Al utilizar enums, se obtiene un tipo seguro en tiempo de compilación, lo que evita errores de
  asignación de tipos incorrectos.

En resumen, los enums en Java son una forma eficaz de definir un conjunto fijo de constantes con nombre, lo que mejora
la legibilidad, la seguridad y el mantenimiento del código.

## Conclusión

Los tipos enumerados (enums) en Java son una herramienta poderosa para definir un conjunto fijo de constantes con
nombre. Al utilizar enums, se mejora la legibilidad, la seguridad y el mantenimiento del código, lo que facilita el
desarrollo de aplicaciones robustas y fáciles de mantener.

En resumen, los enums en Java son una característica fundamental del lenguaje que todo programador debería conocer y
utilizar en sus proyectos.