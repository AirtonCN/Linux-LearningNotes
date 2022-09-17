## Comandos Linux Unhatched
### Se describen comandos sintaxis y ejemplos.

1. ***ls*** (list): Muestra todos los archivos y directorios del directiorio actual.
    * ***sl -l***: Muestra una lista detallada de los acchivos y directorios de la carpeta actual.
    * ***ls -lr***: La misma list pero muestra los archivos al reverso.
    * ***ls -t***: Ordena la lista por ultima fecha de modificacion.
    * ***ls -S***: Ordena la lista por tamaño de archivo o directorio.
    * ***ls/***: Muestra los archivos del direcorio principal "/".
    * ***ls /var/log/***: Muestra los archivos del directorio "var/log" sin importar en que carpeta estemos.
    * Se pueden combinar diferentes argumentos: ***ls -Sr***(Muestra la lista de archivos por tamaño en orden ascendente).
    * Puedes mostrar detalles de un archivo especifico con la siguiente sintaxis: ***ls -l*** [archivo].
    * ***ls -l hello.sh***: Muestra detalles unicamente del archivo hello.sh. 

---

2. ***cd*** (Change directory): Cambia al directorio designado.
    * ***cd var***: Cambia al directorio var si estas en un directorio superior a el.
    * ***cd /var/***: Cambia al directorio var sin importar enq ue directorio estas.
    * ***cd ..***: Retrocede un directorio.
    * ***cd /***: Cambia al directorio principal.
    * ***cd .***: Señala al directorio actual.
    * Nota: Puedes concatenar varios directorios.
    * Puedes ingresar a cualquier directorio desde cualquier directorio con la siguiente sintaxis: ***cd [directorio raíz]/[subdirectorio]/[subdirectorio]***.

---

3. ***pwd*** (print working directory): Imprime textualmente la direccion del directorio actual.
    * Este comando solamente se usa para eso.

---

4. ***su*** (substitute user): Ingresa al modo administrativo o root, **cabe resaltar que este comando crea un nuevo shell donde todos los comandos se ejecutaran en modo administrativo**.
    * Este comando solicitara una contraseña.
    * ***su -***: Ingresa al modo administrativo.
    * ***su -l***: Ingresa al modo administrativo.
    * ***su --login***: Ingresa al modo administrativo.

---

5. ***sl*** (Steam locomotive): Este comando ejecuta una animacion de un tren a vapor en el shell.
    * Este comando solo se puede ejecutar en el modo administrativo.
---

6. ***sudo*** (substitute user do): Este comando permite ejecutar cualquier otro en modoadministrativo tambien ejecuta como usuario root administrativo sin crear otro shell.
    * Tambien solicittara una contraseña, una sola vez.
    * ***sudo sl***: Ejecuta la animacion del tren a vapor.

---

7. ***exit*** (exit): Se usa para salir del modo administrativo ***su***.

---

8. ***chmod*** (Change acces mode): Con este comando cambia los permisos de un archivo o directorio.
    * Sintaxis: ***chmod [conjunto][accion][permiso]***.
    * ***chmod u+w archivo***: Agrega el permiso de lectura al usuario prop.
    * ***chmod u-w archivo***: Quita el permiso de lectura al usuario prop.
    * ***chmod u+r archivo***: Agrega el permiso de lectura al usuario prop.
    * ***chmod u-r archivo***: Quita el permiso de lectura al usuario prop.
    * ***chmod u+x archivo***: Agrega el premiso de ejecucion al usuario prop.
    * ***chmod u-x archivo***: Quita el permiso de ejecucion al usuario prop.
    * **Para cambiar permisos de grupo u otros solo cambiamos la *u* por *g* para grupos, o la letra *o* para todos los demas y *a* para todos**.
    * ***chmod u=x archivo***: Especifica el permiso exacto (Probé este comando y tambien quita permisos).

---

9. ***./*** (Ejecutar script): Se utiliza para ejecutar un script cualquiera ubicado en el directorio actual
    * Sintaxis: ***./ [script]***.
    * ***./ hello.sh***: Ejecuta el script hello.sh.

---

10. ***chown*** (Change owner): Cambia el propietario del archivo.
    * Sintaxis: ***chown [opcion] [propietario] [archivo]***.
    * ***chown root hello.sh***: Cambia el usuario propietario a root.

---

11. ***cat*** (Concatenate): Visualiza archivos, normalmente usado para ver archivos pequeños ya que con archivos grandes no es muy practico.
    * Sintaxis: ***cat [opcion] [archivo]***.
    * ***cat alpha.txt***: Muestra el contenido del archivo alpha.txt.

---

12. ***tail*** y ***head***: Visualiza las primeras o las ultimas lineas de un archivo, el numero de lineas puede variar en cada shell.
    * Sintaxis: ***head [opcion] [archivo]***.
    * Sintaxis: ***tail [opcion] [archivo]***.
    * ***head alpha.txt***: muestra las primeras lineas del archivo alpha.txt.
    * ***tail alpha.txt***: muestra las ultimas lineas del archivo alpha.txt.
    * ***head -n 5 alpha.txt***: muestra las primeras 5 lineas del archivo alpha.txt contando desde arriba.
    * ***tail -n 5 alpha.txt***: muestra las ultimas 5 lineas del archivo alpha.txt contando desde abajo.

---

13. ***cp*** (Copy): Copia un archivo y envialo a un directorio destino, Se debe tener como minimo permisos de ejecucion y lectura del archivo y el directorio en el que se encuentra. Se debe tener siempre estos permisos en el directorio /home y /tmp 
    * Sintaxis desde cualquier directorio: ***cp [origen]/[archivo] [destino]***.
    * Sintaxis para un copiar archivo en directorio actual: ***cp [archivo] [destino]***.
    * Sintaxis para copiar un archivo al directorio actual: ***cp [origen]/ .***.

---

14. ***dd*** (Disk/Data Duplicate): Copia/clona particiones de disco completas, crea archivos con un tamalo especifico, realiza backups, copia datos no procesados.
    * Sintaxis para crear archivo de un tamaño específico: ***dd if=[entrada] of=[salida] bs=[tamaño] count=[cantidad]***
    * ***if*** (Input file): Direccion completa del archivo de entrada.
    * ***of*** (Output file): Direccion completa del archivo de salida.
    * ***bs*** (Block size): Tamañao de bloque en bytes, se puede usar K,M,G,T.
    * ***count*** (Cuenta): Cuantos bloques del tamaño extablecido se usaran.
    * Para copiar particiones discos o directorios completos no es necesario especificar el tamaño. Sintaxis: ***dd if=[entrada] of=[salida]***.

---

15. ***mv*** (Move): Mover archivos entre ubicaciones del sistema. Mover el archivo dentro del mismo directorio resulta en el cambio de nombre del archivo. Este comando requiere como minimo permisos de escritura y ejecución.
    * Sintaxis: ***mv [origen] [destino]***
    * ***mv people.csv Work***: mueve el archivo people.csv del directorio actual al subdirectiorio Work del directorio actual.
    * ***mv Work/people.csv .***: Mueve el archivo people.csv del subdirectorio Work al directorio actual.
    * ***mv animals.txt zoo.txt***: Cambia de nombre el archivo de animals.txt a zoo.txt.
    * Se pueden mover varios archivos con la siguiente sintaxis: ***mv [archivo1] [archivo2] [archivo3] [destino]***.
    * ***mv alpha.txt letters.txt os.csv School***: Mueve tres archivos txt y un csv al directorio School.

---

16. ***rm*** (Remove): Elimina un archivo o un directorio entero, este comando es irreversible, mucho cuidado. Requiere como minimo permisos de escritura y ejecución.
    * Sintaxis para archivos: ***rm [archivo]***
    * Sintaxis para directorios: ***rm -r [directorio]***
    * ***rm animals.txt***: Elimina el archivo animals.txt.
    * ***rm -r Documents***: Elimina el directorio Documents.

---

17. ***grep*** (Global regular expresion print): Filtra entradas de un archivo, busca e imprime y una linea de un archivo de acuerdo aun patron definido en el comando.
    * Sintaxis: ***grep [opciones] [patron] [archivo]***
    * ***grep sysadmin passwd***: Muestra detalles del usuario sysadmin, detalles que se encuentran en el archivo passwd, mas info de este archivo en linux essentials.
    * Este comando puede interpretar patrones de busqueda mucho mas complejos.
    * Se debe poner comillas simples en el patron para que este no sea confundido con un comando especial del shell.
    * ***grep 'r..d' alpha.txt***: Encuentra todos las coincidencias con el patron 'r..d' donde los puntos simbolizan cualquier caracter.
    * ***grep '[0-9]' profile.txt***: Encuentra caracteres numéricos y muestra las lineas donde estan.
    * ***grep '[^0-9]' profile.txt***: Muestra lineas que contengan carácteres no numéricos, omite las que tienen carácteres puramente numéricos.
    * ***grep 're*d' red.txt***: Muestra lineas que contengan el caracter "e" repetido de manera corrida, o en su defecto, su ausencia total.Tambien deben contener "r" al principio y "d" al final.   
    * ***grep 'r[oe]*d' red.txt***: Muestra lineas que contengan los caracteres "o" o "e" repetido de manera corrida, o en su defecto, la auscencia total de ambos. Tambien deben contener "r" al principio y "d" al final de cada linea.
    * ***grep 'red'***: El shell nos permitira introducir caracteres para luego identificar aquellas lineas que contengan "red" en el texto introducido.

----

18. ***shutdown*** (Apagar): Apaga el sistema, para ello debes definir un temporizador o una hora en su defecto. Se requiere ser usuario administrador para ejecutar este comando.
    * Sintaxis: ***shutdowm [hora/tiempo] [banner_opcional]***
    * ***shutdown now***: Apaga el sistema ahora mismo.
    * ***shutdown 22:54***: Se apagara el sistema a las 22:54 UTC, solo se puede introducir en este horario. Tu zona horaria es UTC-5.
    * ***shutdown +1 "Alamoz"***: Se apaga el sistema en un minuto y se muestra el mensaje en broadcast: Alamoz.

---

19. ***ifconfig*** y ***iwconfig*** (Interface configuration y Wireless interface configuration): Ambos comandos sirven para mostrar la configuracion de red alámbrica e inálambrica.
    * Sintaxis: ***ifconfig [opcion]***
    * ***ifconfig***: Muestra informacion de todas las interfaces de red de nuestro sistema.
    
        ```
            root@localhost:~# ifconfig                                     
        eth0      Link encap:Ethernet  HWaddr 02:42:c0:a8:01:02                         
                inet addr:192.168.1.2  Bcast:192.168.1.255  Mask:255.255.255.0        
                UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1                    
                RX packets:59 errors:0 dropped:0 overruns:0 frame:0                   
                TX packets:86 errors:0 dropped:0 overruns:0 carrier:0                 
                collisions:0 txqueuelen:1000                                          
                RX bytes:4346 (4.3 KB)  TX bytes:5602 (5.6 KB)                        
                                                                                        
        lo        Link encap:Local Loopback                                             
                inet addr:127.0.0.1  Mask:255.0.0.0                                   
                UP LOOPBACK RUNNING  MTU:65536  Metric:1                              
                RX packets:2 errors:0 dropped:0 overruns:0 frame:0                    
                TX packets:2 errors:0 dropped:0 overruns:0 carrier:0                  
                collisions:0 txqueuelen:1000                                          
                RX bytes:100 (100.0 B)  TX bytes:100 (100.0 B)  
        ```

    * En el ejemplo anterior se muestra la interfaz ethernet 0 y el loopback(Interfaz que sirve para que la maquina envie informacion basada en red a si misma).

---

20. ***ping*** (Proviene de ping-pong): Envia paquetes a un dominio o direccion ip y espera una respuesta.
    * Sintaxis: ***ping [ip/dominio]***
    * ***ping 192.168.1.2***: Envia paquetes icmp a la ip introducida de manera indefinida.
    * ***ping -c 4 192.168.1.2***: Envia 4 paquetes icmp a la ip introducida.

        ```
        root@localhost:~# ping -c 4 192.168.1.2                                       
        PING 192.168.1.2 (192.168.1.2) 56(84) bytes of data.                          
        64 bytes from 192.168.1.2: icmp_req=1 ttl=64 time=0.051 ms                    
        64 bytes from 192.168.1.2: icmp_req=2 ttl=64 time=0.064 ms                    
        64 bytes from 192.168.1.2: icmp_req=3 ttl=64 time=0.050 ms                    
        64 bytes from 192.168.1.2: icmp_req=4 ttl=64 time=0.043 ms                    
                
        --- 192.168.1.2 ping statistics ---                                           
        4 packets transmitted, 4 received, 0% packet loss, time 2999ms                
        rtt min/avg/max/mdev = 0.043/0.052/0.064/0.007 ms 
        ```
    
    * El éxito del comando indica una buena conectividad a la ip dominio o host que se introdujo en el comando.

---

21. ***ps*** (Process Status): Muestra detalles de los procesos que se estan ejecutando actualmente.
    * Sintaxis: ***ps [opciones]***
    * ***ps***: Muestra lo siguiente.
    
        ```
        sysadmin@localhost:~$ ps
        PID TTY          TIME CMD
        80 pts/0        00:00:00 bash
        94 pts/0        00:00:00 ps
        ```
    * Se puede observar en la ultima columna que los procesos en ejecucion son bash y el comando ps.
    * PID (Process ID): Es el identificador unico de cada proceso.
    * TTY (Teletype): Nombre o tipo de la terminal en donde el proceso esta funcionando.
    * CMD (Command): El comando que inició el proceso.
    * ***ps -e***: Muestra todos los procesos que ejecuta el sistema y no solo los del shell.
    * ***ps -ef***: Muestra todos los procesos que ejecuta el sistema y no solo los del shell(de manera mas detallada).
    *
    *
    *





---
---
### Anexos

* Consola vs Shell vs CLI vs Terminal
    * Consola
    * Shell
    * CLI
    * Terminal
* Sintaxis útil
    * ***.*** (Punto): Apunta al directorio actual.
    * ***..*** (Punto): Apunta al directorio anterior.
    * Todo comando que acepte como argumento un archivo, por ejemplo: ***comando [archivo]***. Puede aceptar la direccion del archivo sin importar en que directorio te encuentres.
* Detener comandos.
    * Ctrl+D
    * Ctrl+C

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

### Notas
    
* Realizar una aclaración de los comandos ping, ifconfig y ps, en onenote.

```
```