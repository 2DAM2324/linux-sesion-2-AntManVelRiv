# Ejercicio 2

Utilizando solamente las órdenes de la sesión anterior y los metacaracteres de redirección de salida:

- Crear un archivo llamado ej31 , que contendrá el nombre de los archivos del directorio padre del directorio
de trabajo.

```cpp
~$ touch ej31 | ls /home > ej31
~$ cat ej31
    amvr
    lost+found
```
- Crear un archivo llamado ej32 , que contendrá las dos últimas líneas del archivo creado en el ejercicio
anterior.
```cpp
~$ tail -2 ej31 > ej32
~$ cat ej32
    amvr
    lost+found
```
- Añadir al final del archivo ej32 , el contenido del archivo ej31 .
```cpp
~$ tail 2 ej31 >> ej32
~$ cat ej32
    amvr
    lost+found
    amvr
    lost+found
```
