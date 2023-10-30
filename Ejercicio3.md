# Ejercio 3
Utilizando el metacarácter de creación de cauces y sin utilizar la orden cd:
- Mostrar por pantalla, el listado (en formato largo) de los últimos 6 archivos del directorio padre en el directorio de trabajo.
```cpp
~$ ls -l /home | tail -6
```
- La orden wc muestra por pantalla el número de líneas, palabras y caracteres de un archivo (consulta la orden man para conocer más sobre ella). Utilizando dicha orden, mostrar por pantalla el número de caracteres (sólo ese número) de los archivos del directorio de trabajo que comiencen por los caracteres “e” o “f”.
```cpp
~$ wc -c e* f*
```
