# 8. Operadores III lógicos

Los operadores lógicos son aquellos del tipo **y** (&&), **o** (||) y **no** (!). Estos operadores operarán con boolean y devolverán como resultado un boolean. Un ejemplo, de uso de este tipo de operador sería para responder a preguntas del tipo: ¿Es adulto y puede conducir?

## &&

Este operador devolverá true siempre y cuando los dos valores/variables a izquierda y derecha sean true. Podemos resumir el operador del siguiente modo:

* true && true dará como resultado true
* true && false dará como resultado false
* false && true dará como resultado false
* false && false dará como resultado false

## ||

Este operador devolverá true si uno de los o los dos valores/variables a izquierda y derecha son true. Podemos resumir el operador del siguiente modo:

* true || true dará como resultado true
* true || false dará como resultado true
* false || true dará como resultado true
* false || false dará como resultado false

## !

Este operador dará como resultado el valor contrario al que le pasemos. Es decir:

* !true dará como resultado false
* !false dará como resultado true

Una vez vistos los operadores lógicos pasemos a ver que hace uso de ellos junto a los operadores relacionales:

```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
  
        // Supuestas variables de una persona:  
        int age = 30; // Edad  
        boolean hasDrivingLicense = true; // Carnet de conducir
        boolean isDrunk = false; // Ha bebido alcohol  
  
        // Datos de edad para que una persona sea considerada adulta:
        int ageAdult = 18;  
  
        // Cálculo e impresión por pantalla de si esa persona puede conducir:
        boolean canDrive = age >= ageAdult && hasDrivingLicense && !isDrunk;  
        System.out.println("¿Puede conducir? " + canDrive);  
    }  
  
}
```
No lo he comentado antes pero las lineas que empiezan por // son comentarios que Java ignorará. Nos vendrán muy bien para comentar nuestro código.

Con estos últimos operadores ya hemos terminado! Ahora pasaremos a ver los controles de flujo.