.. -*- coding: utf-8 -*-

1. Guía rápida de Instalación
=============================

Como instalar Plone, paso a paso. Versión corta


Linux/BSD
---------


Requisitos previos
..................

Antes de instalar Plone en Linux, BSD, o cualquier otro sistema operativo
basado en Unix, debería asegurarse que tiene los siguientes paquetes
instalados:

-   Compilador gcc, a C

-   Software g++, extensión de gcc para compilar código C++

-   GNU make, una herramienta de compilación

-   GNU tar, paquete para crear archivos tar

-   Paquetes para descomprimir: bzip2 y gzip

Los siguientes paquetes también son recomendados, pero no son necesarios para
construir Plone

-   libssl, le permite usar TSL como su servidor de correo electrónico.

-   readline, un paquete GNU que incrementa la capacidad de las
    aplicaciones para editar los comandos de Terminal.


Obtener el instalador de Plone
..............................

El instalador para Linux/BSD/Unix, denominado Unified Installer (Instalador
Unificado), se puede descargar de `esta pagina`_ en el sitio web de Plone.

1.  Haga clic en *Download Plone* (descargar Plone), y este le llevara a
    la pagina que contiene los distintos instaladores de Plone.
2.  Haga clic en el enlace Unified Installer para comenzar la descarga de
    Plone.
3.  Después que la descarga haya finalizado, abra la Terminal y cambie
    los directorios donde el archivo del instalador que usted descargo esta
    localizado.
4.  Descomprima el instalador escribiendo ``tar xzf InstallerName``, donde
    InstallerName es el nombre del instalador de Plone que usted descargo.
5.  En su Terminal de comandos introduzca el directorio de la carpeta que
    usted acaba de extraer.


Configurando su Instalación Plone
.................................

Lo primero que debe decidir al momento de instalar Plone es si quiere una
instalación ZEO o una instalación autónoma. Probablemente debería escoger ZEO
si va a usar Plone para cualquier producción. Sin embargo, si simplemente
esta probando Plone o lo va a usar para formación, la opción autónoma se
adecuaría mejor. Para un discusión mas profunda de este tema lea la
sección llamada :ref:`¿Ser ZEO o no ser ZEO? <ser-zeo-o-no-ser-zeo>`.

Para comenzar la instalación escriba ``./install.sh method`` donde *method* es
"standalone" (autónoma) o "zeo". Si desea instalar Plone en modo servidor
escriba ``sudo ./install.sh method`` o ejecute el script de instalación
como root de alguna otra manera. una lista completa de opciones de lineas de
comando la puede encontrar `aquí`_.


Últimos pasos
.............

Cercano del final de la instalación, el instalador debió haber mostrado su
nombre de usuario y contraseña para su instalación Plone en la Terminal. Si
tiene problemas encontrándolos, estos están también listados en un archivo de
texto llamado ``adminPassword.txt`` (el cual se puede encontrar en la carpeta
``zinstance`` de la instalación de Plone).

Para iniciar Plone:

1.  Haga un "cd" al directorio de su instalación Plone.
2.  Entre en su carpeta zinstance.
3.  Ejecute ``./bin/plonectl start``. (El puerto que usa Plone se puede
    ajustar en buildout.cfg para luego ejecutar ``./bin/buildout``).
4.  Navegue a su instancia visitando http://localhost:8080 en su
    navegador web. Si usted estableció otro puerto, use ese en vez del
    *8080*.
5.  Haga clic en "Create a new Plone site" (Crear un nuevo sitio Plone) e
    introduzca su información de inicio de sesión para comenzar a usar Plone.
    Introduzca la información requerida y luego envié el formulario para
    finalizar la creación de su sitio. Usted puede encontrar su sitio en
    http://localhost:8080/*SiteName*, donde **SiteName** es la identificación
    de su sitio Plone.

Para detener el proceso Plone ejecute ``./bin/plonectl stop``. ¡Diviértase
usando Plone!


OS X
----

Si usted quiere usar Plone en un escritorio Mac, el instalador binario OS X
es una buena opción. Este proporciona el instalador para OS X y contiene un
controlador visual. Sin embargo, ya que provee binarios pre-compilados, es
muy difícil agregar nuevos componentes que requieran construcciones binarias.
Si usted tiene la necesidad realizar esa acción, pues entonces agregue XCode
a su sistema y use el instalador Unificado.


MS Windows (2000, 2003, XP, Vista, 7)
-------------------------------------


Obtener Plone
.............

Puede descargar Plone para Windows de `esta pagina`_.

1.  Haga clic en el botón **Download Plone** (Descargar Plone).
2.  Haga clic en el enlace para el instalador de Windows y guárdelo en
    una locación que sea fácil de recordar tal como su Escritorio.
3.  Haga doble-clic en el instalador para iniciar el proceso de
    instalación.


Asistente de instalación de Plone
.................................

1.  Introduzca el directorio donde le gustaría instalar Plone. La mayoría
    de personas están de acuerdo con la ubicación predeterminada. (Haga clic
    en "Next" (Siguiente) al finalizar cada paso para continuar)
2.  Introduzca el nombre de usuario y contraseña que desee para la cuenta
    del administrador.
3.  Revise las opciones de configuración actual.
4.  Durante el proceso de instalación una barra mostrara que tan cerca
    esta la instalación de completarse.  Marque las casillas de confirmación
    para determinar si usted quiere agregar Plone como un servicio para que
    se inicie automáticamente con el inicio de Windows.

    .. note::
        esto se puede cambiar en cualquier momento ejecutando ``bin\\instance.exe remove`` en su
        directorio de instalación o si desea ejecutar Plone después de que la
        instalación haya culminado.


Iniciando Plone
...............

Si usted decidió no hacer de Plone un servicio, usted lo puede iniciar y
detener a través del directorio de Plone en su linea de comandos y a
continuación ejecutar:

.. code-block:: sh

    bin/instance.exe fg

o mediante el uso del Controlador GUI (interfaz gráfica de usuario) de Plone.

El Controlador de Plone se puede encontrar en su menú de Inicio -> Todos los
programas -> Plone -> Plone Controller. Este se usa para modificar la
configuración de Plone, así como para iniciarlo o detenerlo. Ahora si usted
decide hacer de Plone un servicio ejecute:

.. code-block:: sh

    bin/instance.exe install

Del mismo modo, para la desinstalación ejecute:

.. code-block:: sh

    bin/instance.exe remove

Una vez que usted haya iniciado una instancia de Plone, la puede ver
visitando http://localhost:8080 en su navegador web. Si no se carga,
asegúrese de que su Firewall no ha bloqueado el puerto TCP 8080.

Haga clic en "Create a new Plone site" (Crear un nuevo sitio Plone) e
introduzca su información de inicio de sesión para comenzar a usar Plone.
Ingrese la información solicitada y luego envié el formulario para finalizar
la creación de su sitio. Puede encontrar su sitio en
http://localhost:8080/*SiteName*, donde **SiteName** es la identificación de su
sitio Plone. ¡Diviértase con Plone!


.. links:
.. _esta pagina: http://plone.es/descubre/descarga-plone
.. _aquí: http://plone.org/documentation/kb/installing-plone-with-the-unified-installer/command-line-options

