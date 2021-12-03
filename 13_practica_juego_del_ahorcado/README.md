
# Práctica: Juego del ahorcado

## Introducción

Llegados a este punto, hemos aprendido muchas cosas pero no las hemos puesto en práctica.

En este capítulo, vamos a realizar nuestra primera práctica: El juego del ahorcado. Para quien no lo conozca, las reglas de este juego son muy sencillas:

 1. Un jugador introduce una palabra
 2. Otro jugador introduce letras una a una hasta que se queda sin intentos (y pierde) o adivina la palabra (y gana).
 
## Utilidades adicionales

Aparte de todas las cosas que hemos visto hasta ahora. Vamos a necesitar una serie de métodos para poder programar nuestro primer juego. Estos son:

### String charAt(N)
Nos permitirá saber el carácter que contiene un String en la posición N. Por ejemplo, el siguiente código imprimirá la letra *a*:
```
String myString = "abc";
System.out.println(myString.charAt(0));
```

### String lenght()
Nos permitirá saber la longitud de un String. Por ejemplo el siguiente código imprimirá el número *3*:
```
String myString = "abc";
System.out.println(myString.lenght());
```
### int ++
Nos permitirá aumentar en uno un entero . Por ejemplo, el siguiente código imprimirá *2*:
```
int myInt = 1;
myInt++
System.out.println(myInt);
```
Sería lo mismo que:
```
int myInt = 1;
myInt = myInt + 1;
System.out.println(myInt);
```
Todos estos métodos y más los podréis encontrar en la documentación de Java: https://docs.oracle.com/javase/7/docs/api/java/lang/String.html

## Solución

Con la anterior información ya deberíais poder programar el juego. No obstante, la primera vez puede ser muy complicado, por lo que vamos a ver la solución paso a paso:

### Paso 1: El jugador 1 introduce la palabra a adivinar
En este caso le mostraremos un mensaje al jugador y leeremos la palabra:
```
System.out.println("Player 1! Please, introduce the word to guess:");  
BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));  
String wordToGuess = bufferedReader.readLine();
```
### Paso 2: Configuramos el juego

Añadimos una serie de variables que vamos a utilizar durante el juego:

Para almacenar el número de intentos del jugador 2:
```
int currentAttempt = 0;  
```
Para almacenar el número máximo de intentos que tendrá el jugador 2:
```
int maximumNumberOfAttempts = 6; 
```
Para almacenar el número de letras que ha adivinado el jugador 2:
```
int numberOfGuessedCharacters = 0; 
```
Para almacenar el número de letras de la palabra:
```
int numberOfWordCharacters = wordToGuess.length();
```
### Paso 2: Bucle del juego
Con las variables anteriores tenemos que ver hasta cuando podrá jugar el jugador 2. Y esto será hasta que se cuplan las siguientes dos condiciones:
* Que el jugador 2 tenga todavía intentos. Es decir: ```currentAttempt < maximumNumberOfAttempts```
* Que el jugador 2 todavía no haya adivinado todas las letras. Es decir: ```numberOfGuessedCharacters < numberOfWordCharacters```

Con estos datos, podemos añadir el siguiente bucle de juego:
```
while (currentAttempt < maximumNumberOfAttempts
&& numberOfGuessedCharacters < numberOfWordCharacters)
{
// El Código del paso 3: buble del juego irá aquí dentro
}
```
Una vez dentro del bucle del juego tendremos que ver como juega el jugador 2. Esto lo podemos dividir en 3 pasos:

#### Paso 2.1: El jugador introduce una letra
Le mostraremos un mensaje al jugador y le pediremos que introduzca una letra:
```
System.out.println("Player 2! Please, introduce the letter to guess:");  
String guessedLine = bufferedReader.readLine();  
char guessedCharacter = guessedLine.charAt(0);
```
#### Paso 2.2: Comprobamos cuantas veces la letra aparece en la palabra introducida por el jugador 1 *wordToGuess*
Por cada vez que aparezca la letra añadiremos una a la variable *numberOfGuessedCharacters*:
```
for(int i = 0; i < wordToGuess.length(); i++) {  
    if(guessedCharacter == wordToGuess.charAt(i)) {  
        numberOfGuessedCharacters++;  
    }  
}
```
#### Paso 2.3: Por último, añadiremos uno al número de intentos del jugador 2 *currentAttempt*
```
currentAttempt++;
```
De este modo, el bucle del juego para el jugador 2 quedará del siguiente modo:

```
while(currentAttempt < maximumNumberOfAttempts && numberOfGuessedCharacters < numberOfWordCharacters) {  
    // Receive the player 2 input:  
  System.out.println("Player 2! Please, introduce the letter to guess:");  
    String guessedLine = bufferedReader.readLine();  
    char guessedCharacter = guessedLine.charAt(0);  
    // Check how many times the character is in the wordToGuess:  
  for(int i = 0; i < wordToGuess.length(); i++) {  
        if(guessedCharacter == wordToGuess.charAt(i)) {  
            numberOfGuessedCharacters++;  
        }  
    }  
    // Increase the number of attemps:  
  currentAttempt++;  
}
```
### Paso 3: Mostrar los resultados

Una vez que el juego haya terminado tendremos que mostrar los resultados.

Para ello podemos ver si el jugador 2 ha acertado todas las letras de la palabra o no del siguiente modo:

```
if(numberOfGuessedCharacters == numberOfWordCharacters) {  
    System.out.println("Player 2 wins! The player guessed the word!");  
} else {  
    System.out.println("Player 1 wins! Player 2 has no clue of your word!!");  
}
```
## Juego finalizado

Con todo lo anterior el juego finalizado quedaría así:
```
package com.company;  
  
import java.io.BufferedReader;  
import java.io.IOException;  
import java.io.InputStreamReader;  
  
public class Main {  
  
    public static void main(String[] args) throws IOException {  
        // Player 1: introduction of the word to guess:
        System.out.println("Player 1! Please, introduce the word to guess:");  
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));  
        String wordToGuess = bufferedReader.readLine();  
        // Player 2: Game:  
        // Game configuration
        int currentAttempt = 0;  
        int maximumNumberOfAttempts = 6;  
        int numberOfGuessedCharacters = 0;  
        int numberOfWordCharacters = wordToGuess.length();  
        // Game loop:  
        while(currentAttempt < maximumNumberOfAttempts && numberOfGuessedCharacters < numberOfWordCharacters) {  
            // Receive the player 2 input:
            System.out.println("Player 2! Please, introduce the letter to guess:");  
            String guessedLine = bufferedReader.readLine();  
            char guessedCharacter = guessedLine.charAt(0);  
            // Check how many times the character is in the wordToGuess:
            for(int i = 0; i < wordToGuess.length(); i++) {  
                if(guessedCharacter == wordToGuess.charAt(i)) {  
                    numberOfGuessedCharacters++;  
                }  
            }  
            // Increase the number of attemps:
            currentAttempt++;  
        }  
        // Show game result:
        if(numberOfGuessedCharacters == numberOfWordCharacters) {  
            System.out.println("Player 2 wins! The player guessed the word!");  
        } else {  
            System.out.println("Player 1 wins! Player 2 has no clue of your word!!");  
        }  
    }  
  
}
```

## Retos adicionales

Hasta aquí hemos realizado un juego del ahorcado funcional. Pero propongo al usuario los siguientes retos:

 1. Corregir el error que hace que el usuario gane si introduce la misma letra correcta varias veces.
 2. Mostrar un error al usuario si el jugador 2 introduce más de una letra en *guessedLine* y que esto provoque que ese sea un intento no valido para el jugador 2

Hasta aquí la primera parte de este curso. Nos vemos en la segunda parte!
