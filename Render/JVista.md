# JVista
Clase para manejo de vistas dinámicas.

Sinopsis
---
```php
class JVista {
 ....
}
```
Parámetros
---
- **private $dataVista**
- **$ordenamientos**
- **$buscador**
- **private $_debug**
- **private $nroFilas**
- **private $_ce**
- **private $paginasMostradas**
- **private $totalPaginas**
- **private $titulos**
- **private $titulosKey**
- **private $contenedorAcciones**
- **private $accionesFila**
- **private $_parametrosGET**
- **$camposOrder**
- **private $configFilaOpciones**
- **private $ejecucion**
- **private $_ordenamientos**
- **private $_tipoOrdenamiento**
- **private $_campoOrdenar**
- **private $titulo**
- **private $_funcionData**
- **private $_parametrosFuncionData**
- **private $clausulas**
- **private $acciones**
- **$controlFila**
- **$funcionNoRegistros**
- **private $parametroPagina**
- **private $usaBD**
- **private $queryString**
- **$analizaURL**
- **private $mensajeNoRegistros**
- **private $htmlPersonalizado**
- **private $filtros**
- **private $tabla**
- **private $campos**
- **private $nameInputLinea**
- **private $configTabla**
- **private $configAcciones**
- **private $configAccionesFila**
- **private $configContenedorAcciones**
- **private $configFiltros**
- **private $configArticleVista**
- **private $configSeccionForm**
- **private $registros**
- **private $totalRegistros**
- **private $paginador**
- **private $paginaActual**
- **private $configPaginador**
- **private $paginaConsulta**
- **private $objeto**
- **private $urlActual**
- **private $idVista**
- **private $data**
- **private $keys**

Métodos:
---
1. **function __construct($ejecucion, $parametros = [], $titulo = "")**: Contructor de Jvista.
2. **private function validarPaginaConsulta()**: Verifica la estructura de la url manejada para la funcionalidad de la vista.
3. **private function establecerValoresDefault()**.
4. **private function realizarConsulta()**.
5. **private function procesarArrayData($data)**: Procesa la informacion para una vista a partir de un arreglo.
6. **private function obtInformacionObjeto($metodo = FALSE)**: Obtiene la información a renderizar desde un objeto dado.
7. **private function _ejecutarFuncionData()**.
8. **private function obtenerNombreCampos()**: obtiene los nombres de los campos consultados a base de datos.
9. **private function obtConsultaPaginada()**: ejecuta la consulta de la vista agregando el limite de registros requeridos.
10. **function render($function = "", $parametrosFuncion = [])**: Retorna la vista renderizada.
11. **private function checkMensajes()**.
12. **private function checkTitulo()**: Renderiza el titulo de la vista.
13. **private function procesarControlFila()**.
14. **private function procesarFormBusqueda()**.
15. **private function procesarAccionesFila()**: Verifica si se agregaron acciones a una fila.
16. **private function _validarPerfilesFila($accionFila)**: Verifica los perfiles que pueden visualizar una opcion de la fila a renderizar.
17. **private function crearTitulos()**: Crea los titulos de la tabla.
18. **private function obtParametrosOrden()**.
19. **private function procesarAcciones()**.
20. **private function crearPaginador()**: Genera el páginador de la vista.
21. **function accionesFila($acciones)**.
22. **function acciones($acciones = FALSE)**: Define acciones generales para la vista.
23. **function tabla()**: Retorna el objeto Table Selector.
24. **private function checkGlobals()**: Verifica si existen arreglos GLobales de configuración para el estilo.
25. **function addFiltros($filtros)**: Permite agregar filtros a la vista.
26. **function renderFiltros()**.
27. **private function urlFiltro($params = [])**: Retorna la url para un filtro de la vista.
28. **function procesarNoRegistros()**.
29. **function obtTotalRegistros()**.
30. **function obtConsulta()**.
31. **static function msj($idVista, $tipo, $msj, $redireccion = "")**: Crea mensajes a mostrar en la vista.
32. **function addMensajeNoRegistros($msj, $cssDiv = [])**: Permite personalizar un mensaje en caso de no haber registros.
33. **function clausula($nombreClausula, $valores)**: Permite agregar clausulas a la consulta realizada por la vista.
34. **function funcionFila($numeroFila, $function)**.
35. **private function procesarURL($params, $print = FALSE)**: Gestiona la url de los enlaces a usar en la página.
36. **private function checkConfig($config = [])**.
37. **function configuracion($configuracion, $valor = "")**: Permite definir valores de configuracion para la vista creada.
38. **private function _obtTemplate($template, $params)**: Renderiza el contenido en plantillas predeterminadas.
39. **protected function _imprimir()**.
40. **private function _procesarParametros()**.
41. **private function _definirKeys($data)**: Arma en un array las keys por las que se construye la tabla.


Métodos obsoletos:
---
1. **function obtenerVista($function = "")**: Renderiza la vista.
