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
- **private $dataVista**.
- **$ordenamientos**.
- **$buscador**.
- **private $_debug**.
- **private $nroFilas**.
- **private $_ce**.
- **private $paginasMostradas**.
- **private $totalPaginas**.
- **private $titulos**.
- **private $titulosKey**.
- **private $contenedorAcciones**.
- **private $accionesFila**.
- **private $_parametrosGET**.
- **$camposOrder**: Permite definir los campos de ordenamiento para cada titulo.
- **private $configFilaOpciones**: Define la configuracion para la fila de opciones de la vista.
- **private $ejecucion;**.
- **private $_ordenamientos;**.
- **private $_tipoOrdenamiento;**: Tipo de ordenamiento, asc o desc.
- **private $_campoOrdenar;**: Nombre del campo con el cual se solicita ordenar la consulta.
- **private $titulo;**.
- **private $_funcionData;**: Funcion pasada por el usuario a ejecutar sobre la data obtenida.
- **private $_parametrosFuncionData;**.
- **private $clausulas;**: Arreglo de clausulas agregadas a la consulta a base de datos implementada por el objeto.
- **private $acciones;**: acciones Permite definir acciones para toda la vista.
- **$controlFila;**: Define si las filas llevaran algún control.
- **$funcionNoRegistros;**.
- **private $parametroPagina;**.
- **private $usaBD;**.
- **private $queryString;**: Parametros pasados como querystring y que son manipulados por el objeto.
- **$analizaURL;**: Define si debe analizarse la URL, si esta en true se tratara la url de conformidad con la estructura de urls usada por JidaFramework.
- **private $mensajeNoRegistros;**: Mensaje a mostrar si no se consigues registros.
- **private $htmlPersonalizado;**.
- **private $filtros;**: definir los objetos de filtro.
- **private $tabla;**: Objeto TablaSelector.
- **private $campos;**.
- **private $nameInputLinea;**.
- **private $configTabla;**.
- **private $configAcciones;**.
- **private $configAccionesFila;**.
- **private $configContenedorAcciones;**.
- **private $configFiltros;**.
- **private $configArticleVista;**.
- **private $configSeccionForm;**.
- **private $registros;**: Data obtenida de la consulta a base de datos.
- **private $totalRegistros;**: Numero total de registros obtenidos.
- **private $paginador;**: objeto ListaSelector como paginador.
- **private $paginaActual;**.
- **private $configPaginador;**.
- **private $paginaConsulta;**: Página donde consulta el paginador para traer nuevos registros.
- **private $objeto;**: var object $objeto Objeto implementado.
- **private $urlActual;**.
- **private $idVista;**.
- **private $data;**.
- **private $keys;**.

Métodos:
---
1. **function __construct()**: En términos generales, éste método se encarga de construir las urls partiendo de la url base, es decir, recibe los parámetros de la url base y desde aquí­ va recibiendo y contruyendo las rutas de las url que contienen las data que conforman las distintas pantallas, por ejemplo: dev.jida.local(url base)/Data(información gestionada desde los controladores)/vista(pantalla, ya sean formularios, tablas, etc.). Adicionalmente, también recibe los parámetros de idiomas, ya que al construir las url, éstas reciben el nombre de la vista con el idioma determinado a mostrar, de igual manera, de trabajar con sesiones de usuario, éste método valida si la sesión está abierta o cerrada para que el usuario, o bien sea dirigido al home principal, o bien a la pantalla de inicio de sesión.
2. **protected function __conf()**: Retorna el objeto de configuración de la aplicación. 
3. **function validarVarGlobales($bug = FALSE)**: Procesa las variables de parametros globales, es decir, valida que la información que viajan por los métodos $_POST, $_GET, $_REQUEST sean correctos, y no generen error.
4. **private function instanciarHelpers()**: Permite procesar información posterior a la ejecucion de metodos accedidos por url.
5. **private function instanciarModelos()**: Permite procesar información mediante los modelos a usar en el controlador.
6. **protected function obtString($valor)**: Convierte el contenido de una variable en codigo aceptado HTML (string).
7. **protected function entero($valor)**: Valida y filtra el contenido de una variable como Entero.
8. **protected function decimal($valor)**: Valida y filta el contenido de una variable como Float.
9. **protected function process()**: Ejecuta un formulario de manera generica, El formulario debe ser pasado por medio de un parametro get "form". Si el formulario debe ejecutarse en modo de edición se debe pasar un parametro get "id".
10. **protected function solicitudAjax()**: Valida si se ha realizado una solicitud ajax, utilizando un plugin de javascript de nombre jd.ajax.
11. **protected function _setUrl($url)**: configura la propiedad url, para pasarla a un objeto $this->url.
12. **protected function obtPost($param)**: Retorna parámetros obtenidos mediante método post, false sino hay parámetros.
13. **protected function get($param = "")**: Retorna el valor get solicitado, false si el valor no es conseguido.
14. **protected function post($param = "", $nuevoValor = "")**: Retorna el valor post solicitado, false si el valor no es conseguido.
15. **protected function request($param = "", $nuevoValor = "")**: Retorna el valor request solicitado, false si el valor no es conseguido.
16. **protected function urlActual($valor = 1)**: Devuelve la URL correspondiente al metodo que hace la llamada.
17. **static function convertirNombreAUrl($nombre)**: Convierte un nombre en la estructura estándar de urls.
18. **protected function urlController($ctrl = "")**: Retorna la url del controlador actual, es decir, validará si el parámetro pasado es una cadena, o si el parámetro no existe, para posteriormente comenzar a formar y retornar dicha url.
19. **protected function urlModulo()**: agrega el modulo que se está trabajando a la url de la aplicación, si no hay modulo retornará false.
20. **protected function getUrl($metodo = "", $data = [])**: Devuelve la estructura de la url solicitada, construye la url a partir de un método, si sus parámetros están vacíos, retornará la url actual.
21. **protected function obtUrl($metodo = "", $data = [])**: Devuelve la estructura de la url solicitada, construye la url a partir de un método, si el método no existe, construye la url de la forma convencional (base/controlador/...), si los parámetros están vacíos, retornará la url actual.
22. **function getModulo($obj)**: Retorna el nombre del módulo en el que se encuentra el objeto.
23. **private function getModelo()**: Verifica si el controlador tiene un modelo correspondiente. Para que el modelo del controlador sea conseguido debe tener el nombre del Controlador en singular.
24. **protected function eliminarDatos($id)**: función estándar para eliminar registros de la base de datos, funcional solo con modelos que extiendan del objeto DataModel.
25. **protected function _404()**: Genera una excepción 404.
26. **protected function obtenerListaGet($lista)**: Retorna una lista a partir de un arreglo, si al recorrer el array no encuentra datos, retornará false.
27. **protected function respuestaAjax($respuesta, $tipo = 2)**: Devuelve contenido para una solicitud via ajax, permite imprimir la respuesta de la solicitud realizada sin esperar llegar a la vista.
28. **protected function respuestaJson($respuesta)**: Retorna la representación JSON del valor dado.
29. **protected function redireccionar($url)**: Redirecciona a la url dada.
30. **protected function obtURLApp()**: Retorna la aurl de la aplicación actual. 
31. **protected function obtJson($path)**: Retorna un arreglo a partir de un archivo JSON.
32. **protected function layout($layout)**: Define el layout a utilizar.
33. **protected function data($data, $valor = "")**: Asigna los parametros pasados para que puedan ser accedidos desde la vista.

Parámetros obsoletos:
---
1. **$tituloPagina**: Define el titulo de la pagina a colocar en la etiqueta title del head del sitio.
2. **$metaDescripcion**: Define el contenido de la meta-etiqueta description para uso de los buscadores.
3. **$data**: Arreglo que contiene la información que desee pasarse a la vista.


Métodos obsoletos:
---
1. **protected function getString($valor)**: Al ingresar un valor, nos devuelve el mismo valor en tipo de dato string. Para lograrlo éste método usa otro método de nombre obtString().
2. **protected function obtEntero($valor)**: Al ingresar un valor, nos devuelve el mismo valor en tipo de dato entero. Para lograrlo éste método usa otro método de nombre entero().
