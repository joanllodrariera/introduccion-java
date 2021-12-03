# Condicionales II

En el capítulo anterior hemos visto los condicionales de tipo if.  Java  nos da otro tipo de condicional el *switch*. Este condicional nos servirá para comprobar que valor tiene una variable. Podemos ver un ejemplo de su uso en el siguiente código:

```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        int number = 2;  
        switch (number) {  
            case 1:  
                System.out.println("Number equals 1");  
                break;  
            case 2:  
                System.out.println("Number equals 2");  
                break;  
            case 3:  
                System.out.println("Number equals 3");  
            case 4:  
                System.out.println("Number equals 3 or 4");  
                break;  
            default:  
                System.out.println("Number is not 1, 2, 3 or 4");  
  
        };  
    }  
  
}
```
  

Una de las cosas a tener en cuenta en los switch es la sentencia *break*. Si no la ponemos el código seguirá ejecutando aunque no se cumplan las condiciones. Es decir, en el case 3 podemos ver que no hay break. Esto significará que si la variable number tiene el valor 3 se imprimirá por pantalla *Number equals 3* y *Number equals 3 or 4*.

Otra cosa a tener en cuenta es el default. El default nos permite ejecutar un código cuando el valor pasado en el switch no es ninguno de los valores del case. Por ejemplo, el *Number is not 1, 2, 3 or 4* solo se imprimirá si no es ninguno de los valores.
