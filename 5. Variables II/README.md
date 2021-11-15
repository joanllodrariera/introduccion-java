
# 5. Variables II

Como hemos visto antes, tenemos tipos primitivos que nos permiten guardar datos y clases que nos permiten guardar datos y además tienen métodos.

Pasemos a ver ahora los arrays. **Los arrays son conjuntos de variables de un mismo tipo** y los podemos declarar del siguiente modo:
* Declaración de un array de String:

   * ```String[] textos = {"texto primero", "texto segundo"};```
* Declaración de un array en int:
  * ```int[] enteros = {1, 2, 3, 4, 5};```

Si nos fijamos los distintos valores de los arrays irán **entre corchetes** **{** y **}**.

Una vez tenemos un array declarado podemos ver algunas de sus propiedades:

* ```textos[1]``` Nos devolverá el String de la posición 1. En este caso: "texto segundo".
  *  **Si**, nos devolverá "texto segundo" y no "texto primero" porque los arrays empiezan a contar por el 0 y no por el 1

* Al igual que podemos saber que contiene un array en una posición determinada, podríamos modificar su valor. Para ello, podríamos hacer:
   * ```enteros[2] = 33;```

* Tras esta operación el array quedaría del siguiente modo:
  * {1, 2, 33, 4, 5}

* Finalmente, podemos saber su tamaño mediante la propiedad length del siguiente modo:

  * ```int longitud = enteros.length;```
    * De este modo, la variable longitud contendría el valor de la propiedad length que es un int con el valor 5

Una cosa particular de los arrays es que pueden tener varias dimensiones. Es decir, podríamos tener un array de array (o incluso más). Esto, podemos hacerlo del siguiente modo:

* ```int[][] matriz = {{1, 2}, {3, 4, 5}};```
 
De este modo, una vez declarado el array podríamos acceder a sus propiedades igual que antes:

* ```matriz[0]```; Nos devolvería el array {1, 2}
* ```matriz[1][0];``` Nos devolvería el int 3.
  * Es decir, primero accederíamos al array 1, en este caso {3, 4} y luego al elemento 0 en este caso 3
* ```matriz.length```; Nos devolvería el int 2
* ```matriz[1].lentgh```; Nos devolvería el int 3

Veamos ahora con 3 programas todo lo que acabamos de ver:

### Array de String
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        String[] textos = {"texto primero", "texto segundo"};  
        System.out.println(textos[1]);  
    }  
  
}
```
### Array de enteros
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        int[] enteros = {1, 2, 3, 4, 5};  
        System.out.println(enteros[2]);  
        enteros[2] = 33;  
        System.out.println(enteros[2]);  
        int longitud = enteros.length;  
        System.out.println(longitud);  
    }  
  
}
```
#### Matriz
```
package com.company;  
  
import java.util.Arrays;  
  
public class Main {  
  
    public static void main(String[] args) {  
        int[][] matriz = {{1, 2}, {3, 4, 5}};  
        System.out.println(Arrays.toString(matriz[0]));  
        System.out.println(matriz[1][0]);  
        System.out.println(matriz.length);  
        System.out.println(matriz[1].length);  
    }  
  
}
```
Notar que en este caso para imprimir el array ```matriz[0]``` hemos tenido que utilizar un método especial ```Arrays.toString``` porque si no no se hubiera imprimido como toca por pantalla. Por ahora, no entraremos en detalle en este asunto.

Con los arrays hemos visto ya algunos de los tipos de variables más importantes de  Java. Por ahora será suficiente y pasaremos a la parte de lógica de los programas.