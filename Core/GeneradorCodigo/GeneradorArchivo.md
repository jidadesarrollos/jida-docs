# GeneradorArchivo
Clase generadora de archivos.

Sinopsis
---
```php
trait GeneradorArchivo {
 ....
}
```
Parámetros
---
- **$nombreArchivo**: Nombre del Archivo.
- **$extension**: Extension del archivo.
- **$dir**: Directorio de ubicación del archivo.
- **protected $contenido**: Define el contenido del Archivo.

Métodos:
---
1. **function crear($archivo="")**: Crea un archivo.
2. **function directorio($dir="")**: Permite definir u obtener el directorio del archivo.
3. **function escribir($contenido="")**
4. **function cerrar()**
5. **function saltodeLinea($total=1)**
6. **function tab($cantidad=1)**: Agrega tabulaciones al archivo.
7. **function retorno()**
8. **function addContenido($contenido)**
9. **function imprimirContenido($contenido="")**
