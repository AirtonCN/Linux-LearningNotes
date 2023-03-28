### Anexos

* Rutas absolutas y relativas
    * Una ruta absoluta se especifica de la siguiente manera ***/directorio/directorio2/etc***
    * Una ruta relativa se especifica de la siguiente manera ***directorio1/directorio2/etc***
    * Notese que la dirferenecia esta en el slash "/"
    * Se puede acceder a una ruta absoluta desde cualquier directorio, pero las rutas relativas deben comenzar con el directorio actual (Este no se debe especificar a la hora de introducir el comando).

---

* Permisos de archivos y documentos
    * Listado de archivos.El tipo de archivo y permisos de archivo se muestran en los primeros 10 caracteres.
        ```
        sysadmin@localhost:~$ ls -l /var/log/
        total 844                                                                       
        -rw-r--r-- 1 root   root  18047 Dec 20  2017 alternatives.log                   
        drwxr-x--- 2 root   adm    4096 Dec 20  2017 apache2                            
        drwxr-xr-x 1 root   root   4096 Dec 20  2017 apt                                
        ```
    * En este ejemplo el propietario del archivo es el primer "root" y el grupo propietario es el segundo "root", el tamaño en bytes es 18047 y la última fecha de modificación es Dec 20 2017. El nombre es alternatives.log. 
        ```
        -rw-r--r-- 1 root   root  18047 Dec 20  2017 alternatives.log
        ```
    * Tipos de archivo y permisos para el ejemplo anterior:
        * Permisos para el propietario, solo tiene permisos de lectura "r" y escritura "w".
            |Tipo de archivo|Read|Write|Execute|
            |---|---|---|---|
            |-|r|w|-|
        * Permisos para el grupo propietario, solo tiene permisos de lectura "r".
            |Read|Write|Execute|
            |---|---|---|
            |r|-|-|
        * Permisos para invitados (todos los demás), solo tiene permisos de lectura "r".
            |Read|Write|Execute|
            |---|---|---|
            |r|-|-|

    * Tipos de archivos:
        |Símbolo|Tipo de archivo|
        |---|---|
        |d|Directorio|
        |-|Archivo Ordinario|
        |l|Enlaces simbólicos|
        |s|Socket|
        |p|Tubería (pipe)|
        |b|Archivo Bloque|
        |c|Archivo carácter|
    * Tipo de permiso:
        |Símbolo|Tipo de permiso|
        |---|---|
        |r|Lectura|
        |w|Escritura|
        |x|Ejecución|

---

* Consola vs Shell vs CLI vs Terminal
    * Consola
    * Shell: Es el programa o proceso que se encarga de ejecutar los comandos que reciba mediante el CLI.
    * CLI: Solo es la interfaz de linea de comandos.
    * Terminal: No lo tengo claro.

---

* Sintaxis útil
    * ***.*** (Punto): Apunta al directorio actual.
    * ***..*** (Punto): Apunta al directorio anterior.
    * Todo comando que acepte como argumento un archivo, por ejemplo: ***comando [archivo]***. Puede aceptar la ruta absoluta del archivo.

---

* Detener comandos.
    * Ctrl+D
    * Ctrl+C

---

* Regex (Regular Extended Expressions): Expresiones regulares extendidas que no todos los comandos aceptan a menos que se use el argumento adecuado.
    |Regex|Descripcion|
    |---|---|
    |***.***|Cualquier caracter individual|
    |***[ ]***|Cualquier caracter especificado|
    |***[^]***|Cualquier caracter que no sea el especificado|
    |***&ast;***|Cero o igual al caracter anterior|
    |***^***|Como primer caracter indica que el patron debera estar al principio de la linea para coincidir, de lo contrario se lo tomara como **^**|
    |***&dollar;***|Como ultimo caracter indica que el patron debera estar al final de la linea para coincidir, de lo contrario se tomara como ***$***|
    
    Expresiones para usar con ***egrep*** o ***grep -E***
    |Regex|Descripcion|
    |---|---|
    |***+***|Uno o mas del patrón anterior|
    |***?***|El patron introducido es opcional|
    |***{ }***|Especificar un minimo o un maximo de coincidencias para el patron introducido|
    |***&vert;***|Alternancia - or lógico|
    |***( )***|Crea grupos|

    Existen mas expresiones regulares extendidas, vease linux essentials para mas información.

---
---

### Notas
    
* Realizar una aclaración de los comandos ping, ifconfig y ps, en onenote.

```
```