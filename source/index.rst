.. -*- coding: utf-8 -*-

=========================================
Documentación oficial de Plone en Español
=========================================

Esta sección intenta recoger todo la documentación que hasta el momento 
esta traducida al Español, como resultado de la iniciativa llamada 
*traducciones plone* creada en 2008 en el sitio CoActivate.org por miembros 
de la comunidad Plone Conosur. A continuación se listan los documentos 
traducidos hasta el momento:


Instalación de Plone
====================

Este sección se dedica a recopilar las diversas formas de instalación de Plone 
en diversos Sistemas operativos como Windows, OS X, Linux, BSD (distribución de 
software Berkeley) y prácticamente cualquier otra plataforma.

.. toctree::
   :maxdepth: 1

   manuales/instalando_plone


Uso de Plone
============

Plone es un Sistema de gestión de contenidos muy completo y útil,
por lo que es muy importante conocerlo para poder tomar máxima ventaja de
estos CMS.  

En esta sección tenemos el tutorial traducción oficial a los manuales de usuario 
y administración de elementos de Plone.

.. toctree::
   :maxdepth: 1


   Manual de Usuario de Plone 3 <manuales/usando_plone3/index>
..
   Manual de Usuario de Plone 2.5 (En proceso) 
   Manual de Usuario de Plone 4 (En proceso) 


Desarrollo en Zope/Plone
========================

Plone es un Sistema de gestión de contenidos muy completo y útil,
por lo que es muy importante conocer las técnicas y tecnologías que 
agilicen nuestro desarrollo.

.. toctree::
   :maxdepth: 1

   plone/apariencias/index
   Realizando pruebas en Plone <plone/haciendo-pruebas/index>


==========================
Mejores Practicas de Plone
==========================

Esta sección intenta recoger todo la documentación disponible en en Español, 
sobre las *Mejores Practicas de Plone*, esta es resultado de la iniciativa de 
*Carlos de la Guardia* que publica esta documentación en busca de promover la 
documentación en Español, desde entonces esta documentación es mantenida por 
miembros de la comunidad Plone Conosur. A continuación se listan los documentos 
traducidos hasta el momento:

Introducción
============

Desarrollar un sitio con Plone requiere de la combinación de una serie de
tecnologías y conocimientos, desde HTML hasta desarrollo avanzado con Python.
A lo largo del tiempo, la comunidad de Plone ha ido experimentando y
adoptando diversas formas de trabajar un proyecto, las cuales hoy en día
pueden considerarse como las mejores practicas de desarrollo con Plone.

Algunas de estas practicas se refieren por supuesto a la programación con
Python y a la construcción de aplicaciones administración de contenido con
Plone, pero hay algunas otras que rebasan el ámbito de Plone y son útiles
para cualquier ambiente de desarrollo.

En este texto vamos a abordar una por una diversas practicas que consideramos
invaluables para el trabajo profesional con Plone. La intención es demostrar
la manera en que se integra un ambiente de desarrollo ideal para desarrollar
con Plone.

Además de las mejores practicas, conoceremos en detalle algunas de las
principales tecnologías de Zope y Plone.

En particular, conoceremos:


Tutorial de control de versiones
================================

Para tener un ambiente de desarrollo productivo, en especial cuando se
trabaje en equipo, es muy importante contar con un sistema de control de
versiones. ``Subversion`` es el utilizado por plone.org y el plone collective,
por lo que consideramos necesario conocerlo, aunque recientemente la
popularidad de sistemas distribuidos como ``Git``, ``Mercurial`` y ``Bazaar`` 
ha aumentado.

.. toctree::
   :maxdepth: 1

   rcs/subversion
   Control de versiones utilizando Git <http://www-cs-students.stanford.edu/~blynn/gitmagic/intl/es/index.html>
   Control de versiones utilizando Mercurial <http://mercurial.selenic.com/wiki/SpanishTutorial>
   Control de versiones utilizando Bazaar <http://blog.malev.com.ar/tutorial-de-bazaar/>

Python
======

Python es el lenguaje con el que están desarrollados tanto Zope como Plone,
por lo que es muy importante conocerlo para poder tomar máxima ventaja de
estos sistemas. Es imprescindible programar en Python para poder crear
productos y tipos de contenido para Plone.

En esta sección tenemos el tutorial oficial de Python, preparado por la
asociación de Python de Argentina y la fundación de Python.

.. toctree::
   :maxdepth: 1

   Tutorial de Python <python/tutorial-usla/index>


Inmersión al modo interactivo de Python
---------------------------------------

La idea de este tutorial es que alguien que **NUNCA** ha trabajando con el
interprete de `Python`_ pueda tener un primer acercamiento **SIN
PROGRAMAR**, solamente con conocer el uso del interprete y sus comandos
básicos.

.. _Python: http://www.python.org/

.. toctree::
   :maxdepth: 2

   python/una_pequena_inmersion_python


Entornos virtuales en Python
----------------------------

Python ofrece un mecanismo para poder experimentar con nuevas versiones de 
librerías Python en formato Egg, sin afectar su sistema, o para crear un 
entorno de instalación Python aislado al Python de su sistema operativo, por 
eso está sección que se dedica a explicar sus casos de uso.

.. toctree::
   :maxdepth: 2

   python/creacion-de-entornos-virtuales-python


Setuptools / Distribute
-----------------------

Python ofrece un sistema de paquetes para aplicaciones Python en formato Egg, 
para la cual posee dos especificaciones de como hacer paquetes Egg y sus respectivas
utilidades para la gestión de estos paquetes, por eso está sección que se dedica a 
explicar sus diferencias.

.. toctree::
   :maxdepth: 1

   python/setuptools
   python/distribute-y-pip


Esqueletos de proyectos
-----------------------

Como parte de la filosofía de desarrollo ágil de aplicaciones, varios proyectos 
Python ofrecen mecanismo de plantilla de proyectos y tipos de módulos que cumplen 
con las buenas practicas implementadas en sus proyectos.

.. toctree::
   :maxdepth: 1

   python/skel-proyectos-python
   python/skel-proyectos-plone


Buildout y sus complementos
===========================

Buildout es un sistema que permite definir ambientes de desarrollo
que pueden ser replicados, incluyendo dependencias y configuración. Buildout 
se apoya fuertemente en setuptools, que permite instalar paquetes de Python 
a través de Internet. Es recomendable utilizar buildout para cualquier proyecto 
de Plone que se quiera emprender.

.. toctree::
   :maxdepth: 1

   buildout/replicacion-de-proyectos-python
   buildout/hola-mundo-en-zc-buildout
   buildout/recipes-buildout
   buildout/programar-tareas-con-crontab
   buildout/rotar-archivos-log
   buildout/plone3
   buildout/plone-esquema-alta-disponibilidad


Administración de Zope
======================

Plone esta basado en el servidor de aplicaciones Zope y este requiere realizar 
tareas de hospedaje y administrativa para un servidor de aplicación Zope / 
sitio de Plone.

.. toctree::
   :maxdepth: 1

   zope/cli-zope
   zope/configuraciones-generales
   zope/configurar-zope-plone-como-demonio
   zope/zope-como-servidor-ftp
   zope/zope-como-servidor-webdav
   zope/puntos-montaje-zodb-sitios-plone
   zope/compactar-zodb
   zope/importar-exportar-plone
   zope/instancia-debug-zope
   zope/zope-plone-detras-servidor-web

Tecnologías de Zope
-------------------

Plone esta basado en el servidor de aplicaciones Zope y en un toolkit de
desarrollo de portales llamado CMF. Para trabajar con Plone es necesario
conocer diversas tecnologías provenientes de estos sistemas.

.. toctree::
   :maxdepth: 1

   zope/zca/zca-es
   zope/zpt
   zope/zcatalog
   zope/workflow
   zope/gs


Temáticas diversas de Plone
===========================

Existen muchos temas importantes para el desarrollo con Plone, en esta
sección tocaremos algunos de ellos.

.. toctree::
   :maxdepth: 1

   plone/productos
   plone/policy
   plone/tema
   plone/productos-adicionales/index
   plone/tutoriales/index

Otros recursos
--------------

.. toctree::
   :maxdepth: 2

   links
   presentaciones


Acerca de esta documentación
----------------------------

Instrucciones acerca de esta documentación.

.. toctree::
   :maxdepth: 2

   procesos_de_documentacion
   traducciones_de_contenidos


   
Índices y tablas
================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
