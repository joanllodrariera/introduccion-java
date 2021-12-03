# Operadores I aritméticos

Cuando vimos las variables pudimos experimentar como declararlas y como darles un valor. Además de eso Java y la mayoría de lenguajes de programación nos permiten realizar operaciones sobre las variables. En el caso de Java podemos hacer las siguientes operaciones aritméticas (entre otras):

## Suma:

Para sumar deberemos utilizar el símbolo **+**:
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        int result = 2 + 3;  
        System.out.println(result);  
    }  
  
}
```
Una vez ejecutado el código la variable result tendrá el valor 5.

## Resta:

Para restar deberemos utilizar el símbolo **-**:

```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        int two = 2;  
        int result = two - 3;  
        System.out.println(result);  
    }  
  
}
```
Una vez ejecutado el código la variable result tendrá el valor -1.

## Multiplicación:

Para multiplicar deberemos utilizar el símbolo **\***:

```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        int two = 2;  
        int three = 3;  
        System.out.println(two * three);  
    }  
  
}
```

Una vez ejecutado el código imprimirá el valor 6.

## División:

Para dividir deberemos utilizar el símbolo **\\**:
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        System.out.println(4 / 2);  
    }  
  
}
```
Una vez ejecutado el código imprimirá el valor 2.

## Módulo:

Para hacer el módulo deberemos utilizar el símbolo **%**:
```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        System.out.println(4 % 2);  
    }  
  
}
```
Una vez ejecutado el código imprimirá el valor 0.
 
 ---
 
Notar que en los diferentes casos hemos utilizado números y variables para ilustrar las diferentes opciones que tenemos. En todos los casos, hemos utilizado int. No obstante, estos operadores aritméticos los podemos utilizar con float o incluso char (cosa que no os recomiendo).

---

Antes de abandonar los operadores aritméticos quiero hacer una mención especial al +. Este símbolo además de permitirnos sumar nos permite concatenar (unir) uno o más String entre ellos y también con tipos de datos (int, float, char, boolean). Como ejemplo, de este operador tenemos el siguiente código:

```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        String myString = "String Value";  
        int number = 3;  
        System.out.println(myString + number);  
    }  
  
}
```
Una vez ejecutado el código imprimirá *String Value 3*.
