# LINUX

<aside>
💡 para usar la vpn de thm es: **sudo openvpn 1012farcy.ovpn**

 luego ponemos en la máquina de attackbox: **ssh tryhackme@ip** y la contraseña es tryhackme.

</aside>

## 1. Comandos básicos

- **whoami:** para saber con que usuario estamos
- **********su:********** para cambiar de usuario. **su -l** para que nos lleve a nuestra carpeta principal.
- ********************************************************************************************************sudo su:******************************************************************************************************** cambiar a root usando nuestra contraseña.
- **pwd:** para saber la ruta donde estamos
- **ls:** listar contenido
    - **-a….** estos se llaman interruptores. ls -a es para mostrar archivos ocultos
- **cd:** ir a un directorio
- ************************find:************************ buscar un archivo cuando sabemos el nombre ej: find lista.txt sino sabemos el nombre podemos listar todos los que sean .txt así: find *.txt
- **cat:** para concatenar varios ficheros(unirlos) o mostrar el contenido de un archivo.
- **************grep:************** nos permite buscar en el contenido de los archivos valores específicos que estamos buscando.
    - **grep -n:** nos da tambien el numero de la linea donde esta lo que buscamos.
- --help: proporcionará una breve descripción y un ejemplo de cómo usar algun comando.
- man: leer la documentación de un comando.

- **ssh:** es para iniciar sesión remotamente, necesitamos saber el nombre del usuario, contraseña y su dirección ip.
    - **ssh usuario@direccion.ip**

---

## 2. Directorios y Ficheros

- **mkdir: crear directorio.**
- **rmdir: borrar directorio vacío.**
- **rm -r: borrar todo un directorio que no esta vacio.**
- **rm -r -i: nos pregunta que borrar de un directorio.**
- **touch: crear un fichero**
- **rm: borrar fichero**
- **mv: mover ficheros o cambiar nombres:**
    
       mv fichero.txt directorio/
    
    - para regresar un fichero donde estaba:
        
        mv directorio/fichero.txt directorionuevo
        
    - para cambiar nombre a un fichero:
        
        mv fichero.txt nombrenuevo.txt
        
- **cp: copiar un fichero.**
    
      cp fichero directorio/
    
    - para copiar un directorio y cambiar nombre:
        
        cp fichero.txt directorio/nuevonombre.txt
        

---

## 3. Rutas

~: es /home/f4rcy la carpeta personal.

. :  directorio actual.

.. :  es el padre(directorio antes del actual)

---

## 4. Permisos

para poder los permisos damos ls -l.

- nos aparecerá algo así es un ****************ejemplo:****************

```
-rw-r--r-- 1 cmnatic cmnatic 0 Feb 19 10:37 file1
-rw-r--r-- 8 cmnatic cmnatic 0 Feb 19 10:37 file2
```

![https://www.prored.es/wp-content/uploads/2018/11/prored-bits-de-permisos-unix-permission-bits.png](https://www.prored.es/wp-content/uploads/2018/11/prored-bits-de-permisos-unix-permission-bits.png)

**-:** es para indicar que es un fichero.

**d:** es para indicar que es un directorio.

**l:** es para indicar que es un enlace.

**r:** permisos de lectura.

**w:** permisos de escritura.

**x:** permisos de ejecución.

**u:** usuario.

**g:** grupo.

**o:** otros.

### **como se cambia?**

para añadir permisos:

- **chmod u+x nombrearchivo.txt** : le estamos dando permisos de ejecución al usuario.

para quitar permisos:

- **********************************************************chmod u-x nombrearchivo.txt**********************************************************

> ***************************************************************************************************************************************también lo podemos hacer con varios a la v******************************************************************************************ez:* **********************************************************chmod u+x, g+w nombrearchivo.txt**********************************************************
> 

---

## 5. Sistema

- actualizar sistema:
    - **sudo apt update, sudo apt upgrade**. (por ahi 2 veces al mes)
- instalar software:
    - **sudo apt install:** instalar un paquete de repositorios online.
    - **sudo dpkg -i:** para instalar un archivo local que hayamos descargado.
- desinstalar software:
    - **sudo apt remove:** remover software.

---

temas por ver:

puertos
