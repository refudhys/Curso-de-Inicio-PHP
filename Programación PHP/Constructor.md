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



Nota: El constructor se define en la sección pública de la clase. Incluso los valores de las propiedades de la clase se establecen mediante constructores.
Tipos de constructores:


Constructor predeterminado: no tiene parámetros, pero los valores al constructor predeterminado se pueden pasar dinámicamente.
Constructor parametrizado: toma los parámetros y también puede pasar diferentes valores a los miembros de datos.
Constructor de copias: Acepta la dirección de los otros objetos como parámetro.
Herencia: Como la herencia es un concepto orientado a objetos, los constructores se heredan de la clase padre a la clase hija derivada de ella. Siempre que la clase hija tenga su propio constructor y destructor, estos se invocan en orden de prioridad o preferencia.
Constructor predeterminado predefinido: al usar la función __construct(), puede definir un constructor.
Nota: En el caso de un constructor predefinido (__construct) y un constructor definido por el usuario en la misma clase, el constructor predefinido se convierte en el constructor mientras que el constructor definido por el usuario se convierte en el método normal.
Programa:

```php
<?PHP
class Tree
{
    function Tree()
    {
        echo "Its a User-defined Constructor of the class Tree";
    }
 
    function __construct()
    {
        echo "Its a Pre-defined Constructor of the class Tree";
    }
}
 
$obj= new Tree();
?>

```

Es un constructor predefinido de la clase Árbol.
Constructor parametrizado: El constructor de la clase acepta argumentos o parámetros.
El operador -> se utiliza para establecer valores para las variables. En el método constructor, puede asignar valores a las variables durante la creación del objeto.
Programa:

```php
<?php
 
class Employee
{ 
     
    Public $name;
 
    Public $position;
 
    function __construct($name,$position)
 
    {
        // This is initializing the class properties
        $this->name=$name;
        $this->position=$position;
 
 
    }     
    function show_details()
    {
        echo $this->name." : ";
        echo "Your position is ".$this->profile."\n";
    }
}
     
$employee_obj= new Employee("Rakesh","developer");
$employee_obj->show_details();
     
$employee2= new Employee("Vikas","Manager");
$employee2->show_details();
 
?>
```
<a href="https://www.geeksforgeeks.org/php-constructors-and-destructors/">Referencia</a>