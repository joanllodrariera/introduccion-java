
# Interacción con el usuario

Hasta ahora, la única parte que hemos visto para interactuar con el usuario es la impresión de mensajes por pantalla. En este capítulo vamos a ver como el usuario nos puede introducir datos a través de la consola.

Para leer una linea que haya introducido el usuario en la consola lo podemos hacer del siguiente modo:

```
package com.company;  
  
import java.io.BufferedReader;  
import java.io.IOException;  
import java.io.InputStreamReader;  
  
package com.company;  
  
import java.io.BufferedReader;  
import java.io.IOException;  
import java.io.InputStreamReader;  
  
public class Main {  
  
    public static void main(String[] args) throws IOException {  
        System.out.println("Write something and press enter: ");  
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));  
        String line = bufferedReader.readLine();  
        System.out.println("You entered the line: " + line);  
    }  
  
}
```

En este caso, el código:

 1. Nos mostrará un mensaje que nos indica que debemos introducir un texto ```Write something and press enter: ```.
 2. En el mismo sitio donde se pinta este mensaje podemos introducir un texto y luego apretar la tecla intro.
 3. Finalmente se pintará el mensaje ```You entered the line: ``` más el texto que hayamos decidido introducir.

Notar que la lectura de la línea se hace con las siguientes dos lineas de código:

```
 BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
 String line = bufferedReader.readLine();  
```
No obstante, si queremos leer varias líneas bastaría con repetir la segunda instrucción. Es decir:

```
package com.company;  
  
import java.io.BufferedReader;  
import java.io.IOException;  
import java.io.InputStreamReader;  
  
package com.company;  
  
import java.io.BufferedReader;  
import java.io.IOException;  
import java.io.InputStreamReader;  
  
public class Main {  
  
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        System.out.println("Write something and press enter: "); 
        String line = bufferedReader.readLine();  
        System.out.println("First entered line: " + line);  
        System.out.println("Write something and press enter: "); 
        line = bufferedReader.readLine();  
        System.out.println("Second entered line: " + line);  

    }  
  
}
```
Notar que en el anterior código la variable ```line``` ya la tenemos declarada por lo que no hace falta volverla a declarar simplemente asignarle un valor.

En un futuro veremos otros métodos de interacción con el usuario pero para este capítulo esto sería todo!
