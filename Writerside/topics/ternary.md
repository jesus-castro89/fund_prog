# El Operador Ternario

El operador ternario es una forma abreviada de escribir una sentencia `if` en una sola línea. La sintaxis es la
siguiente:

```c++
condicion ? expresion1 : expresion2;
```

Donde `condicion` es una expresión que se evalúa a verdadero o falso, `expresion1` es el valor que se asigna si la
condición es verdadera y `expresion2` es el valor que se asigna si la condición es falsa.

Por ejemplo, el siguiente código:

```c++
int x = 5;
int y = (x > 0) ? 1 : -1;
// Cuando en modo if seria:
// int y;
// if (x > 0) 
//     y = 1;
// else
//     y = -1;    
```

Asigna el valor 1 a `y` si `x` es mayor que 0, y -1 en caso contrario.

El operador ternario es muy útil para asignar valores a variables en función de una condición, pero no se debe abusar
de él, ya que puede hacer que el código sea menos legible. En general, se recomienda usarlo solo para expresiones
simples.

## Ejercicios

1. Escriba un programa que lea un número entero e imprima si es par o impar.
2. Escriba un programa que lea dos números enteros e imprima el mayor de ellos.
3. Escriba un programa que lea tres números enteros e imprima el mayor de ellos.