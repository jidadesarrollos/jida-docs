# DataVista
 Clase para pasar información a Vistas y Layouts.

Sinopsis
---
```php
class DataVista {
 ....
}
```
Parámetros
---
- **$js**
- **$css**
- **$jsAjax**
- **$title**
- **$meta_descripcion**
- **$meta_autor**
- **$meta_image**
- **$meta_url**
- **$meta**
- **$url_canonical**
- **$responsive**
- **$robots**
- **$solicitudAjax**
- **$google_verification**
- **$metodo**
- **$modulo**
- **$controlador**
- **$idioma**
- **$jsAgregado**
- **$cssAgregado**
- **$_esJadmin**
- **$_esApp**
- **$_urlCssBase**
- **$_urlJsBase**
- **$private $_plantilla**: Define una ruta absoluta para el template de la vista a usar, si no se encuentra.
- **$private $_path**

Métodos:
---
1. **function __construct($modulo = "", $controlador = "", $metodo = "", $jadmin = false, $app = FALSE)**: Método constructor.
2. **function incluirJS($js, $dir = TRUE, $contentJS = "", $footer = TRUE)**: Agrega un javascript para ser renderizado en el layout.
3. **function addJs($js, $dir = TRUE, $contentJS = "", $footer = TRUE)**
4. **function addCssModulo($css, $ruta = true)**: Permite agregar archivos css pertenecientes a un modulo específico.
5. **function addJsAjax($js, $dir = TRUE, $ambito = "")**: Agrega un javascript para ser renderizado en el layout.
6. **function addCSS($css, $url = "")**: Agrega un css a la hoja de estilo global.
7. **function removerCSS($archivo, $key = null)**: Elimina un archivo css de la lista de archivos registrada para inserción en el view.
8. **function removerJs()**
9. **function usarPlantilla($nombreVista, $path = "")**: Este método está disponible para vistas estándar que puedan tener un mismo comportamiento en diversos controladores.
10. **function obtPlantilla()**
11. **function getPath()**
12. **function addCodeJs($arg1, $file = false)**: Agrega código Js al final de la vista, luego de incluir.
12. **function editarMeta($array)**: Permite editar las múltiples etiquetas metas de una página.
13. **private function setMetaBasico()**
14. **function addMeta($meta)**
15. **protected function establecerAtributos($arr, $clase = "")**: Establece los atributos de una clase, valida si los valores pasados en el arreglo corresponden a los atributos de la clase en uso y asigna el valor correspondiente.
16. **function addJsCodigo($codigo)**

Métodos obsoletos:
---
1. **function addJsModulo($js, $modulo = "")**: Permite agregar archivos JS pertenecientes a un módulo especifico.
2. **function setVistaAsTemplate($nombreVista, $path = "")**
