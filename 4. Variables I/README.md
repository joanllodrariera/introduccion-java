# Variables I

Ahora que ya hemos realizado nuestro primer programa pasaremos a ver las variables.

¿Qué son las variables? Las variables son sitios/estructuras donde podremos **almacenar datos** para utilizarlos más adelante.

Para ver como funcionan modificaremos el código que hemos realizado anteriormente para añadir una variable:
```
package com.company;

public class Main {

    public static void main(String[] args) {
        String myFirstVariable;
        myFirstVariable = "Hola mundo variable";
        System.out.println(myFirstVariable);
    }

}
```
Si ejecutamos este programa (con el botón *Run* tal como hicimos en el capítulo 3). Veremos que por pantalla imprime el valor "Hola mundo variable". Pasemos a ver ahora como funciona este programa.

## En primer lugar, tenemos la declaración de una variable


Las variables se declaran del siguiente modo:

* (tipo de la variable) (nombre de la variable);. Por ejemplo, en el programa:
  *    ```String myFirstVariable;```

Veamos primero que es el *tipo de la variable*. El tipo de la variable, indicará el tipo de datos que queremos almacenar (un número, un texto, etc).

Los tipos de las variables podrán ser de dos tipos:
  * Los **tipos primitivos** que son simples almacenes de datos básicos
  * Las **clases** que serán almacenes de datos pero además tendrán funcionalidades extra como métodos

Pasemos a ver algunos de los tipos primitivos más importantes:
* **Enteros**:
  * Nos permitirán almacenar números sin decimales tanto positivos como negativos: -2, -1, 0, 1, 2, etc.
  * Para utilizar una variable de tipo entero (declarado en lenguaje técnico) podemos hacerlo utilizando la palabra *int*, Es decir:
    * int myInt;
* **Carácteres**:
  * Nos permitirán almacenar una letra o un símbolo. Por ejemplo: a, b, c, #, ?, etc.
  * Para utilizar una variable de tipo carácter lo podemos hacer del siguiente modo:
    * char myChar;
* **Booleanos**:
  * Los booleanos son un tipo de variable que solo permiten almacenar dos valores: verdadero (true) o falso (false).
  * Para utilizar una variable de tipo booleano lo podemos hacer del siguiente modo:
    * boolean myBoolean;
* **Decimales**:
  * Las variables de tipo decimal nos permiten almacenar números sin o con decimales: -1.1, 0, 1, 1.3, etc. 
  * Para utilizar una variable de tipo decimal lo podemos hacer del siguiente modo:
      * float myFloat;

Hasta aquí, hemos visto algunos de los tipos primitivos más importantes que tiene Java.

Aparte de los tipos primitivos, como hemos dicho, también tenemos las clases. Las clases pueden ser definidas por cualquier programador (Veremos como hacerlo más adelante). Sin darnos cuenta ya ya hemos utilizado una variable de tipo clase. Esta es la clase String y la hemos utilizado en nuestro programa más arriba en la que hemos declarado la variable:
```
String myFirstVariable
```
Como hemos dicho antes, las clases pueden tener métodos. Por ejemplo, podríamos hacer:
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        String myFirstVariable;  
        myFirstVariable = "Hola mundo variable";  
        System.out.println(myFirstVariable.toUpperCase());  
    }  
  
}
```
Ahora el programa nos habrá impreso el siguiente texto: HOLA MUNDO VARIABLE. Es decir, hemos llamado al método toUpperCase() y este ha hecho que todos los carácteres se muestren en mayúscula. Por ahora, no entraremos más en profundidad en los métodos.

Por otro lado, tenemos el *nombre de la variable*. El nombre de la variable será cualquier nombre que queramos. Las únicas reglas que debe cumplir el nombre son las siguientes: Debe empezar por:
  * Letra
  * El símbolo del dolar: $
  * El símbolo barra baja/guión bajo: _

Como recomendación (normalmente) las variables serán letras en formato *lowerCamelCase*. Es decir, la primera palabra en minúscula y las siguientes en mayúscula. Por ejemplo: valorSensorAireAcondicionado, cocheAzul, etc.

## En segundo lugar, tenemos de un valor a una variable

A las variables les podemos asignar valores del siguiente modo:
* (nombre de la variable) = (valor que queremos asignarle);. Por ejemplo, en el programa:
  *    ```myFirstVariable = "Hola mundo variable";```
  * De este modo, esa variable cogerá el valor "Hola mundo variable".
  * Si nos fijamos en detalle, el operador **=** es el que se encarga de asignar el valor a la variable.

En función del tipo de variable esta aceptará unos valores u otros. Vayamos a ver algunos programas de ejemplo con los tipos primitivos:

### Entero
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        int myFirstIntVariable;  
        myFirstIntVariable = 1;  
        System.out.println(myFirstIntVariable);  
    }  
  
}
```
### Carácteres
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        char myFirstCharacterVariable ;  
        myFirstCharacterVariable = 'a';  
        System.out.println(myFirstCharacterVariable );  
    }  
  
}
```
Si nos fijamos los carácteres deberán ir entre comillas simples **'**carácter**'**

### Booleanos
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        boolean myFirstBooleanVariable ;  
        myFirstBooleanVariable = true;  
        System.out.println(myFirstBooleanVariable );  
    }  
  
}
```
### Decimales

```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        float myFirstDecimalVariable;  
        myFirstDecimalVariable = 1.3;
        System.out.println(myFirstDecimalVariable);  
    }  
  
}
```

Y finalmente, veamos un programa de nuevo con una variable de tipo String

### String

```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        String myFirstVariable;  
        myFirstVariable = "Hola mundo";
        System.out.println(myFirstVariable);  
    }  
  
}
```
Si nos fijamos los String deberán ir entre comillas dobles **"**carácter**"**

Como ejercicio dejo al lector probar y deducir lo que hacen los siguientes programas:

### Programa 1. Declaración y asignación en una misma linea:
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        String myVariable = "Hola mundo";  
        System.out.println(myVariable);  
    }  
  
}
```

### Programa 2. Asignación de una variable múltiples veces I:
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {
        int myVariable;
        myVariable = 1;
        myVariable = 2;  
        System.out.println(myVariable);  
    }  
  
}
```
### Programa 2. Asignación de una variable múltiples veces II:
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {
        int myVariable;
        myVariable = 1; 
        System.out.println(myVariable);
        myVariable = 2;  
        System.out.println(myVariable);  
    }  
  
}
```