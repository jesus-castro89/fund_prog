# Constructores

Un constructor en Java es un método especial que se utiliza para inicializar un objeto de una clase. Los constructores
tienen el mismo nombre que la clase a la que pertenecen y no tienen tipo de retorno. Se utilizan para asignar valores
iniciales a los atributos de un objeto cuando se crea una instancia de la clase o tipo enumerado.

## Declaración de un Constructor

Para declarar un constructor en Java, se utiliza el mismo nombre que la clase a la que pertenece y se define sin tipo de
retorno. Por ejemplo:

```java
class Persona {
    String nombre;
    int edad;

    Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}
```

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
}
```

En estos ejemplos, se ha declarado un constructor para la clase `Persona` y para el tipo enumerado `DiaSemana`. El
constructor de la clase `Persona` recibe dos parámetros (`nombre` y `edad`) y asigna los valores correspondientes a los
atributos de la clase. El constructor del tipo enumerado `DiaSemana` recibe dos parámetros (`nombre` y `numero`) y
asigna los valores correspondientes a los atributos de cada constante del enum.

## Uso de un Constructor

Para utilizar un constructor en Java, se debe llamar al método `new` seguido del nombre de la clase y los parámetros
necesarios para inicializar el objeto. Por ejemplo:

```java
Persona persona = new Persona("Juan", 30);
```

```java
DiaSemana dia = DiaSemana.LUNES;
```

En estos ejemplos, se ha creado una instancia de la clase `Persona` con el nombre «Juan» y la edad 30, y se ha asignado
la constante `LUNES` del enum `DiaSemana` a la variable `dia`.

## Sobrecarga de Constructores

En Java, es posible definir varios constructores para una clase, siempre y cuando tengan diferentes listas de
parámetros. Esto se conoce como sobrecarga de constructores y permite crear instancias de la clase con diferentes
combinaciones de valores. Por ejemplo:

```java
class Persona {
    String nombre;
    int edad;

    Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    Persona(String nombre) {
        this.nombre = nombre;
        this.edad = 0;
    }
}
```

En este ejemplo, se ha definido un segundo constructor para la clase `Persona` que recibe solo el nombre de la persona y
asigna la edad por defecto a 0. Esto permite crear instancias de la clase `Persona` con diferentes combinaciones de
valores para los atributos.

## Conclusión

Los constructores en Java son métodos especiales que se utilizan para inicializar objetos de una clase. Permiten asignar
valores iniciales a los atributos de un objeto cuando se crea una instancia de la clase. Es posible definir varios
constructores para una clase mediante la sobrecarga de constructores, lo que facilita la creación de instancias con
diferentes combinaciones de valores.