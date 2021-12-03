# Condicionales I

 Si pensamos de nuevo en los programas como recetas para hacer cosas pronto nos daremos cuenta que nos hacen falta algo más que instrucciones una detrás de otra. En según que casos tendremos que tomar decisiones. Por ejemplo, si hacemos una receta para salir de casa seguramente tendremos algo como: *Si llueve entonces coger un paraguas*

Para este tipo de controles, Java nos proporciona los condicionales. Es decir, los condicionales nos permitirán ejecutar un conjunto de instrucciones si se cumple una condición de terminada

## If
Este condicional nos permitirá ejecutar un código solo si se cumple una condición. Por ejemplo, solo imprimemos el texto por pantalla si la variable number es mayor que 5:

```
package com.company;

public class Main {

    public static void main(String[] args) {
        int number = 6;
        if (number > 5) {
            System.out.println("Number greater than 1");
        }
    }

}
```
## Else
Este condicional siempre irá ligado a un if y nos permitirá ejecutar un código si no se cumple la condición del if. Siguiendo el ejemplo anterior y cambiando la variable number por el valor 4, la parte del else se ejecutará si la variable number es menor o igual que 5:

```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        int number = 4;  
        if (number > 5) {  
            System.out.println("Number greater than 5");  
        } else {  
            System.out.println("Number smaller than or equal to 5");  
        }  
    }  
  
}
```

## Else if
      
A veces ocurrirá que vamos a querer ejecutar un código si se cumple una condición pero si no se cumple para ejecutar otro código también queremos ver si se cumple otra condición. Por ejemplo, tendremos el if si number es mayor que 5, el else if si es mayor que 3 y el else para los casos en los que no se cumpla ninguna de las dos condiciones:

```
package com.company;  
  
public class Main {  
  
    public static void main(String[] args) {  
        int number = 4;  
        if (number > 5) {  
            System.out.println("Number greater than 5");  
        } else if (number > 3) {  
            System.out.println("Number between 3 and 5");  
        } else {  
            System.out.println("Number smaller than or equal to 3");  
        }  
    }  
  
}
```

Para finalizar el capítulo notar que:

* Un if puede tener tantos else if como quiera
* Un if solo puede tener un else
* El else deberá ir siempre después de todos los else if
