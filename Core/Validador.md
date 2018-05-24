# Validador
Clase genérica para validaciones del framework.

Sinopsis
---
```php
class Validador {
 ....
}
```
Parámetros
---
- **protected $mensajeError**: Guarda el String del mensaje de Error.
- **protected $validacion**: TRUE si se cumple la valicación, FALSE caso contrario.
- **protected $dataValidaciones**: Arreglo asociativo con validaciones y mensajes de error.
- **private $errors**: Arreglo que registra los errores.

Métodos:
---
1. **function __construct($cadena = "", $validacion = "", $datosValidacion = [])**: Método constructor.
2. **function validarCadena($nombreValidacion, $datosValidacion)**
3. **protected function obtenerMensajeError($validacion, $datos)**: Obtiene el mensaje de error configurado para el campo.
4. **static function validar($validacion, $cadena, $mensaje = FALSE)**: Permite realizar validaciones a una cadena.
5. **public function getValidacion()**: Devuelve el valor del resultado de la valicación efectuada.
6. **public function getErrors()**
