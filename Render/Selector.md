# Selector
Clase que permite renderizar combos selectores html con su data respectiva, mediante la aplicación de los métodos de dicha clase.

Sinopsis
---
```php
class Selector {
 ....
}
```
Parámetros
---
- **protected $selector**: Define el selector a crear.
- **protected $id**
- **protected $atributos**
- **protected $envoltorio**
- **$data**: Atributos data para el selector.
- **$class**
- **$style**
- **$attr**: Arreglo para agregar atributos adicionales al selector.
- **$contenido**: Contenido del selector, que puede incluir el innerHTML y otros selectores.
- **$padreInner**: Define si es el selector contenedor del InnerHTML o no.
- **private $nodos**: Nodo de selectores hijos del selector.
- **private $selectorCreado**: Contiene el HTML que se genera al crear el selector.
- **protected $innerHTML**: Contenido especifico a agregar.
- **private $propiedades**. Permite agregar propiedades adicionales al selector.
- **private $_ce**
- **protected $noCierre**

Métodos:
---
1. **function __construct($selector = "", $attr = [])**.
2. **function getSelector($tabs = 0)**: Genera el HTML del selector instanciado.
3. **private function getElementosData()**: Verifica si existen elementos datas que deban ser agregados al selector y los agrega.
4. **private function getAttr()**: Verifica si existen elementos datas que deban ser agregados al selector y los agrega.
5. **public static function crear($selector, $atributos = array(), $content = "", $tabs = 0)**: Genera un selector HTML.
6. **public static function crearBreadCrumb($data, $config = [])**: Crea una lista OL con estilo bootstrap de breadcrumb.
7. **public static function crearLista($css, $content)**: Genera el codigo HTML de una Lista ul.
8. **static function crearUL($content, $attrUL = array(), $attrLi = array())**.
9. **public static function crearInput($value, $valores = "")**: Crea un boton Input, el valor por defecto es un submit, permite modificar los atributos del control a crear por medio de un arreglo asociativo con los datos que se desean.
10. **protected function establecerAtributos($arr, $clase = "")**.
11. **static function addTabs($nums)**.
12. **static function obt($selector)**: Genera una instancia selector y la retorna.
13. **function render()**.
14. **protected function renderContenido()**.
15. **private function selectorCierre()*.
16. **protected function renderAttr()**.
17. **protected function obtClases()**.
18. **function addClass($clase)**.
19. **function removerClass()**.
20. **function data($data = "", $valor = "")**.
21. **function attr($attr, $valor = "")**: Manejo de atributos del Selector permite obtener o asignar valor a un selector.
22. **function innerHTML($innerHTML = "")**.
23. **function addInicio($html)**: Agrega contenido al principio del innerHTML.
24. **function addFinal($html)**: Agrega contenido al final del innerHTML.
25. **function envolver($selector, $attr = [])**: El nuevo selector creado se convertirá en el innerHTML.
26. **function ejecutarFuncion($funcion)**: Ejecuta una funcion del programador sobre el selector.
27. **function obtSelector()**: Retorna el tipo de selector.
