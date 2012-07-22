.. -*- coding: utf-8 -*-

=========================
Procesos de documentación
=========================

.. contents :: :local:

Obtener y compilar la documentación
===================================

El almacenamiento de este material está disponible en el repositorio Git
`collective.spanishdocumentation`_ de la cuenta `plone-es`_ en GitHub.com.

Este repositorio recoge la documentación oficial de Plone en Español
publicada en el sitio web `Plone.es`_. Tenga en cuenta que en la web
`Plone.es`_ se publica solo una parte de la documentación disponible,
puede encontrar toda la documentación que hasta el momento está traducida
al Español en la pagina http://plone-spanish-docs.readthedocs.org/en/latest/index.html
y su codigo fuente en el repositorio `collective/collective.spanishdocumentation`_
de la cuenta `Plone collective`_ en GitHub.com.

Si usted tiene unas credenciales en este servidor y desea convertirse en
un colaborador ejecute el siguiente comando:

.. code-block:: sh

  $ git clone git@github.com:plone-es/collective.spanishdocumentation.git

Si usted no tiene las credenciales de acceso al repositorio Git
`collective.spanishdocumentation`_ en la cuenta de `plone-es`_
en GitHub.com o simplemente solo desea obtener y compilar esta
documentación ejecute el siguiente comando:

.. code-block:: sh

  $ git clone git://github.com/plone-es/collective.spanishdocumentation.git

Crear entorno virtual de Python para reconstruir este proyecto:

.. code-block:: sh

  # aptitude install git-core build-essential python-dev python-setuptools texlive-full
  # easy_install virtualenv
  $ cd $HOME ; mkdir $HOME/virtualenv ; cd $HOME/virtualenv
  $ virtualenv --python=/usr/bin/python sphinx
  $ source virtualenv/sphinx/bin/activate

Ahora puede generar la documentación de HTML, con los siguiente comandos:

.. code-block:: sh

  (sphinx)$ cd collective.spanishdocumentation/
  (sphinx)$ python bootstrap.py
  (sphinx)$ ./bin/buildout -vN
  (sphinx)$ ./bin/sphinx

Ahora se puede abrir ``collective.spanishdocumentation/build/html/index.html`` desde
su navegador Web favorito.

Para obtener la documentación en PDF:

.. code-block:: sh

  (sphinx)$ cd ./collective.spanishdocumentation/build
  (sphinx)$ make latex
  (sphinx)$ make latexpdf

Ahora se puede abrir ``collective.spanishdocumentation/sphinx/build/latex/DocumentacionEspanolPlone.pdf``
con sus programas de visor de PDF favorito (Evince, Acrobat Reader, ...)


Reglas de redacción
===================

En primer lugar, debe aprender los `fundamentos de Sphinx`_ que es un reStructuredText extendido.


Codificación de caracteres
==========================

Su editor debe codificar el texto en **utf-8** si le gusta lo que está leyendo.
Si su editor de texto favorito no reconoce esta codificación
(en la actualidad, eso es bien extraño), entonces cambie de editor de texto.

.. admonition::
   Truco

   Para ``vi``, ``emacs`` y algunos otros editores de texto soportan
   utf-8 de forma automática al abrir un archivo de Sphinx, el lugar en
   primera línea de la siguiente marca (como en este archivo)::

     .. -*- coding: utf-8 -*-


Desplazamientos y indentaciones
===============================

El uso del carácter de tabulación en el texto fuente para las distintas
desplazamientos y indentaciones está **estrictamente prohibido**. Utilice siempre
espacios para este fin. Todos los editores de texto ofrecen opciones avanzadas
para insertar espacios al pulsar la tecla TAB. No tiene
excusa si es necesario.

Estilos de subrayado
====================

Sphinx y ReStructuredText no imponer estilo de subrayado para
diferentes niveles de secciones de un documento. Todo se deja a la discreción
editores. Para mantener la coherencia nosotros adoptamos la siguiente convención: ::

  ==============================================
  Titulo de capitulo (uno solo por cada archivo)
  ==============================================
  ...
  Sección del nivel 1
  ===================
  ...
  Sección del nivel 2
  -------------------
  ...
  Sección del nivel 3
  ...................
  ...
  Sección del nivel 4
  ~~~~~~~~~~~~~~~~~~~
  ...
  Sección del nivel 5
  :::::::::::::::::::
  ...
  Sección del nivel 6
  *******************
  ...
  Sección del nivel 7
  +++++++++++++++++++

No es necesario ni deseable ir más allá del nivel 4. Cuando la generación del
documento allá completado, el nivel de las secciones básicas de un archivo
depende del nivel de anidamiento del archivo en la estructura general de
documento. Para generar el HTML, no es un problema, pero en LaTeX limita
la superposición de las secciones a 6 niveles.

Contribuciones
==============

Wow, estás contento con tu excelente trabajo. Y le gustaría compartirlo con
todo el mundo. Al igual que cuando "contribuidor" de código fuente, las pruebas
unitarias no deben mostrar ningún error, compruebe en primer lugar:

* Que el comando ``make html`` no genere ningún error o advertencia.
* Que su redacción no posea ningún error de ortografía.
* Los enlaces de hipertexto que se ha agregado o cambiado (glosario, enlaces
  externos explícitos, referencias a las secciones, ...) funcionan correctamente.

Imágenes
========

Aparte de las capturas de pantalla - ¡Uy, lo siento - las capturas de pantalla!,
las imágenes Sphinx se inserta en el documento debe ir acompañada de su versión
"Fuente" en un formato público interoperables, y para que el editor pueda abrir
el archivo fuente que este disponible. Las imágenes deben estar preferentemente en el formato
PNG.

Además, durante cada inserción o cambio de imagen, usted **debe**
verificar y ajustar si es necesario la representación PDF, a sabiendas de las limitaciones
la imagen a tamaño del papel final.

**Ejemplo :** ::

   .. gs-map.mm: imagen de mapa mental de los servicios de GenericSetup. Creado con FreeMind

   .. image:: gs-map.png
      :align: center
      :alt: imagen de mapa mental de los servicios de GenericSetup

   .. figure::  screenshot.jpg
      :align:   center
      :alt: Captura de pantalla del programa de mapa mental


**Aplicaciones gráficas recomendadas**

Diagramas : `Graphviz`_


Ejemplos de documentación en Sphinx
===================================

* `Python documentation`_
* `Zope documentation`_
* `Plone Developer Documentation`_
* `D:YAML documentation`_


Algunas de las herramientas recomendadas
========================================

Emacs : usted puede agregar a emacs el módulo `rst.el
<http://svn.berlios.de/svnroot/repos/docutils/trunk/docutils/tools/editors/emacs/rst.el>`_
que añade un par de comandos y la sintaxis de la documentación a los escritores
simpatizantes de Sphinx y reStructuredText.

Subir la documentación a un sitio web Plone
===========================================

Esta documentación se puede subir a un sitio web Plone gracias al
programa `funnelweb`_. A continuación se demuestra como hacerlo en
nuestro entorno de desarrollo.

Antes de todo hay que iniciar el servidor y crear un sitio Plone.

.. code-block:: sh

  (sphinx)$ cd collective.spanishdocumentation/
  (sphinx)$ ./bin/instance start

1. Navegue a su instancia visitando http://localhost:8080 en su navegador web.
   Si usted estableció otro puerto, use ese en vez del *8080*.
2. Haga clic en "Create a new Plone site" (Crear un nuevo sitio Plone) e
   introduzca su información de inicio de sesión para comenzar a usar Plone.
3. Introduzca la información requerida, en nuestro caso usaremos el nombre **Plone**,
   luego envíe el formulario para finalizar la creación de su sitio.
4. Usted puede ahora encontrar su sitio en http://localhost:8080/Plone.
5. Ahora debe agregar una nueva carpeta llamada *Documentación* en la raiz del sitio
   en la que añadiremos la documentación en html creada con Sphinx.

El sitio Plone está ahora listo para recibir la documentación, para hacerlo
simplemente hay que ejecutar el script ``toplone``.

.. code-block:: sh

  (sphinx)$ ./bin/toplone

Configuración de funnelweb
--------------------------

Es posible configurar el programa `funnelweb`_ editando el
fichero ``pipeline.cfg``.

Por ejemplo, para subir la documentación en otra carpeta llamada
*Manuales* o para usar un nombre de usuario y contraseña diferentes,
puede cambiar la opción de configuración ``ploneupload:target``
editando el fichero ``pipeline.cfg`` de esta manera::

    # Upload to Plone Development Server
    [ploneupload]
    target=http://administrador:mitesoro@localhost:8080/Plone/manuales

También puede resultar utíl hacer unas pruebas subiendo sólo algunas
paginas en vez de toda la documentación, por eso hay que descomentar
la opción ``crawler:max``::

    [crawler]
    max=10

Puede encontrar más información acerca de la configuración de funnelweb
en la pagina http://pypi.python.org/pypi/funnelweb.

.. note::

    Al cambiar el fichero ``pipeline.cfg`` NO es necesario volver
    ejecutar el ``buildout``, de hacerlo se perderían eventuales
    modificaciones ya que buildout genera el fichero de
    configuración a partir de la plantilla ``pipeline.in``.

FAQ
===

**Pregunta :** He añadido una entrada del índice o un nuevo término en el glosario y
no se actualiza cuando compilo el documento.

**Respuesta :** El índice de Sphinx es a veces es desorientado y la gestión de la dependencia
a veces, mejor. Por lo tanto, todo se debe reiniciar ejecutando el comando ``make clean``
dentro del directorio ``collective.spanishdocumentation/sphinx/build/``.


.. links:
.. _collective.spanishdocumentation: https://github.com/plone-es/collective.spanishdocumentation
.. _plone-es: https://github.com/plone-es
.. _`Plone.es`: http://plone.es/documentacion
.. _`collective/collective.spanishdocumentation`: https://github.com/collective/collective.spanishdocumentation
.. _`Plone collective`: https://github.com/collective
.. _fundamentos de Sphinx: http://sphinx.pocoo.org/contents.html
.. _Graphviz: http://www.graphviz.org/
.. _Python documentation: http://docs.python.org/
.. _Zope documentation: http://docs.zope.org/zope2/index.html
.. _Plone Developer Documentation: http://collective-docs.plone.org/
.. _D\:YAML documentation: http://dyaml.alwaysdata.net/static/html/doc_0.4/index.html
.. _rst.el: http://svn.berlios.de/svnroot/repos/docutils/trunk/docutils/tools/editors/emacs/rst.el
.. _`funnelweb`: http://plone.org/products/funnelweb/

