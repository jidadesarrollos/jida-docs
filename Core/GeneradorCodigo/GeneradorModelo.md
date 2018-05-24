# GeneradorModelo
Clase generadora de modelos.

Sinopsis
---
```php
class GeneradorModelo extends GeneradorObjeto {
 ....
}
```
Parámetros
---
- **private $tabla**

Métodos:
---
1. **public function __construct()**
2. **function obtenerTablas()**
3. **function ubicacion($ubicacion="")**
4. **function generar($tablaBD,$prefijos)**
5. **private function generarDoc()**
6. **private function obtenerMetodos($tablaBD)**
7. **private function definirPropiedadesBD($tablaBD)**
8. **private function  generarDocPropiedad($type,$prop,$comment="")**
