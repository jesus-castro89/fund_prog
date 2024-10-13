# 8. Contenido en Java

## Introducción

Para nuestro proyecto deberemos de crear lo siguiente en el archivo `Main.java`:

* **Suite**: La forma de las cartas.
    * Será un tipo enumerado.
* **Figure**: Las figuras de las cartas.
    * Será un tipo enumerado.
* **Card**: Las cartas en sí.
    * Será una clase.
* **Deck**: La baraja de cartas.
    * Será una clase.
* **Player**: Los jugadores.
    * Será una clase.
* **Blackjack**: El juego de Blackjack.
    * Será una clase.

## Suite

Nuestro enum deberá de contar con los siguientes atributos:

* **suiteName**: El nombre de la suite.
* **suiteSymbol**: El símbolo de la suite.

```java
enum Suite {
    HEARTS("Corazones", "♥");

    final String suiteName;
    final String suiteSymbol;

    Suite(String suiteName, String suiteSymbol) {
        this.suiteName = suiteName;
        this.suiteSymbol = suiteSymbol;
    }

    String getSuiteName() {
        return suiteName;
    }

    String getSuiteSymbol() {
        return suiteSymbol;
    }
}
```

En este caso, se ha declarado un enum `Suite` con la constante `HEARTS` que representa la suite de corazones. Se han
añadido los atributos `suiteName` y `suiteSymbol` a la constante `HEARTS`, así como un constructor que inicializa estos
atributos. También se han añadido métodos `getSuiteName()` y `getSuiteSymbol()` para obtener el nombre y el símbolo de
la suite de corazones.