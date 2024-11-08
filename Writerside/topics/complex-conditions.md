# Condiciones complejas en los ciclos

En Java, es posible utilizar condiciones complejas en los ciclos `for`, `while` y `do-while` para controlar el flujo de
ejecución del programa. Estas condiciones pueden incluir múltiples expresiones booleanas y operadores lógicos para
evaluar si se cumple una condición específica.

En esta guía, exploraremos cómo utilizar condiciones complejas en los ciclos `for`, `while` y `do-while` en Java, así
como algunos ejemplos prácticos para comprender mejor su funcionamiento.

## AND y OR Lógicos

En Java, los operadores lógicos `&&` (AND) y `||` (OR) se utilizan para combinar múltiples expresiones booleanas en una
sola condición. Estos operadores permiten evaluar si se cumplen una o ambas condiciones para determinar si una expresión
es verdadera o falsa.

### Operador `&&` (AND)

El operador `&&` (AND) se utiliza para evaluar dos expresiones booleanas y devuelve `true` si ambas expresiones son
verdaderas. Si alguna de las expresiones es falsa, el resultado será `false`.

Por ejemplo:

```java
int x = 5;
int y = 10;

if (x > 0 && y < 15) {
    System.out.println("Ambas condiciones son verdaderas");
}
```

En este ejemplo, la condición `x > 0 && y < 15` se evaluará como verdadera si `x` es mayor que `0` y `y` es menor que
`15`.

### Operador `||` (OR)

El operador `||` (OR) se utiliza para evaluar dos expresiones booleanas y devuelve `true` si al menos una de las
expresiones es verdadera. Si ambas expresiones son falsas, el resultado será `false`.

Por ejemplo:

```java
int x = 5;
int y = 10;

if (x > 0 || y > 15) {
    System.out.println("Al menos una de las condiciones es verdadera");
}
```

En este ejemplo, la condición `x > 0 || y > 15` se evaluará como verdadera si `x` es mayor que `0` o `y` es mayor que
`15`.

## Multiples concatenaciones de condiciones

En Java, es posible combinar múltiples expresiones booleanas utilizando los operadores lógicos `&&` (AND) y `||` (OR)
para crear condiciones complejas en los ciclos `for`, `while` y `do-while`.

Por ejemplo:

```java
for (int i = 0; i < 10; i++) {
    if (i % 2 == 0  && i % 4 == 0 && i < 5) {
        System.out.println("Número par menor que 5: " + i);
    }
}
```

En este ejemplo, la condición `i % 2 == 0 && i % 4 == 0 && i < 5` se evaluará como verdadera si `i` es un número par,
divisible por `4` y menor que `5`.

> **Nota:** Es importante tener en cuenta la precedencia de los operadores lógicos al combinar múltiples expresiones
> booleanas en una sola condición. Se recomienda utilizar paréntesis para agrupar las expresiones y evitar confusiones.

## Ejemplos de Condiciones Complejas

A continuación, se presentan algunos ejemplos de condiciones complejas en los ciclos `for`, `while` y `do-while` en
Java:

### Ciclo `for`

```java
for (int i = 0; i < 10; i++) {
    if (i % 2 == 0 && i < 5) {
        System.out.println("Número par menor que 5: " + i);
    }
}
```

En este ejemplo, se utiliza una condición compleja en un ciclo `for` para imprimir los números pares menores que `5`.

### Ciclo `while`

```java
int i = 0;
while (i < 10 && i % 3 == 0) {
    System.out.println("Número divisible por 3: " + i);
    i++;
}
```

En este ejemplo, se utiliza una condición compleja en un ciclo `while` para imprimir los números divisibles por `3`.

### Ciclo `do-while`

```java
int i = 0;
do {
    if (i % 5 == 0 || i % 7 == 0) {
        System.out.println("Número divisible por 5 o 7: " + i);
    }
    i++;
} while (i < 20);
```

En este ejemplo, se utiliza una condición compleja en un ciclo `do-while` para imprimir los números divisibles por `5`
o `7`.

Con estos ejemplos, esperamos haber aclarado cómo utilizar condiciones complejas en los ciclos `for`, `while` y
`do-while` en Java para controlar el flujo de ejecución del programa de manera efectiva y concisa.