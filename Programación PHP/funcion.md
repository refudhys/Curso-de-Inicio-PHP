# funcion

Las funciones son uno de los elementos fundamentales en la programación. Permiten organizar y modularizar el código, lo cual es esencial para crear programas estructurados, reutilizables y más fáciles de mantener. En PHP, como en muchos otros lenguajes de programación, definir funciones es una práctica clave que contribuye significativamente a la eficiencia y legibilidad del código.


## Ejemplo

```php

	function fxsuma()
	{
		$v1=2;
		$v3=3;
		$suma=$v1+$v3;
		//echo $suma;
		return $suma;
	}
	
	$vx=4;
	echo $vx+fxsuma();

```