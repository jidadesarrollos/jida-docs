# Explicaci�n del funcionamiento de cada uno de los m�todos en la clase controller, que se ubica en el archivo controller.php

#JIDA FRAMEWORK
Framework para aplicaciones web, con sintaxis simple, actual y elegante.

**Versi�n Actual: 0.6**

## class Controller [\jida\Core\Controller.php]

**M�todos:**

1. __construct(): En t�rminos generales, �ste m�todo se encarga de construir las urls partiendo de la url base, es decir, recibe los par�metros de la url base y desde aqu�� va recibiendo y contruyendo las rutas de las url que contienen las data que conforman las distintas pantallas, por ejemplo: dev.jida.local(url base)/Data(informaci�n gestionada desde los controladores)/vista(pantalla, ya sean formularios, tablas, etc.). Adicionalmente, tambi�n recibe los par�metros de idiomas, ya que al construir las url, �stas reciben el nombre de la vista con el idioma determinado a mostrar, de igual manera, de trabajar con sesiones de usuario, �ste m�todo valida si la sesi�n est� abierta o cerrada para que el usuario, o bien sea dirigido al home principal, o bien a la pantalla de inicio de sesi�n.
2. __conf(): Retorna el objeto de configuración de la aplicaci�n. 
3. validarVarGlobales($bug = FALSE): Procesa las variables de parametros globales, es decir, valida que la información que viajan por los métodos $_POST, $_GET, $_REQUEST sean correctos, y no generen error.
4. instanciarHelpers(): Permite procesar información posterior a la ejecucion de metodos accedidos por url.
5. instanciarModelos(): Permite procesar información mediante los modelos a usar en el controlador.
6. getString($valor): Al ingresar un valor, nos devuelve el mismo valor en tipo de dato string. Para lograrlo éste método usa otro método de nombre obtString().
7. obtString($valor): Convierte el contenido de una variable en codigo aceptado HTML (string).
8. obtEntero($valor): Al ingresar un valor, nos devuelve el mismo valor en tipo de dato entero. Para lograrlo éste método usa otro método de nombre entero().
9. entero($valor): Valida y filtra el contenido de una variable como Entero.
10. decimal($valor): Valida y filta el contenido de una variable como Float.
11. process(): Ejecuta un formulario de manera generica, El formulario debe ser pasado por medio de un parametro get "form". Si el formulario debe ejecutarse en modo de edición se debe pasar un parametro get "id".
12. solicitudAjax(): Valida si se ha realizado una solicitud ajax, utilizando un plugin de javascript de nombre jd.ajax.
13. _setUrl($url): configura la propiedad url, para pasarla a un objeto $this->url.
14. obtPost($param): Retorna parámetros obtenidos mediante método post, false sino hay parámetros.
15. get($param = ""): Retorna el valor get solicitado, false si el valor no es conseguido.
16. post($param = "", $nuevoValor = ""): Retorna el valor post solicitado, false si el valor no es conseguido.
17. request($param = "", $nuevoValor = ""): Retorna el valor request solicitado, false si el valor no es conseguido.
18. urlActual($valor = 1): Devuelve la URL correspondiente al metodo que hace la llamada.
19. convertirNombreAUrl($nombre): Convierte un nombre en la estructura estándar de urls.
20. urlController($ctrl = ""): Retorna la url del controlador actual, es decir, validará si el parámetro pasado es una cadena, o si el parámetro no existe, para posteriormente comenzar a formar y retornar dicha url.
21. urlModulo(): agrega el modulo que se está trabajando a la url de la aplicación, si no hay modulo retornará false.
22. getUrl($metodo = "", $data = []): Devuelve la estructura de la url solicitada, construye la url a partir de un método, si sus parámetros están vacíos, retornará la url actual.
23. obtUrl($metodo = "", $data = []): Devuelve la estructura de la url solicitada, construye la url a partir de un método, si el método no existe, construye la url de la forma convencional (base/controlador/...), si los parámetros están vacíos, retornará la url actual.
24. getModulo($obj): Retorna el nombre del módulo en el que se encuentra el objeto.
25. getModelo(): Verifica si el controlador tiene un modelo correspondiente. Para que el modelo del controlador sea conseguido debe tener el nombre del Controlador en singular.
26. eliminarDatos($id): función estándar para eliminar registros de la base de datos, funcional solo con modelos que extiendan del objeto DataModel.
27. function _404(): Genera una excepción 404.
28. obtenerListaGet($lista): Retorna una lista a partir de un arreglo, si al recorrer el array no encuentra datos, retornará false.
29. respuestaAjax($respuesta, $tipo = 2): Devuelve contenido para una solicitud via ajax, permite imprimir la respuesta de la solicitud realizada sin esperar llegar a la vista.
30. respuestaJson($respuesta): Retorna la representación JSON del valor dado.
31. redireccionar($url): Redirecciona a la url dada.
32. obtURLApp(): Retorna la aurl de la aplicación actual. 
33. obtJson($path): Retorna un arreglo a partir de un archivo JSON.
34. layout($layout): Define el layout a utilizar.
35. data($data, $valor = ""): Asigna los parametros pasados para que puedan ser accedidos desde la vista.
