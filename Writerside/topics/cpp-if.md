# Decisión en C++

La estructura de decisión `if` es una estructura de control que permite evaluar una expresión y ejecutar un bloque de
código si la expresión es verdadera.

## Decisión simple (if) en C++

La estructura `if` en C++ se utiliza para evaluar una expresión y ejecutar un bloque de código si la expresión es
verdadera. La sintaxis de la estructura `if` es la siguiente:

<tabs>
<tab title="Pseudocódigo">

```text
n.- Si [expresión] Entonces
       Inicio
         [Acción]
       Fin
```

</tab>
<tab title="Código C++">

```c++
if (expresion) {
    // Acción si la expresión es verdadera
}
```

</tab>
</tabs>

En el ejemplo siguiente, se muestra cómo utilizar la estructura `if` en C++ para verificar si un número es positivo:

```c++
#include <iostream>

int main() {
    // Declaración de variables
    int numero;
    // Impresión de mensaje y lectura de datos del usuario
    std::cout << "Ingrese un número: ";
    std::cin >> numero;
    // Verificación de si el número es positivo
    if (numero > 0) {
        // Impresión de mensaje si el número es positivo
        std::cout << "El número es positivo." << std::endl;
    }
    // Fin del programa
    return 0;
}
```

## Decisión compuesta (if-else) en C++

La estructura `if-else` en C++ se utiliza para evaluar una expresión y ejecutar un bloque de código si la expresión es
verdadera, y otro bloque de código si la expresión es falsa. La sintaxis de la estructura `if-else` es la siguiente:

<tabs>
<tab title="Pseudocódigo">

```text
n.- Si [expresión] Entonces
       Inicio
         [Acción1]
       Fin
    Sino
       Inicio
         [Acción2]
       Fin
```

</tab>
<tab title="Código C++">

```c++
if (expresion) {
    // Acción si la expresión es verdadera
} else {
    // Acción si la expresión es falsa
}
```

</tab>
</tabs>

En el ejemplo siguiente, se muestra cómo utilizar la estructura `if-else` en C++ para verificar si un número es positivo
o negativo:

```c++
#include <iostream>

int main() {
    // Declaración de variables
    int numero;
    // Impresión de mensaje y lectura de datos del usuario
    std::cout << "Ingrese un número: ";
    std::cin >> numero;
    // Verificación de si el número es positivo o negativo
    if (numero > 0) {
        // Impresión de mensaje si el número es positivo
        std::cout << "El número es positivo." << std::endl;
    } else {
        // Impresión de mensaje si el número es negativo
        std::cout << "El número es negativo." << std::endl;
    }
    // Fin del programa
    return 0;
}
```

## Decisión múltiple (if-else-if) en C++

La estructura `if-else-if` en C++ se utiliza para evaluar múltiples expresiones y ejecutar un bloque de código
dependiendo del resultado de la evaluación de las expresiones. La sintaxis de la estructura `if-else-if` es la
siguiente:

<tabs>
<tab title="Pseudocódigo">

```text
n.- Si [condición1]
       Entonces
          Inicio
            [Acción1]
          Fin
       Si no
          Si [condición2]
             Entonces
                Inicio
                  [Acción2]
                Fin
          Si no
            Si [condición3]
                Entonces
                   Inicio
                       [Acción3]
                   Fin
            Si no
                    Inicio
                        [Acción4]
                    Fin
```

</tab>
<tab title="Código C++">

```c++
if (condicion1) {
    // Acción si la condición1 es verdadera
} else if (condicion2) {
    // Acción si la condición2 es verdadera
} else if (condicion3) {
    // Acción si la condición3 es verdadera
} else {
    // Acción por defecto
}
```

</tab>
</tabs>

En el ejemplo siguiente, se muestra cómo utilizar la estructura `if-else-if` en C++ para verificar si un número es
positivo, negativo o cero:

```c++  
#include <iostream>

int main() {
    // Declaración de variables
    int numero;
    // Impresión de mensaje y lectura de datos del usuario
    std::cout << "Ingrese un número: ";
    std::cin >> numero;
    // Verificación de si el número es positivo, negativo o cero
    if (numero > 0) {
        // Impresión de mensaje si el número es positivo
        std::cout << "El número es positivo." << std::endl;
    } else if (numero < 0) {
        // Impresión de mensaje si el número es negativo
        std::cout << "El número es negativo." << std::endl;
    } else {
        // Impresión de mensaje si el número es cero
        std::cout << "El número es cero." << std::endl;
    }
    // Fin del programa
    return 0;
}
```

En resumen, la estructura de decisión en C++ permite evaluar expresiones y ejecutar bloques de código dependiendo del
resultado de la evaluación de las expresiones. La estructura `if` se utiliza para evaluar una expresión simple, la
estructura `if-else` se utiliza para evaluar una expresión y su negación, y la estructura `if-else-if` se utiliza para
evaluar múltiples expresiones en orden.