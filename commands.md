## Comandos Linux Unhatched
### Se describen comandos sintaxis y ejemplos.

1. ***ls*** (list): Muestra todos los archivos y directorios del directiorio actual.
    * *sl -l*: Muestra una lista detallada de los acchivos y directorios de la carpeta actual.
    * *ls -lr*: La misma list pero muestra los archivos al reverso.
    * *ls -t*: Ordena la lista por ultima fecha de modificacion.
    * *ls -S*: Ordena la lista por tamaño de archivo o directorio.
    * *ls/*: Muestra los archivos del direcorio principal "/".
    * *ls /var/log/*: Muestra los archivos del directorio "var/log" sin importar en que carpeta estemos.
    * Se pueden combinar diferentes argumentos: *ls -Sr*(Muestra la lista de archivos por tamaño en orden ascendente).
    * Puedes mostrar detalles de un archivo especifico con la siguiente sintaxis: *ls -l* [archivo].
    * *ls -l hello.sh*: Muestra detalles unicamente del archivo hello.sh. 
---

2. ***cd*** (Change directory): Cambia al directorio designado.
    * *cd var*: Cambia al directorio var si estas en un directorio superior a el.
    * *cd /var/*: Cambia al directorio var sin importar enq ue directorio estas.
    * *cd ..*: Retrocede un directorio.
    * *cd /*: Cambia al directorio principal.
    * *cd .*: Señala al directorio actual.
    * Nota: Puedes concatenar varios directorios.
    * Puedes ingresar a cualquier directorio desde cualquier directorio con la siguiente sintaxis: *cd* [directorio raíz]*/*[subdirectorio]*/*[subdirectorio].
---

3. ***pwd*** (print working directory): Imprime textualmente la direccion del directorio actual.
    * Este comando solamente se usa para eso.
---
4. ***su*** (substitute user): Ingresa al modo administrativo o root, **cabe resaltar que este comando crea un nuevo shell donde todos los comandos se ejecutaran en modo administrativo**.
    * Este comando solicitara una contraseña.
    * *su -*: Ingresa al modo administrativo.
    * *su -l*: Ingresa al modo administrativo.
    * *su --login*: Ingresa al modo administrativo.
---
5. ***sl*** (Steam locomotive): Este comando ejecuta una animacion de un tren a vapor en el shell.
    * Este comando solo se puede ejecutar en el modo administrativo.
---
6. ***sudo*** (substitute user do): Este comando permite ejecutar cualquier otro en modoadministrativo tambien ejecuta como usuario root administrativo sin crear otro shell.
    * Tambien solicittara una contraseña, una sola vez.
    * *sudo sl*: Ejecuta la animacion del tren a vapor.
---
7. ***exit*** (exit): Se usa para salir del modo administrativo *su*.
---
8. ***chmod*** (Change acces mode): Con este comando cambia los permisos de un archivo o directorio.
    * Sintaxis: *chmod* [conjunto][accion][permiso].
    * *chmod u+w archivo*: Agrega el permiso de lectura al usuario prop.
    * *chmod u-w archivo*: Quita el permiso de lectura al usuario prop.
    * *chmod u+r archivo*: Agrega el permiso de lectura al usuario prop.
    * *chmod u-r archivo*: Quita el permiso de lectura al usuario prop.
    * *chmod u+x archivo*: Agrega el premiso de ejecucion al usuario prop.
    * *chmod u-x archivo*: Quita el permiso de ejecucion al usuario prop.
    * **Para cambiar permisos de grupo u otros solo cambiamos la *u* por *g* para grupos, o la letra *o* para todos los demas y *a* para todos**.
    * *chmod u=x archivo*: Especifica el permiso exacto (Probé este comando y tambien quita permisos).
---
9. ***./*** (Ejecutar script): Se utiliza para ejecutar un script cualquiera ubicado en el directorio actual
    * Sintaxis: *./* [script].
    * *./ hello.sh*: Ejecuta el script hello.sh.
---
10. ***chown*** (Change owner): Cambia el propietario del archivo.
    * Sintaxis: *chown* [opcion] [propietario] [archivo]
    * *chown root hello.sh*: Cambia el usuario propietario a root.
---
11. ***cat*** (Concatenate): Visualiza archivos, normalmente usado para ver archivos pequeños ya que con archivos grandes no es muy practico.
    * Sintaxis: *cat* [opcion] [archivo].
    * *cat alpha.txt*: Muestra el contenido del archivo alpha.txt.
---
12. ***tail*** y ***head***: Visualiza las primeras o las ultimas lineas de un archivo, el numero de lineas puede variar en cada shell.
    * Sintaxis: *head* [opcion] [archivo]
    * Sintaxis: *tail* [opcion] [archivo]
    * *head alpha.txt*: muestra las primeras lineas del archivo alpha.txt.
    * *tail alpha.txt*: muestra las ultimas lineas del archivo alpha.txt.
    * *head -n 5 alpha.txt*: muestra las primeras 5 lineas del archivo alpha.txt contando desde arriba.
    * *tail -n 5 alpha.txt*: muestra las ultimas 5 lineas del archivo alpha.txt contando desde abajo.
---
13. ***cp*** (Copy): Copia un archivo y envialo a un directorio destino, Se debe tener como minimo permisos de ejecucion y lectura del archivo y el directorio en el que se encuentra. Se debe tener siempre estos permisos en el directorio /home y /tmp 
    * Sintaxis desde cualquier directorio: *cp* [origen]*/*[archivo] [destino].
    * Sintaxis para un copiar archivo en directorio actual: *cp* [archivo] [destino].
    * Sintaxis para copiar un archivo al directorio actual: *cp* [origen]*/* *.*.
---
14. ***dd*** (Disk/Data Duplicate): Copia/clona particiones de disco completas, crea archivos con un tamalo especifico, realiza backups, copia datos no procesados.
    * Sintaxis para crear archivo de un tamaño específico: *dd* *if=*[entrada] *of=*[salida] *bs=*[tamaño] *count=*[cantidad]
    * *if* (Input file): Direccion completa del archivo de entrada.
    * *of* (Output file): Direccion completa del archivo de salida.
    * *bs* (Block size): Tamañao de bloque en bytes, se puede usar K,M,G,T.
    * *count* (Cuenta): Cuantos bloques del tamaño extablecido se usaran.
    * Para copiar particiones discos o directorios completos no es necesario especificar el tamaño. Sintaxis: *dd* *if=*[entrada] *of=*[salida].




---
---
### Anexos

a. Consola vs Shell vs CLI vs Terminal