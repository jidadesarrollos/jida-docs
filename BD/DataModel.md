# DataModel
Clase Padre de modelos.

Sinopsis
---
```php
class DataModel {
 ....
}
```
Parámetros
---
- **protected $debug**
- **protected $tablaBD**
- **protected $esquema**
- **protected $manejadorBD**
- **private $consultaMultiple**
- **private $join**
- **private $usoLimit**
- **private $_ce**
- **private $condicion**
- **private $_limit**
- **protected $prefijoBD**
- **protected $fecha_creacion**
- **protected $fecha_modificacion**
- **protected $nivelORM**
- **protected $prefijoRelacional**
- **protected $unico**
- **protected $registroMomentoGuardado**
- **protected $registroUser**
- **protected $tieneUno**
- **protected $tieneMuchos**
- **protected $pertenece**
- **protected $perteneceAUno**
- **private $query**
- **private $nivelActualORM**
- **protected $pk**
- **private $tablaQuery**
- **protected $bd**
- **protected $configuracionBD**
- **private $propiedades**
- **private $consultaRelaciones**
- **private $propiedadesObjetos**
- **private $usoWhere**
- **protected $usoBD**
- **private $_groupBy**
- **private $order**
- **private $totalInserciones**
- **private $idsResultantes**
- **private $valoresIniciales**
- **private $_clase**
- **private $resultBD**
- **private $reflector**
- **private $_paginar**
- **private $_paginaConsultada**
- **private $_paginas**
- **protected $filasPagina**
- **protected $_totalRegistros**

Métodos:
---
1. **function __construct($id = FALSE)**: Función constructora. 


Métodos obsoletos:
---
1. **function objectAsArray()**: Retorna un arreglo con las propiedades públicas del objeto.
2. **function __call($rel, $campos)**: Realiza llamado a los objetos de relación existentes.
