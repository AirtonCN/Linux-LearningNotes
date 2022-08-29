# Comandos de linux


1. ***ls*** (list): Muestra todos los archivos y directorios del directiorio actual
    * *sl -l*: Muestra una lista detallada de los acchivos y directorios de la carpeta actual
    * *ls -lr*: La misma list pero muestra los archivos al reverso
    * *ls -t*: Ordena la lista por ultima fecha de modificacion}
    * *ls -S*: Ordena la lista por tamaño de archivo o directorio
    * *ls/*: Muestra los archivos del direcorio principal "/"
    * *ls /var/log/*: Muestra los archivos del directorio "var/log" sin importar en que carpeta estemos
---

2. ***cd*** (Change directory): Cambia al directorio designado
    * *cd var*: Cambia al directorio var si estas en un directorio superior a el
    * *cd /var/*: Cambia al directorio var sin importar enq ue directorio estas
    * *cd ..*: Retrocede un directorio
    * *cd /*: Cambia al directorio principal 
    * Nota: Puedes concatenar varios directorios
---

3. ***pwd*** (print working directory): Imprime textualmente la direccion del directorio actual
    * Este comando solamente se usa para eso
---
4. ***su*** (substitute user): Ingresa al modo administrativo, **cabe resaltar que este comando crea un nuevo shell donde todos los comandos se ejecutaran en modo administrativo**
    * Este comando solicitara una contraseña
    * *su -*: Ingresa al modo administrativo
    * *su -l*: Ingresa al modo administrativo
    * *su --login*: Ingresa al modo administrativo
---
5. ***sl*** (Steam locomotive): Este comando ejecuta una animacion de un tren a vapor en el shell.
    * Este comando solo se puede ejecutar en el modo administrativo
---
6. ***sudo*** (substitute user do): Este comando permite ejecutar cualquier otro en modo tambien ejecuta como usuario root administrativo sin crear otro shell.
    * Tambien solicittara una contraseña, una sola vez
    * *sudo sl*: Ejecuta la animacion del tren a vapor
7. ***chmod*** (Change acces mode): Con este comando cambia los permisos de un archivo o directorio
    * *chmod u+w archivo*: Agrega el permiso de lectura al usuario prop.
    * *chmod u-w archivo*: Quita el permiso de lectura al usuario prop.
    * *chmod u+r archivo*: Agrega el permiso de lectura al usuario prop.
    * *chmod u-r archivo*: Quita el permiso de lectura al usuario prop.
    * *chmod u+x archivo*: Agrega el premiso de ejecucion al usuario prop.
    * *chmod u-x archivo*: Quita el permiso de ejecucion al usuario prop.
    * **Para cambiar permisos de grupo u otros solo cambiamos la *u* por *g* para grupos, o la letra *o* para todos los demas**
    * *chmod u=x archivo*: Especifica el permiso exacto (Probé este comando y tambien quita permisos)
---

