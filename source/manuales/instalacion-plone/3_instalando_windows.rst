.. -*- coding: utf-8 -*-

3. Instalando en Windows
========================

¿Como preparar y ejecutar Plone en Windows?; no para desarrollo considerable.

El instalador binario para Windows es la opción a escoger si quiere probar
Plone en Windows o para ser el host de un sitio, pero no para desarrollo
considerable. Si quiere elaborar un desarrollo considerable, revise `este
documento`_.

De lo contrario, continué leyendo estas instrucciones tomadas del sitio
`Catapult Solutions`_.


Descargue e instale Plone
-------------------------

1.  Descargue el instalador de esta pagina contenida en plone.org:
    `http://plone.org/products/plone`_.

2.  Guárdelo en un sitio que pueda recordar, tal como su Escritorio.

3.  Después que la descarga haya finalizado, haga doble clic en archivo
    del instalador para ejecutarlo.

4.  Encamínese por el asistente de instalación. Nunca instale Plone en la
    misma carpeta que uso para instalar una versión vieja, siempre use una
    nueva.

5.  Escriba o copie la locación de la instalación, tal como esta
    ``C:\\Program Files\\Plone``. Usted necesitara esto mas adelante.

6.  Escriba el nombre de usuario y contraseña que ingrese en el
    asistente. Ya que también necesitara esto después.

7.  Aguarde mientras el instalador Extrae los archivos y crea la
    instancia de Plone.


Iniciando/Deteniendo Plone
--------------------------


Usando el Controlador
.....................

Usted puede acceder al Controlador de Plone para Windows, mediante el botón
de *Inicio > Todos los programas > Plone*. Con el controlador puede start/stop
(iniciar/detener) el servidor (Zope) de Plone y revisar el estado.


Usando la linea de comando
..........................

Después de que el instalador haya finalizado proceda a abrir una ventana de
Símbolo de sistema (generalmente *Inicio > Todos los programas > Accesorios*).

Vaya al directorio de instalación de Plone, aquel que escribió anteriormente.
Ejemplo:

.. code-block:: sh

    cd "C:\\Program Files\\Plone"

Para iniciar la instancia de Plone por primera vez, introduzca el siguiente
comando:

.. code-block:: sh

    bin\\instance.exe fg

Esto iniciara Plone en modo de depuración. A su vez mostrara el numero de
puerto por el cual Plone se esta ejecutando; por defecto es el puerto 8080.
Usted sabrá que la instancia de Plone ha terminado la iniciación y esta listo
cuando se muestre el siguiente mensaje en la terminal **"INFO Zope Ready to
handle requests"** (Información Zope preparado para manejar solicitudes).

Para detener Plone, simplemente use *CTRL-C* en su ventana de Símbolo de
sistema.


Iniciar Plone como un servicio
------------------------------

Si quisiera que Plone se inicie como un servicio al momento de iniciar su
computadora necesitara efectuar un CD al directorio de su instalación, luego
ingrese el siguiente comando en la ventana de Símbolo de sistema:
``bin\\instance install``. Esta acción instalara un nuevo servicio que a su vez
se mostrara en la Consola de Administración de Servicios. Estará listada
como: "Zope instance at C:\\Program Files\\Plone\\parts\\instance.exe", por
supuesto si hizo la instalación en ``C:\\Program Files\\Plone``.

Luego de que el servicio ha sido instalado inmediatamente puede iniciar Plone
escribiendo el siguiente comando en su venta de Símbolo de sistema :
``bin\\instance.exe start``, o utilice el Controlador de Plone (visto
anteriormente).

En el caso de que quiera remover este servicio, use el comando CD al
directorio de su instalación y luego ingrese lo siguiente: ``bin\\instance.exe remove``.


Accediendo a Plone
------------------

Quizás tenga que transmitirle a su Firewall (cortafuegos) que abra el puerto
8080, antes de que pueda acceder a la interfaz web de Plone.

Abra un navegador web y vaya a http://localhost:8080/. Haga clic en el botón
que contiene el texto "Create a new Plone site" (Crear un nuevo sitio Plone)
Se le pedirá que introduzca el nombre de usuario y contraseña: aquellos que
escribió anteriormente.

Otórguele a su sitio una identificación como "Plone", y un titulo como "Mi
sitio Plone". Además puede seleccionar el idioma del sitio y algunos
productos adicionales para su instalación. Luego haga clic en el botón "Add
Plone Site" (Agregar nuevo sitio Plone) cerca del final de la pagina. Tomara
unos segundos crear su sitio Plone

Después de que su sitio se haya creado puede acceder a el mediante esta URL:
*http://localhost:8080/Plone*, donde "Plone" es la identificación de su
sitio.

.. links:
.. _este documento: http://plone.org/documentation/kb/using-buildout-on-windows
.. _Catapult Solutions: www.catapultsolutions.net

