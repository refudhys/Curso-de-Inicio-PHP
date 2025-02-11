# class 


#### class {collapsible="true"}
La definición básica de una clase comienza con la palabra reservada class, seguida de un nombre de clase, y continuando con un par de llaves que encierran las definiciones de las propiedades y métodos pertenecientes a dicha clase.


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
#### 2 class {collapsible="true"}
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