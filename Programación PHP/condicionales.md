# condicionales

Condicionales If else

la condicional if se utiliza para comparar resultados y realizar toma de deciciones
Ejemplo:

si 1=1 entonces son iguales
si 1≠1 entonces son diferentes
Por lo anterior se deduce que si se cumple la condición pasa y se debe de hacer algo

      si 1=1 entonces
        se cumple la condición
         aquí va el código cuando se cumple la condición
      fin // aquí termina el código 
Ahora como quedaría lo anterior en lenguaje php ?
```php
    <?php
      
      if (1==1)
      {
          se cumple la condición
       }
	   
``` 

por otro lado tenemos que si se cumple la codicio se realiza una tarea x,
y si no se cumple podemos ejecutar una tarea y de acuerdo a esto podemos
ejemplificar como:

    si 2=2 entonces
      tarea x;
    si no entonces
       tarea y;
    fin

Como queda esto en php ?

```php
   if (2==2) //si
   { 
      tarea x;
   }else{ // si no
       tarea y;
   } // fin
   	 
```

switch

```php
    switch ($i) {
      case 0:
         echo "$i igual 0";
        break;
      case 1:
         echo "$i igual 1";
       break;
      case 2:
       echo "$i igual 2";
      break;
    }

```