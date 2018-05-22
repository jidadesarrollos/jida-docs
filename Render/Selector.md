# Formulario
Renderiza formularios configurados en html visible para el usuario, permite la validación de los mismos y la definición de su estructura mediante los distintos métodos que aplica la clase.

Sinopsis
---
```php
class Formulario extends Selector {
 ....
}
```
Parámetros
---
- **private $layout**
- **$name**
- **$tagPost**
- **$method**
- **$action**
- **$enctype**
- **$target**
- **public $setHtmlEntities**
- **$tagForm**
- **$botonEnvio**
- **$jidaValidador**
- **private $_consultaUpdate**
- **$_labelBotonEnvio**
- **private $_numeroExcepciones**
- **private $_fieldsets**
- **private $_id**
- **$labels**
- **private $_titulo**
- **private $_ce**
- **private $_arrayOrden**
- **private $_plantillaItem**
- **private $_plantillaBotones**
- **private $_plantillaTitulo**
- **private $_configuracion**
- **private $_columnasTotal**
- **private $_css**
- **private $_cssTitulo**
- **private $html**
- **private $_exprEstructura**
- **private $_path**
- **private $_campos**
- **private $_estructura**
- **private $_totalCampos**
- **private $_filaPivote**
- **$_botones**
- **private $_idEdicion**
- **private $_dataUpdate**
- **private $_dataUpdateMultiple**
- **private $_errores**
- **private $_validaciones**
- **private $_dataCampos**


Métodos:
---
1. **function __construct($form = "", $dataEdicion = "")**.
2. **private function _cargarFormulario($form, $dataEdicion)**: Carga el Formulario a mostrar, verifica si existe un archivo json para el formulario pedido, carga la informacion del mismo y la procesa.
3. **private function _configuaricionInicial()**.
4. **private function _procesarUpdate($dataEdicion)**: Procesa la informacion para renderizar el formulario en modo update.
5. **function removerTagForm($class = "form-alone")**: Remueve la etiqueta FORM del formulario, esta funcion puede llamarse cuando se deseen integrar múltiples formularios en una misma pantalla.
6. **private function _obtenerDataUpdate()**.
7. **private function validarJson()**.
8. **private function _botonEnvio()**: Genera el botón de envio si es requerido.
9. **function css($elemento, $css = "")**: Get y Set para css de los componentes del formulario, si el método es usado como setter retornará el mismo objeto form, si es usado como getter retornará la clase del elemento si es conseguido, caso contrario retornará un string vacio.
10. **private function _procesarEstructura()**: Procesa la estructura del formulario.
11. **private function _obtSelector($_campo)**: Define el objeto SelectorInput a retornar.
12. **private function _instanciarCampo($_campo)**: Genera la instancia de un SelectorInput.
13. **private function _instanciarCamposConfiguracion()**: Instancia los campos configurados del formulario, gestiona los campos del formulario realizando una instancia del objeto SelectorInput sobre cada campo para su posterior renderizacion.
14. **function titulo($titulo, $selector = "h2", $class = "page-header")**: Permite agregar un título al formulario.
15. **function enArreglo()**: Retorna los campos del formularo en un arreglo.
16. **function fieldsets($fieldsets)**: Agrega Fielsets y legends a la estructua del formulario.
17. **function render()**: Renderiza un formulario, genera el HTML de un formulario creado en el Framework, con toda la personalización creada.
18. **function imprimirBotones($plantilla = TRUE)**: Renderiza el HTML de los botones agregados al formulario.
19. **private function _obtTemplate($template, $params)**: Renderiza el contenido en plantillas predeterminadas.
20. **function boton($boton, $label = "", $selector = "button")**: Permite configurar botones para el formulario.
21. **function validar(&$data = "")**: Valida un formulario, verifica que la data pasada cumpla con las validaciones registradas en el formulario.
22. **static function msj($type, $msj, $redirect = false)**: Crea un mensaje a mostrar en un grid u objeto Tipo Vista.
23. **function campo($id)**: Permite acceder al objeto selector de un campo.
24. **function obtConsultaUpdate()**.
25. **function obtErrores()**.

Métodos obsoletos:
---
1. **function armarFormularioEstructura()**: Realiza lo mismo que la funcion armarFormulario, se mantiene la funcion para poder realizar la transicion de formularios usados con la clase Formulario, sin embargo el funcionamiento es el mismo ahora que el de armarFormulario, por tanto no se aconseja su uso..
2. **function armarFormulario()**: Obsoleto, usar método render.
