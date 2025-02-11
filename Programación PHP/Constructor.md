# Constructores y destructores

PHP permite a los desarrolladores declarar métodos constructores para las clases. Las clases que tienen un método constructor invocan este método en cada objeto recién creado, por lo que es adecuado para cualquier inicialización que pueda necesitar el objeto antes de su uso.



Los constructores son funciones miembro especiales para la configuración inicial de instancias de objetos recién creados a partir de una clase, que es la parte clave del concepto orientado a objetos en PHP5 .
Los constructores son los bloques de construcción básicos que definen el objeto futuro y su naturaleza. Se puede decir que los constructores son los planos para la creación de objetos que proporcionan valores para las funciones miembro y las variables miembro.
Una vez que se inicializa el objeto, se llama automáticamente al constructor. Los destructores son para destruir objetos y se llaman automáticamente al final de la ejecución.
En este artículo, vamos a aprender sobre los conceptos orientados a objetos de constructores y destructores.
Ambos son funciones miembro especiales de cualquier clase con diferentes conceptos pero el mismo nombre excepto que los destructores están precedidos por un operador tilda ~ .
Sintaxis:

 ## __construir():

```php



función __construct()
{
// inicializa el objeto y sus propiedades asignando
//valores
}

```

## __destruct():

```php
función __destruct()
{
// destruir el objeto o limpiar recursos aquí
}
```