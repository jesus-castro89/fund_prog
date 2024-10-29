# Clases, Funciones y Atributos

En Java, una clase es una plantilla para crear objetos que define los atributos y métodos que tendrán esos objetos. Los
atributos representan el estado de un objeto, mientras que los métodos definen su comportamiento. En este apartado, se
explicará cómo definir y utilizar clases, funciones y atributos en Java.

## Clases en Java

En Java, una clase se define utilizando la palabra clave `class`, seguida del nombre de la clase y el cuerpo de la clase
encerrado entre llaves `{}`, usando la siguiente estructura:

```java
class NombreDeLaClase {
    // Atributos
    // Métodos
}
```

Por ejemplo, la siguiente clase `Persona` define una clase simple con un atributo `nombre` y un método `saludar`:

```java
class Persona {
    // Atributo
    String nombre;

    // Método
    void saludar() {
        System.out.println("Hola, mi nombre es " + nombre);
    }
}
```

En este ejemplo, la clase `Persona` tiene un atributo `nombre` de tipo `String` y un método `saludar` que imprime un
mensaje de saludo con el nombre de la persona.

## Atributos en Java

Los atributos de una clase representan el estado de un objeto y se definen dentro de la clase. En Java, los atributos
pueden ser de diferentes tipos de datos, como `int`, `double`, `String`, etc. Para acceder a los atributos de un
objeto, se utiliza la notación de punto `.` seguida del nombre del atributo.

Por ejemplo, para crear un objeto de la clase `Persona` y acceder a su atributo `nombre`, se puede hacer lo siguiente:

```java
class Main {
    public static void main(String[] args) {
        // Crear un objeto de la clase Persona
        Persona persona = new Persona();

        // Asignar un valor al atributo nombre
        persona.nombre = "Juan";

        // Llamar al método saludar
        persona.saludar();
    }
}
```

> **Nota:** En este ejemplo, se crea un objeto `persona` de la clase `Persona`, se asigna un valor al atributo `nombre`
> y se llama al método `saludar` para imprimir un mensaje de saludo.

> **Nota:** Para crear un nuevo objeto de una clase, se utiliza la palabra clave `new` seguida del nombre de la clase y
> los paréntesis `()`. Por ejemplo, `Persona persona = new Persona();`. Aunque también se puede crear un objeto sin
> paréntesis si la clase tiene un constructor sin argumentos, por ejemplo, `Persona persona = new Persona;`. O
> mediante un constructor con argumentos, por ejemplo, `Persona persona = new Persona("Juan");`.

En este ejemplo, se crea un objeto `persona` de la clase `Persona`, se asigna un valor al atributo `nombre` y se llama
al método `saludar` para imprimir un mensaje de saludo.

Por defecto la esctura de un atributo es la siguiente:

```java
tipoDeDato nombreDelAtributo;
```

Donde `tipoDeDato` es el tipo de dato del atributo y `nombreDelAtributo` es el nombre que se le asigna al atributo.

> **Nota:** Es importante tener en cuenta que los tipos de datos de los atributos deben ser tipos primitivos o clases
> definidas previamente.

## Métodos en Java

Los métodos de una clase definen el comportamiento de los objetos creados a partir de esa clase. En Java, los métodos
se definen dentro de la clase y siguen la siguiente estructura:

```java
tipoDeRetorno nombreDelMetodo(parametros) {
    // Cuerpo del método
}
```

Dónde:

* `tipoDeRetorno`: es el tipo de dato que devuelve el método. Puede ser un tipo primitivo, un objeto o `void` si el
  método no devuelve ningún valor.
* `nombreDelMetodo`: es el nombre que se le asigna al método.
* `parametros`: son los valores que recibe el método para realizar su tarea.
* `Cuerpo del método`: es el conjunto de instrucciones que realiza el método.

Por ejemplo, el método `saludar` de la clase `Persona` tiene un tipo de retorno `void`, no recibe parámetros y muestra
un mensaje por consola.

## Uso de clases, funciones y atributos

Para utilizar una clase, sus atributos y métodos, se debe crear un objeto de esa clase y acceder a sus atributos y
métodos utilizando la notación de punto `.`. A continuación, se muestra un ejemplo de cómo utilizar la clase `Persona`
definida anteriormente:

```java
class Main {
    public static void main(String[] args) {
        // Crear un objeto de la clase Persona
        Persona persona = new Persona();

        // Asignar un valor al atributo nombre
        persona.nombre = "Juan";

        // Llamar al método saludar
        persona.saludar();
    }
}
```