# Ejemplo 1

Variables
```php
     <?php
        $mensajes =["Suma ","Multiplicacion","Divicion"]; // Se inicializa la variable y se determina que es un array al colocar el contenido dentro de "[]"
        $Int_1 = 3;  // Se inicializa una variable y se determina que es del tipo INT al asignarle un número
        $Int_2 = 3;
        $Chart = "El Resultado es ";  // Se inicia la variable y se determina que es del tipo String o al signarle caracteres dentro de comillas
        // Esto es una suma
        echo $mensajes[0].$Int_1+$Int_2." <br><br><br>"; // Muestra al cliente la suma
        $Int_2 = 10;
        // Esto es una Resta
        /*
         echo $Chart." Resta ".$Int_1-$Int_2." <br>";
         $Int_2 = 40;
         $Int_1 = 10;
       */
      // Esto es una Multiplicacion
       $Chart = "El es bueno ";
       echo $mensajes[1].$Int_1*$Int_2." <br>";
       // Esto es una Divicion
       $Chart = "El es divicio ";
       echo $mensajes[2].$Int_1/$Int_2." <br>";
```
¿Que es hecho?
Es un comando para la impresión de un texto en pantalla. Es utilizado en las terminales de los sistemas operativos como Unix, GNU/Linux, o MS-DOS; dentro de pequeños programas llamados scripts; y en ciertos lenguajes de programación tales como PHP.