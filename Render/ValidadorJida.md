# ValidadorJida
Validador de Controles de formulario.

Sinopsis
---
```php
class ValidadorJida extends \Jida\Core\Validador {
 ....
}
```
Parámetros
---
- **private $validaciones**
- **private $valorCampo**
- **private $expresiones**
- **private $error**
- **private $campo**
- **private $mensajesDefecto**
- **private $opciones**

Métodos:
---
1. **function __construct($campo, $validaciones, $opciones = "")**: Constructor de la clase Validador Jida.
2. **private function getDataValidaciones()**: Devuelve el arreglo con todas las validaciones existentes y los mensajes por defecto para cada una de ellas.
3. **function validarCadena($nombreValidacion, $datosValidacion)**: Verifica si una cadena tiene el formato requerido.
4. **function validarCampo(&$campo)**: Función controladora que verifica las validaciones.
5. **private function validarCampoLleno()**: Valida un campo obligatorio.
6. **private function validarTiny($validacion, $detalle)**: Valida un campo del editor de texto TINY.
7. **private function validarDocumentacion($validacion, $detalle)**
8. **private function validarTelefono($validacion, $detalle)**
9. **private function igualdad($validacion, $detalle)**
10. **private function validarContrasenia($validacion, $detalle)**: Valida un campo de contraseña segura.
11. **private function validarFecha($validacion, $detalle)**: Valida un campo con formato fecha.
12. **private function validarFechaHora($validacion, $detalle)**: Valida un campo con formato fecha.
13. **private function limiteCaracteres($validacion, $detalle)**

Parámetros obsoletos:
---
- **private $validacionesDefault**
