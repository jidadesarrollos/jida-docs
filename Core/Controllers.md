# Controllers
La clase controller permite la ultilización de métodos comunes últiles para facilitar el ejercicio del desarrollo de cualquier proyecto.

# JIDA FRAMEWORK
Framework para aplicaciones web, con sintaxis simple, actual y elegante.

Sinopsis
---
```php
class \jida\Core\Controller extends Controller{
 ....
}
```
Parámetros
---
- **$temaLayout**: Define el tema de diseño a implementar en la aplicacion.
- **$multiidioma**: Define si la aplicación maneja multiples idiomas, Si es colocada en true el controller validara la variable $idioma y la incluira en las urls.
- **$layout**: Define el layout a usar por el controlador.
- **$idioma**:Define el idioma manejado al momento de la ejecucion del controlador.
- **$tituloPagina**: Define el titulo de la pagina a colocar en la etiqueta title del head del sitio.
- **$metaDescripcion**: Define el contenido de la meta-etiqueta description para uso de los buscadores.
- **$preEjecucion**: Define un metodo a ejecutar previo a la ejecucion de metodos accedidos por url.
- **$postEjecucion**: Define un metodo a ejecutar posterior a la ejecucion de metodos accedidos por url.
- **$modelo**: Define el Modelo a usar en el controlador.
- **$modelos**: Permite definir los modelos a usar en el controlador.
- **$vista**: Permite especificar una vista para el método.
- **$data**: Arreglo que contiene la información que desee pasarse a la vista.
- **$requireJS**: Archivos Javascript Requeridos.
- **$requireCSS**: Archivos CSS Requeridos en la vista.
- **$url**: Define la URL principal de acceso para el controlador (En caso de ser usada).
- **$post**: Data POST de Formulario.
- **$get**: Data Get pasada por url.
- **$request**: Contiene la data de solicitud o petición.
- **$_clase**: Nombre de la clase.
- **$_nombreController**: Nombre del controlador.
- **$_modulo**: Nombre del módulo.
- **$_metodo**: Nombre del método.
- **$_controlador**: Nombre del controlador.
- **$__url**: URL Actual Registra la URL ingresada en el navegador.
- **$_controlador**: Nombre del controlador.
- **$dv**: Instancia de clase DataVista.
- **$usuario**: Objeto User instanciado al iniciar sesion. Si la sesion no esta iniciada retorna vacio.
- **$manejoParams**: Define el funcionamiento que realiza el framework para manejar los parametros en las URL.
- **$_controladorURL**: Registra el nombre del controlador para la url.
- **$_urlBase**: Registra el nombre de la url base.

Métodos:
---
1. **__construct()**: En términos generales, éste método se encarga de construir las urls partiendo de la url base, es decir, recibe los parámetros de la url base y desde aquí­ va recibiendo y contruyendo las rutas de las url que contienen las data que conforman las distintas pantallas, por ejemplo: dev.jida.local(url base)/Data(información gestionada desde los controladores)/vista(pantalla, ya sean formularios, tablas, etc.). Adicionalmente, también recibe los parámetros de idiomas, ya que al construir las url, éstas reciben el nombre de la vista con el idioma determinado a mostrar, de igual manera, de trabajar con sesiones de usuario, éste método valida si la sesión está¡ abierta o cerrada para que el usuario, o bien sea dirigido al home principal, o bien a la pantalla de inicio de sesión.
2. **__conf()**: Retorna el objeto de configuraciÃ³n de la aplicación. 
3. **validarVarGlobales($bug = FALSE)**: Procesa las variables de parametros globales, es decir, valida que la informaciÃ³n que viajan por los mÃ©todos $_POST, $_GET, $_REQUEST sean correctos, y no generen error.
4. **instanciarHelpers()**: Permite procesar informaciÃ³n posterior a la ejecucion de metodos accedidos por url.
5. **instanciarModelos()**: Permite procesar informaciÃ³n mediante los modelos a usar en el controlador.
6. **getString($valor)**: Al ingresar un valor, nos devuelve el mismo valor en tipo de dato string. Para lograrlo Ã©ste mÃ©todo usa otro mÃ©todo de nombre obtString().
7. **obtString($valor)**: Convierte el contenido de una variable en codigo aceptado HTML (string).
8. **obtEntero($valor)**: Al ingresar un valor, nos devuelve el mismo valor en tipo de dato entero. Para lograrlo Ã©ste mÃ©todo usa otro mÃ©todo de nombre entero().
9. **entero($valor)**: Valida y filtra el contenido de una variable como Entero.
10. **decimal($valor)**: Valida y filta el contenido de una variable como Float.
11. **process()**: Ejecuta un formulario de manera generica, El formulario debe ser pasado por medio de un parametro get "form". Si el formulario debe ejecutarse en modo de ediciÃ³n se debe pasar un parametro get "id".
12. **solicitudAjax()**: Valida si se ha realizado una solicitud ajax, utilizando un plugin de javascript de nombre jd.ajax.
13. **_setUrl($url)**: configura la propiedad url, para pasarla a un objeto $this->url.
14. **obtPost($param)**: Retorna parÃ¡metros obtenidos mediante mÃ©todo post, false sino hay parÃ¡metros.
15. **get($param = "")**: Retorna el valor get solicitado, false si el valor no es conseguido.
16. **post($param = "", $nuevoValor = "")**: Retorna el valor post solicitado, false si el valor no es conseguido.
17. **request($param = "", $nuevoValor = "")**: Retorna el valor request solicitado, false si el valor no es conseguido.
18. **urlActual($valor = 1)**: Devuelve la URL correspondiente al metodo que hace la llamada.
19. **convertirNombreAUrl($nombre)**: Convierte un nombre en la estructura estÃ¡ndar de urls.
20. **urlController($ctrl = "")**: Retorna la url del controlador actual, es decir, validarÃ¡ si el parÃ¡metro pasado es una cadena, o si el parÃ¡metro no existe, para posteriormente comenzar a formar y retornar dicha url.
21. **urlModulo()**: agrega el modulo que se estÃ¡ trabajando a la url de la aplicaciÃ³n, si no hay modulo retornarÃ¡ false.
22. **getUrl($metodo = "", $data = [])**: Devuelve la estructura de la url solicitada, construye la url a partir de un mÃ©todo, si sus parÃ¡metros estÃ¡n vacÃ­os, retornarÃ¡ la url actual.
23. **obtUrl($metodo = "", $data = [])**: Devuelve la estructura de la url solicitada, construye la url a partir de un mÃ©todo, si el mÃ©todo no existe, construye la url de la forma convencional (base/controlador/...), si los parÃ¡metros estÃ¡n vacÃ­os, retornarÃ¡ la url actual.
24. **getModulo($obj)**: Retorna el nombre del mÃ³dulo en el que se encuentra el objeto.
25. **getModelo()**: Verifica si el controlador tiene un modelo correspondiente. Para que el modelo del controlador sea conseguido debe tener el nombre del Controlador en singular.
26. **eliminarDatos($id)**: funciÃ³n estÃ¡ndar para eliminar registros de la base de datos, funcional solo con modelos que extiendan del objeto DataModel.
27. **function _404()**: Genera una excepciÃ³n 404.
28. **obtenerListaGet($lista)**: Retorna una lista a partir de un arreglo, si al recorrer el array no encuentra datos, retornarÃ¡ false.
29. **respuestaAjax($respuesta, $tipo = 2)**: Devuelve contenido para una solicitud via ajax, permite imprimir la respuesta de la solicitud realizada sin esperar llegar a la vista.
30. **respuestaJson($respuesta)**: Retorna la representaciÃ³n JSON del valor dado.
31. **redireccionar($url)**: Redirecciona a la url dada.
32. **obtURLApp()**: Retorna la aurl de la aplicaciÃ³n actual. 
33. **obtJson($path)**: Retorna un arreglo a partir de un archivo JSON.
34. **layout($layout)**: Define el layout a utilizar.
35. **data($data, $valor = "")**: Asigna los parametros pasados para que puedan ser accedidos desde la vista.
