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

## Figure

Nuestro enum deberá de contar con los siguientes atributos:

* **figureName**: El nombre de la figura.
* **figureValue**: El valor de la figura.

```java
enum Figure {
    TWO("2", 2),
    THREE("3", 3),
    // ...
    JACK("J", 10),
    QUEEN("Q", 10),
    KING("K", 10),
    ACE("A", 11);

    final String figureName;
    final int figureValue;

    Figure(String figureName, int figureValue) {
        this.figureName = figureName;
        this.figureValue = figureValue;
    }

    String getFigureName() {
        return figureName;
    }

    int getFigureValue() {
        return figureValue;
    }
}
```

En este caso, se ha declarado un enum `Figure` con las constantes de los primeros valores del 2 al 10, `JACK`, `QUEEN`,
`KING` y `ACE` que representan las figuras de las cartas. Se han añadido los atributos `figureName` y `figureValue` a
cada constante, así como un constructor que inicializa estos atributos. También se han añadido métodos `getFigureName()`
y `getFigureValue()` para obtener el nombre y el valor de cada figura.

## Card

Nuestra clase deberá de contar con los siguientes atributos:

* **suite**: La suite de la carta.
* **figure**: La figura de la carta.

```java
class Card {
    final Suite suite;
    final Figure figure;
    bollean isTaken = false;

    Card(Suite suite, Figure figure) {
        this.suite = suite;
        this.figure = figure;
    }

    String getCardName() {
        return figure.getFigureName() + suite.getSuiteSymbol();
    }

    int getCardValue() {
        return figure.getFigureValue();
    }
}
```

En este caso, se ha declarado una clase `Card` con los atributos `suite` y `figure` que representan la suite y la figura
de la carta. Se ha definido un constructor que inicializa estos atributos y métodos `getCardName()` y `getCardValue()`
para obtener el nombre y el valor de la carta.

Además, deberás declarar dos funciones, una que te permita saber si la carta ha sido tomada y otra que te permita tomar
la carta(poner el atributo `isTaken` en `true`).

## Deck

Nuestra clase deberá de contar con los siguientes atributos:

* **cards**: Las cartas en la baraja.

```java
class Deck{
    Card[] cards;
  
    Deck(){
        cards = new Card[52];
        int index = 0;
        for(Suite suite : Suite.values()){
          for(Figure figure : Figure.values()){
              cards[index] = new Card(suite, figure);
              index++;
          }
        }
    }
}
```

Así mismo deberás declarar las siguientes funciones:

* **shuffle()**: Barajear las cartas.
```java
  void shuffle(){
      Random random = new Random();
      for(int i = 0; i < cards.length; i++){
          int randomIndex = random.nextInt(cards.length);
          Card temp = cards[i];
          cards[i] = cards[randomIndex];
          cards[randomIndex] = temp;
      }
  }
```
* **drawCard(Player player)**: Tomar una carta de la baraja.

## Player

Nuestra clase deberá de contar con los siguientes atributos:

* **name**: El nombre del jugador.
* **cards**: Las cartas del jugador.

```java
class Player{
    String name;
    ArrayList<Card> cards = new ArrayList<>();

    Player(String name){
        this.name = name;
    }
}
```

Así mismo deberás declarar las siguientes funciones:

* **showHand()**: Mostrar las cartas del jugador.
* **getHandScore()**: Obtener la puntuación de las cartas del jugador.

## Blackjack

Nuestra clase deberá de contar con los siguientes atributos:

* **deck**: La baraja de cartas.
* **player**: El jugador.
* **dealer**: El repartidor.

```java
class Blackjack{
    Deck deck;
    Player player;
    Player dealer;

    Blackjack(String playerName){
        deck = new Deck();
        player = new Player(playerName);
        dealer = new Player("Dealer");
    }
}
```

Así mismo deberás declarar las siguientes funciones:

* **startGame()**: Iniciar el juego que repartirá dos cartas a cada jugador.
* **getWinner()**: Obtener al ganador del juego.

## Evidencia y Entregable

Deberás de subir el código de tu proyecto a un repositorio de GitHub y subir el enlace a la plataforma Moodle.