# GeneradorObjeto
Clase generadora de objetos.

Sinopsis
---
```php
class GeneradorObjeto extends BD\DataModel {
 ....
}
```
Parámetros
---
- **protected $clase**
- **protected $propiedades**
- **protected $metodos**
- **protected $traits**
- **protected $interfaces**
- **protected $String**
- **protected $docBlock**
- **protected $extends**
- **private $Directorio**
- **protected $modulo**
- **$extensionClass**
- **protected $ubicacion**
- **protected $nombreObjeto**

Métodos:
---
1. **function __construct()**
2. **function agregarExtend($nombreClase)**
3. **function nombreObjeto($objeto="",$prefijos="")**: Retorna un string con la estructura de nombre de Un Objeto.
4. **protected function crearClase()**: Crea un objeto.
5. **function cerrarClase()**
6. **function definirPropiedades($vars="",$doc="")**: Estructura las variables del objeto.
7. **function definicion($extends="")**
8. **private function addExtends($extends)**
9. **protected function lineaDoc($content)**
10. **function generarDocObjeto($intro,$content="",$tags=[])**
11. **function obtMetodos()**
