# GeneradorCodigo
Clase generadora de código.

Sinopsis
---
```php
trait GeneradorCodigo {
 ....
}
```
Métodos:
---
1. **function abrirPHP()**
2. **function docBlock($titulo="",$contenido="",$tags=[])**: Genera un bloque inicial de código.
3. **private function tags($tags)**
4. **function cadena($string)**
5. **function docConstante($nombre,$type,$descripcion)**: Crea la documentacion de una constante.
6. **function constante($nombre,$valor,$type,$descripcion)**
7. **function definirArray($name,$valores=[])**: Crea la estructura de un arreglo.
8. **private function valorArray($key,&$array,$value,$margen=2)**
9. **protected function crearFuncion($nombre,$params=[],$ambito,$contenido="")**
10. **protected function apertura()**
11. **protected function cierre()**
12. **protected function cerrarPHP()**
