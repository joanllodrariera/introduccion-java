# 3. Primer programa

Una vez instalado todo el entorno y creado el proyecto podemos ejecutar nuestro primer programa.

Para ejecutar el programa haremos click en el botón *Run*: **(Acordemonos de este paso porque lo utilizaremos una y otra vez)**
* ![Run](https://raw.githubusercontent.com/joanllodrariera/introduccion-java/main/3.%20Primer%20programa/resources/images/1%20Run.png)

Tras un rato de paciencia el programa se habrá ejecutado. Una vez ejecutado nos aparecerá una **consola** en la que veremos el resultado de la ejecución:
* ![Result](https://raw.githubusercontent.com/joanllodrariera/introduccion-java/main/3.%20Primer%20programa/resources/images/2%20Result.png)

Esta consola si todo ha ido bien mostrará el mensaje *Process finished with exit code 0*. Esto básicamente indica que la ejecución ha sido correcta y no ha habido errores.

Llegados a este punto podemos **DAR SALTOS DE ALEGRIA!** Porque acabamos de **ejecutar** nuestro primer programa!

Ahora que sabemos ejecutar un programa con el botón **Run**. Es hora de crear nuestro propio programa.

Para ello reemplazaremos el texto *// write your code here* por el texto *System.out.println("Hola mundo");*

Se puede ver el programa completo en el siguiente enlace: https://github.com/joanllodrariera/introduccion-java/blob/main/3.%20Primer%20programa/resources/code/Main.java


Una vez hecho esto (**y habiendo guardado los cambios**), volveremos a ejecutar el programa con el botón **Run**. Esta vez el resultado en la **consola** debería ser el siguiente:
* ![Result hello world](https://raw.githubusercontent.com/joanllodrariera/introduccion-java/main/3.%20Primer%20programa/resources/images/3%20Result%20hello%20world.png)

Llegados a este segundo punto podemos **GRITAR! Y DAR SALTOS DE ALEGRIA!** Porque acabamos de **escribir** nuestro primer programa!

Como podemos ver el resultado es que el ordenador ha escrito el texto: "Hola mundo". No es gran cosa pero para haberlo hecho en unos minutos no esta nada mal!

Si pasamos a ver el detalle del programa. Podemos ver las siguientes partes:
1. El nombre del paquete:
   * package com.company;
   * Los paquetes nos sirven para organizar nuestros programas. Pensemos en un paquete como en un sitio donde agruparemos cosas que tienen relación entre ellas. Por ejemplo, podríamos tener un paquete "utilidades de cocina" y otro distinto "utilidades de mecánica".
2. El nombre de la clase:
   * public class Main
   * Antes hemos dicho que los paquetes agrupaban cosas que tenían relación entre ellas. En el caso de Java estas cosas (entre otras que veremos más adelante) son las clases. Podemos pensar en una clase en algo que hace una función específica. Por ejemplo, dentro del paquete "utilidades de cocina" podríamos tener una clase llamada "horno" que tendría la función de cocinar alimentos.
3. El método main:
   * public static void main(String[] args) { System.out.println("Hola mundo"); }
   * Los métodos son los sitios donde pondremos las instrucciones que queremos que ejecute el ordenador. En nuestro caso le estamos diciendo: System.out.println("Hola mundo");. Que quiere decir: Escríbeme en la pantalla "Hola mundo". Y tal como hemos podido comprobar el ordenador nos ha hecho caso! Por ahora no entraremos en detalle de lo que es System.out.println solo diremos que es otro método que utilizaremos para escribir en la pantalla.
   * Otra cosa a mencionar de nuestro método es que en este caso se trata de un método especial: El método "main". Dicho método, en Java tiene la particularidad que será el primero que se ejecutará siempre. No obstante y como hemos visto, desde el método main podremos llamar a otros métodos (como en este caso que hemos llamado al método println).

**Hasta aquí nuestro primer programa!**