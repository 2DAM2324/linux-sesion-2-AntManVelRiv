# Ejercicio 1
Se debe utilizar solamente una vez la orden chmod en cada apartado. Los cambios se harán en un archivo concreto del directorio de trabajo (salvo que se indique otra cosa). Cambiaremos uno o varios permisos en cada apartado (independientemente de que el archivo ya tenga o no dichos permisos) y comprobaremos que funciona correctamente:
- Dar permiso de ejecución al “resto de usuarios”.
```cpp
~$ ls -l
    -rw-rw-r-- 1 amvr amvr 0 oct 30 11:52 permisos.txt
~$ chmod o+x permisos.txt
~$ ls -l
    -rw-rw-r-x 1 amvr amvr 0 oct 30 11:52 permisos.txt
```
- Dar permiso de escritura y ejecución al “grupo”.
```cpp
~$ chmod g+wx permisos.txt
~$ ls -l
    -rw-rwxr-x 1 amvr amvr 0 oct 30 11:52 permisos.txt
```
- Quitar el permiso de lectura al “grupo” y al “resto de usuarios”.
```cpp
~$ chmod go-r permisos.txt
~$ ls -l
    -rw--wx--x 1 amvr amvr 0 oct 30 11:52 permisos.txt
```
- Dar permiso de ejecución al “propietario” y permiso de escritura el “resto de usuarios”.
```cpp
~$ chmod a+x,o+w permisos.txt
~$ ls -l
    -rwx-wx-wx 1 amvr amvr 0 oct 30 11:52 permisos.txt
```
- Dar permiso de ejecución al “grupo” de todos los archivos cuyo nombre comience con la letra “e”. Nota: Si
no hay más de dos archivos que cumplan esa condición, se deberán crear archivos que empiecen con “e”
y/o modificar el nombre de archivos ya existentes para que cumplan esa condición.
```cpp
~$ chmod g+x e*
~$ ls -l
    se muestra en dichos archivos que han cambiado los permisos
```
