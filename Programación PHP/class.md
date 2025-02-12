# class 

  **_plantillas o esquemas que se utilizan para crear objetos. Una clase define las propiedades (variables o atributos) y métodos (funciones) que tendrá un objeto_**

**Las clases PHP estructuran el código en módulos lógicos independientes, cada uno de los cuales tiene propiedades y métodos específicos. Esto favorece su reutilización y la gestión en proyectos de gran envergadura.
 La definición básica de una clase comienza con la palabra reservada class, seguida de un nombre de clase, y continuando con un par de llaves que encierran las definiciones de las propiedades y métodos pertenecientes a dicha clase.**
#### 1 class  {collapsible="true"}



```php

<?php
class ClaseSencilla
{
    // Declaración de una propiedad
    // variable que pude representar la propiedad de un objeto como podria se color,forma, tamaño
    public $var = 'un valor predeterminado';

    // Declaración de un método
    // Bloque de codigo que contiene una serie de instrucones
    public function mostrarVar() {
        echo $this->var;
    }
}
?>

```
#### 2 class  {collapsible="true"}
```php

<?php

class Opbasic
{ 
    function Suma($v1,$v2)
    {
      return $v1+$v2;
    }

    function Resta($v1,$v2)
    {
        return $v1-$v2;
    }
   

}

class ObComp
{

    function Mult($v1,$v2){

    }

}

$x = new Opbasic();
$y = new ObComp();

echo $x->Suma(3,2);
echo "<br>";
echo $x->Resta(3,2);

```
#### 3 class  {collapsible="true"}

```php

<?php
class A
{
    function foo()
    {
        if (isset($this)) {
            echo '$this está definida (';
            echo get_class($this);
            echo ")\n";
        } else {
            echo "\$this no está definida.\n";
        }
    }
}

class B
{
    function bar()
    {
        A::foo();
    }
}

$a = new A();
$a->foo();

A::foo();

$b = new B();
$b->bar();

B::bar();
?>
```