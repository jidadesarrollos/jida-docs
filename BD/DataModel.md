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
- **protected $resultBD**
- **private $reflector**
- **private $_paginar**
- **private $_paginaConsultada**
- **private $_paginas**
- **protected $filasPagina**
- **protected $_totalRegistros**

Métodos:
---
1. **function __construct($id = FALSE)**: Función constructora. 
2. **private function instanciarTieneUno()**: Instancia las relaciones uno a uno de un objeto. 
3. **private function instanciarTieneMuchos()**
4. **protected function obtenerDataRelaciones()**: Verifica las relaciones declaradas del Objeto. 
5. **private function obtPerteneceAUno()**
6. **private function instanciarRelaciones()**: Define todas las propiedades de relación del objeto instanciado. 
7. **private function obtTieneMuchos()**: Genera la consulta para las relaciones 1 : M del Objeto. 
8. **private function obtTieneUno()**: Genera las consultas para las relaciones 1:1 del Objeto. 
9. **private function obtPertenece()**: Genera las consultas para las relaciones MaN. 
10. **function instanciar($id, $data = [])**: Permite instanciar un objeto ya inicializado. 
11. **private function instanciarObjeto($id, $data = [])**: Inicializa un objeto a partir de Base de Datos. 
12. **function __obtConsultaInstancia($id)**
13. **private function validarRelaciones()**: Verifica las relaciones existentes, Valida las relaciones uno a muchos y muchos a muchos del objeto. Si el objeto está instanciado, obtiene la data de cada relacion basandose en el limite definido en la constante.
14. **private function obtenerTablaBD()**: Identifica el nombre de la tabla de base de datos. 
15. **private function identificarObjetosRelacion()**
16. **private function _identificarObjetosRelacion()**: Verifica que clases son identificadas como objetos.
17. **function __get($propiedad)**: Permite acceder a propiedades privadas o protegidas del objeto instanciado.
18. **function __establecerAtributos($arr)**
19. **private function initBD($manejador = "")**: Inicializa el objeto correspondiente para el manejo de la base de datos.
20. **private function obtenerPropiedadesObjeto()**: Obtiene todas las propiedades públicas de un objeto instanciado.
21. **function join($clase, $campos = "", $data = [], $tipoJoin = "")**: Agrega la union de campos al query.
22. **function in($filtro, $clave = "", $condicion = "and")**: Emula el in de base de datos.
23. **function consultaSola()**
24. **function consulta($campos = "", $nroPaginacion = FALSE)**: Funcion para obtener datos de una tabla.
25. **function query($campos = [], $tabla)**
26. **private function obtenerpk()**: Obtiene el nombre de la clave primaria de la tabla de base de datos.
27. **function __call($rel, $campos)**: Realiza llamado a los objetos de relacion existentes.
28. **function agregar($relacion, $datos)**: Permite registrar una relacion uno a uno del objeto.
29. **function agregarMuchos()**.
30. **function obtener($relacion)**: Permite acceder a las relaciones uno a uno y uno a muchos de un objeto.
31. **private function where($condicion = " and")**: Agrega la clausula where a la consulta.
32. **function filtro($arrayFiltro = [], $arrayOr = [])**: Permite realizar un filtro de la consulta a realizar.
33. **function agrupar($agrupacion)**: Realiza la agrupación de la consulta.
34. **function select($campos = "")**: Alias de metodo Consulta.
35. **function order($order, $type = 'asc')**: Permite ordenar una consulta.
36. **function condicion($cond)**.
37. **function like($arrayFiltro, $condicion = "or", $tipo = 1)**: Permite hacer una consulta like.
38. **function regExp($arrayFiltro)**: Permite hacer una consulta regExp, Funcion que recibe el campo y la expresion regular para consultar. $arrayFiltro contiene el campo a consultar y la expresion regular a utilizar.
39. **function obt($key = "")**: Retorna una matriz como resultado de una consulta realizada.
40. **private function _paginarConsulta($key)**: Convierte una consulta en una consulta paginada.
41. **function dataPaginacion()**: Retorna la data resultante de una consulta paginada, retorna un arreglo con los siguientes keys : filasPagina, registros, pagina, paginas.
42. **function addConsulta()**.
43. **function obtMultiple($keys)**: Retorna el resultado de múltiples consultas, funcional para trabajar con Mysql. Retorna el resultado de múltiples consultas solicitadas.
44. **function obtenerTodo($key = "", $order = "")**: Retorna todos los registros de Base de datos.
45. **function fila()**: Retorna un vector asociativo de un registro obtenido de base de datos.
46. **protected function obtQuery()**: Retorna el query armado.
47. **function salvar($data = "")**: Permite registrar el objeto actual.
48. **function eliminar($arrayDatos = "", $campo = "", $cond = "and")**: Elimina uno o múltiples registros de base de datos.
49. **function obtenerBy($valor, $property = "")**: Permite instanciar el objeto por medio de una propiedad.
50. **function objectAsArray()**: Retorna un arreglo con las propiedades públicas del objeto.
51. **function obtenerPropiedades($relaciones = FALSE)**: Retorna un arreglo con las propiedades públicas del objeto.
52. **function salvarTodo($data, $insertPK = FALSE)**: Inserta múltiples registros en Base de Datos.
53. **private function armarIdsInsertados()**: Retorna los ids generados a partir de una inserción múltiple.
54. **function obtIdsResultados()**.
55. **private function insertar($data = "")**: Crea un nuevo registro único.
56. **private function obtenerCamposQuery($campos = "", $unsetPK = TRUE)**: Obtiene los campos de Base de datos utilizados para realizar una inserción.
57. **private function estructuraInsert($data = [], $insertPK = FALSE)**.
58. **private function modificar()**
59. **function limit($limit = 100, $offset = 0)**: Limita la consulta a base de datos.
60. **private function verificarUnicos($datos = "")**: Valida las restricciones únicas creadas por medio del array único antes de realizar una inserción.
61. **private function obtenerPlural($palabra)**: Devuelve el plural de una palabra.
62. **private function _obtenerSingular($palabra)**
63. **function getResult()**: Retorna el objeto ResultBD obtenido a partir de una consulta a base de datos.
64. **function envolverFiltro()**
65. **protected function guardarRelacion($arrayData)**
66. **function totalRegistros($filtro = FALSE)**: Registra el total de registros de una tabla.
67. **private function debug($data, $string = TRUE, $condicion = FALSE)**
68. **function paginar($pagina)**: Genera una consulta paginada.
69. **private function _establecerPaginacion($nroPagina = 1)**: Activa la configuración para una consulta paginada.
70. **function imprimir($propiedad = "query", $exit = 1)**
71. **function entre($campo, $ini, $fin)**: Utiliza la clausula between de mysql.
72. **function contar($campo = '*', $distinct = FALSE)**: Utiliza la clausula COUNT de mysql.


Métodos obsoletos:
---
1. **function objectAsArray()**: Retorna un arreglo con las propiedades públicas del objeto.
2. **function __call($rel, $campos)**: Realiza llamado a los objetos de relación existentes.
