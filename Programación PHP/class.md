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

    /*
    public $public = 'Public';
    protected $protected = 'Protected';
    private $private = 'Private';
*/

    public function Suma($v1,$v2)
    {
      
       // $val = self::laOperacion($v1,$v2);
       $val = $this->laOperacion($v1,$v2);
      return "Suma= ".$val;
    }

    public function Resta($v1,$v2)
    {
        return $v1-$v2;
    }
   // static
    private  function laOperacion($v1,$v2){
        return $v1+$v2;
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

echo Opbasic::Resta(3,2);


  $i = 1;
        while ($i <= 10):
            echo $i;
            echo "<br>";
            $i++;
        endwhile;
        
        
        $obj = new Opbasic();
echo $obj->public;    // Funciona bien
echo $obj->protected; // Error Fatal
echo $obj->private;   // Error Fatal
        
        
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
### Definición

La palabra reservada ***'static'***
Declarar propiedades o métodos de clases como estáticos los hacen accesibles sin la necesidad de instanciar la clase. Una propiedad declarada como static no puede ser accedida con un objeto de clase instanciado (aunque un método estático sí lo puede hacer).

Por motivos de compatibilidad con PHP 4, si no se utiliza ninguna declaración de visibilidad, se tratará a las propiedades o métodos como si hubiesen sido definidos como public.

Debido a que los métodos estáticos se pueden invocar sin tener creada una instancia del objeto, la seudovariable $this no está disponible dentro de los métodos declarados como estáticos.

La palabra reservada ***self***
Hace referencia a la clase actual y generalmente lo usarías cuando no se genera una instancia de la misma, como cuando usas métodos estáticos:

¿Qué es  $this en PHP?
En PHP, $thisla palabra clave hace referencia al objeto actual de la clase. La $thispalabra clave permite acceder a las propiedades y métodos del objeto actual dentro de la clase mediante el operador de objeto ( ->):

<a href="https://www.phptutorial.net/php-oop/php-this/"></a>