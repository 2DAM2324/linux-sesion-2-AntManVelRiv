# Ejercicio 4
Resuelva cada uno de los siguientes apartados.
- Crear un archivo llamado ejercicio1, que contenga las 17 últimas líneas del texto que proporciona la orden man para la orden chmod (se debe hacer en una única línea de órdenes y sin utilizar el metacarácter “;” ).
```cpp
~$ man chmod | tail -17 > ejercicio1
```
- Al final del archivo ejercicio1, añadir la ruta completa del directorio de trabajo actual.
```cpp
~$ pwd >> ejercicio1
```
- Usando la combinación de órdenes mediante paréntesis, crear un archivo llamado ejercicio3 que contendrá el listado de usuarios conectados al sistema (orden who) y la lista de archivos del directorio actual.
```cpp
~$ (who && ls) >> ejercicio3
```
- Añadir, al final del archivo ejercicio3, el número de líneas, palabras y caracteres del archivo ejercicio1. Asegúrese de que, por ejemplo, si no existiera ejercicio1, los mensajes de error también se añadieran al final de ejercicio3.
```cpp
~$ (wc ejercicio1 2>&1) >> ejercicio3
```
- Con una sola orden chmod, cambiar los permisos de los archivos ejercicio1 y ejercicio3, de forma que se quite el permiso de lectura al “grupo” y se dé permiso de ejecución a las tres categorías de usuarios.
```cpp
~$ chmod a+x,g+x-r,o+x ejercicio1 ejercicio3
```