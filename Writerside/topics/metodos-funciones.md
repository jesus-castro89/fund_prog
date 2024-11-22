# Métodos y Funciones en Java

En Java, los métodos y funciones son bloques de código que realizan una tarea específica. Los métodos son similares a
las funciones en otros lenguajes de programación y se utilizan para dividir un programa en partes más pequeñas y
manejables. En este artículo, aprenderás cómo definir y utilizar métodos y funciones en Java.

## Diferencias entre Métodos y Funciones

En Java, los términos "método" y "función" se utilizan de manera intercambiable para referirse a bloques de código que
realizan una tarea específica. Sin embargo, en otros lenguajes de programación, como C o C++, existe una distinción
importante entre los dos términos:

* **Métodos**: Los métodos son funciones que están asociadas a una clase o un objeto en particular. En Java, todos los
  métodos deben estar definidos dentro de una clase y pueden acceder a los campos (variables) de la clase.
* **Funciones**: Las funciones son bloques de código independientes que pueden ser invocados desde cualquier parte del
  programa. En lenguajes como C o C++, las funciones pueden ser definidas fuera de cualquier clase.

## Definición de Métodos en Java

En Java, los métodos se definen utilizando la siguiente sintaxis:

```java
public tipo_de_retorno nombre_del_metodo(parametros) {
    // Cuerpo del método
}
```

Donde:

* `public`: Modificador de acceso que indica que el método es accesible desde cualquier parte del programa.
* `tipo_de_retorno`: Tipo de dato que devuelve el método al
* `nombre_del_metodo`: Nombre que identifica al método.
* `parametros`: Lista de parámetros que recibe el método (opcional).
* `Cuerpo del método`: Bloque de código que define las acciones que realiza el método.

A continuación, se muestra un ejemplo de un método en Java que suma dos números:

```java
public class Sumador {
   
    public int sumar(int a, int b) {
        return a + b;
    }
}
```

En este ejemplo, el método `sumar` recibe dos parámetros de tipo `int` (`a` y `b`) y devuelve la suma de los dos
números. Y para poder utilizar este método, debemos crear una instancia de la clase `Sumador` y llamar al método
`sumar`, ya que es un método de instancia.

```java
public class Main {
    public static void main(String[] args) {
        Sumador sumador = new Sumador();
        int resultado = sumador.sumar(5, 3);
        System.out.println("El resultado de la suma es: " + resultado);
    }
}
```

En este ejemplo, creamos una instancia de la clase `Sumador` llamada `sumador` y utilizamos el método `sumar` para
sumar los números 5 y 3. El resultado de la suma se almacena en la variable `resultado` y se imprime en la consola.

## Funciones en Java

Si colocamos la palabra `static` antes de la declaración de un método, este se convierte en un método estático o
función. Los métodos estáticos pueden ser invocados sin necesidad de crear una instancia de la clase a la que
pertenecen.

A continuación, se muestra un ejemplo de una función en Java que calcula el área de un círculo:

```java
public class Circulo {
   
    public static double calcularArea(double radio) {
        return Math.PI * radio * radio;
    }
}
```

En este ejemplo, el método `calcularArea` es un método estático que recibe un parámetro de tipo `double` (`radio`) y
devuelve el área del círculo. Para utilizar este método, no es necesario crear una instancia de la clase `Circulo`, ya
que es un método estático.

```java
public class Main {
    public static void main(String[] args) {
        double radio = 5.0;
        double area = Circulo.calcularArea(radio);
        System.out.println("El área del círculo es: " + area);
    }
}
```

En este ejemplo, calculamos el área de un círculo con radio 5 utilizando el método estático `calcularArea` de la clase
`Circulo`. El resultado se almacena en la variable `area` y se imprime en la consola.

## Conclusión

En Java, los métodos y funciones son bloques de código que realizan una tarea específica. Los métodos están asociados a
una clase o un objeto en particular, mientras que las funciones son bloques de código independientes. Al definir y
utilizar métodos y funciones en Java, puedes dividir tu programa en partes más pequeñas y manejables, lo que facilita
el desarrollo y mantenimiento del software.