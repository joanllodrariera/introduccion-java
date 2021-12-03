# De repetición

Así como en los dos capítulos anteriores hemos querido ejecutar operaciones de manera condicional ahora vamos a querer ejecutar una operación múltiples veces. Para ello tendremos dos instrucciones (principales) *while* y *for*.

## While

La sintaxis de la instrucción while será la siguiente:
```
while(CONDICIÓN) {
	Código a ejecutar
}
```

Es decir, *while* ejecutará un código hasta que una condición deje de cumplirse. Por ejemplo, este código se ejecutará siempre y cuando que la variable number sea menor a 10:
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        int number = 0;  
        while(number < 10) {  
            System.out.println("Number = " +  number);  
            number = number + 1;  
        }  
    }  
  
}  
```
Por lo tanto el código imprimirá por pantalla:

* Number = 0
* Number = 1
* Number = 2
* Number = 3
* Number = 4
* Number = 5
* Number = 6
* Number = 7
* Number = 8
* Number = 9

## For

La sintaxis de la instrucción while será la siguiente:
```
for(CÓDIGO INICIAL; CONDICIÓN; CÓDIGO REPETICIÓN) {
	Código a ejecutar
}
```
Donde:
* CÓDIGO INICIAL: Se ejecutará una única vez antes de la ejecución del *for*.
* CÓNDICIÓN: Será la condición para que el *for* siga ejecutandose.
* CÓDIGO REPETICIÓN: Se ejecutará después del *Código a ejecutar* en cada una de las iteraciones.

Como ejemplo, el mismo código que hemos visto antes con el *while*, con el *for* quedaría así:

```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        for(int number = 0; number < 10; number = number + 1) {  
            System.out.println("Number = " +  number);  
        }  
    }  
  
}
```
