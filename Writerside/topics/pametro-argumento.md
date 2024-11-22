# Parámetros y Argumentos

En programación, los términos "parámetro" y "argumento" se utilizan para referirse a los valores que se pasan a una
función o método. Aunque a menudo se utilizan indistintamente, tienen significados ligeramente diferentes.

## Parámetros

Los parámetros son variables declaradas en la definición de una función o método. Estas variables se utilizan para
recibir valores que se pasan a la función cuando se llama. Los parámetros se definen en la firma de la función y
especifican el tipo de datos que se espera recibir.

> Nota: La firma de una función o método incluye su nombre, tipo de retorno y lista de parámetros.

En Java, los parámetros se definen entre paréntesis después del nombre del método. Por ejemplo, en el siguiente método
`sumar`, `a` y `b` son los parámetros:

```java
public int sumar(int a, int b) {
    return a + b;
}
```

En este caso, `int a` y `int b` son los parámetros de tipo `int` que se esperan recibir al llamar al método `sumar`.

## Argumentos

Los argumentos son los valores reales que se pasan a una función o método cuando se llama. Estos valores se asignan a
los parámetros correspondientes en la definición de la función. Por ejemplo, al llamar al método `sumar` con los
argumentos `5` y `3`, se asignan los valores `5` y `3` a los parámetros `a` y `b` respectivamente:

```java
Sumador sumador = new Sumador();
int resultado = sumador.sumar(5, 3);
```

En este caso, `5` y `3` son los argumentos que se pasan al método `sumar` de la instancia `sumador`.

## Diferencias Clave

La diferencia clave entre parámetros y argumentos radica en su contexto y función:

| Parámetros                                                     | Argumentos                                          |
|----------------------------------------------------------------|-----------------------------------------------------|
| Variables declaradas en la definición de una función o método. | Valores reales que se pasan a una función o método. |
| Se utilizan para recibir valores al llamar a la función.       | Se asignan a los parámetros correspondientes.       |
| Se definen en la firma de la función.                          | Se pasan al llamar a la función.                    |

En resumen, los parámetros son variables definidas en la firma de una función o método, mientras que los argumentos son
los valores reales que se pasan a la función al llamarla.