==============
 Herramientas
==============

Esta página contiene una lista de las herramientas que se utilizarán para el desarorllo del proyecto integrado; así como las intrucciones necesarias para su instalación y configuración. Por cada herramienta se proporciona una breve descripción de la misma y se detalla las acciones que el alumno deberá realizar para configurar dicha herramienta de cara a la correcta realización del proyecto.

ScrumDesk
==========

`Scrumdesk <https://www.scrumdesk.com/>`_ es una herramienta para la gestión de proyectos Scrum. ScrumDesk ofrece las siguiente facilidades:

  * Especificación y seguimiento de *Historias de Usuario*.
  * Definición y gestión de *products backlogs* y *sprint backlogs*.
  * Definición y gestión de tareas.
  * Monitorización de las tareas mediante tablero *Kanban*.
  * Visualización del estado actual de un proyecto mediante *Burndown Chart*.

Acciones Requeridas
--------------------

Scrumdesk es una herramienta web, por lo que no es necesario instalar nada. Cada alumno deberá simplemente abrirse una cuenta en ScrumDesk. Para poder hacer uso de la licencia académica de la cual disponemos, cada alumno, al abrir su cuenta, deberá incorporarse a la organización ``University of Cantabria``.

.. warning:: El nombre de la organización es ``University of Cantabria``, en inglés y no ``Universidad de Cantabria`` (en castellano).

Además, antes del inicio del proyecto, un miembro del equipo, que ejercerá de administrador de Scrumdesk, deberá:

  #. Crear un proyecto que se llame igual que el equipo al que pertenece;
  #. Añadir todos los miembros del correspondiente equipo (con el rol de Scrum Master).
  #. Añadir el *Product Owner* asignado a su equipo.
  #. El profesor responsable de la asignatura de Métodos de Desarrollo.

Recursos
---------

  * `Cómo registrarse en ScrumDesk <../misc/notAvailable.html>`_.
  * `Cómo crear un proyecto en ScrumDesk <../misc/notAvailablenotAvailable.html>`_.
  * `Cómo añadir miembros a un proyecto Scrumdesk <../misc/notAvailablenotAvailable.html>`_.

Git
====

`Git <https://git-scm.com/>`_ es un popular sistema de control de versiones, ampliamente utilizado en la actualidad. La instalación de Git permite utilizar dicho control de versiones sólo desde línea de comandos, siendo necesario instalarse un cliente gráfico si se quiere utilizar Git en modo ventana y no en modo consola.

Acciones Requeridas
--------------------

Cada alumnos deberá instalar Git en su computadora personal y comprobar que éste funciona correctamente. Además se recomienda encarecidamente que haya realizado los tutoriales impartidos en la asignatura de Métodos de Desarrollo.

GitHub
=======

`GitHub <https://github.com/>`_ es un popular sistema de alojamiento en la web de repositorios Git. GitHub ofrece además una serie de facilidades para la gestión de los proyectos asociados a cada repositorio que aloja. Por ejemplo,
Github ofrece una serie de facilidades para la gestión de peticiones de mantenimiunto asociadas a un determinado repositorio, o la posibilidad de interconexión automática de los repositorios con sistemas de integración continua.

GitHub permite a cualquier persona crear y alojar de manera gratuita un repositorio Git en su sistema, siempre y cuando dicho repositorio sea público. Si se quiere que dicho repositorio sea privado, habría que pagar entonces por el alojamiento. No obstante, GitHub tiene un paquete académico, denominado  `Student Pack <https://education.github.com/pack>`_ que permite a aquellos alumnos que se inscriban en él crear repositorios privados, además de otras numerosas ventajas.

Acciones Requeridas
--------------------

Cada alumno deberá disponer de una cuenta en GitHub.

Además, antes del inicio del proyecto, un miembro del grupo, que ejercerá como administrador GitHub, creará un repositorio inicial de pruebas y añadirá a dicho repositorio como colaboradores al resto de los miembros del grupo. Cada miembro del grupo deberá comprobar que es capaz de acceder desde su computadora personal a dicho repositorio tanto para lectura como para escritura.

Finalmente, el administrador GitHub creará un repositorio inicial privado que sirva para el desarrollo del proyecto, con un nombre significativo con respecto a su grupo, y añadirá como colaboradores al resto de mimebros de su equipo.

Recursos
---------

  * `Cómo registrarse en GitHub <../misc/notAvailable.html>`_.
  * `Cómo crear un repositorio privado en GitHub <../misc/notAvailablenotAvailable.html>`_.
  * `Cómo añadir colaboradores a un repositorio GitHub <../misc/notAvailablenotAvailable.html>`_.

Travis
=======

`Travis <https://travis-ci.org/>`_ es un entorno de integración continua muy popular dentro la comunidad de desarrollo de software libre. Travis se integra con GitHub y
permite su utilización gratuita y sin restricciones sobre repositorios públicos de GitHub. Si se desea trabajar sobre repositorios privados, es necesario contratar algún plan de pago. No obstante, aquellos alumnos que estén registrados en el programa `Student Pack <https://education.github.com/pack>`_ de GitHub tienen la posibilidad de utilizar GitHub sobre repositorios privados.

Acciones Requeridas
--------------------

.. todo:: Perguntar a Carlos.

SourceTree/GitKraken
=====================

.. note:: La utilización de estas herramientas es opcional, no siendo estrictamente necesarias para el desarrollo del proyecto. No obstante, se recomienda su instalación y utilización ya que facilitan enormenente ciertas tareas relacionadas con la gestión de repositorios Git, como la visualización de su estructura de ramificación.

`SourceTree <https://www.sourcetreeapp.com/>`_ y
`GitKraken <https://www.gitkraken.com/>`_ son dos clientes gráficos altamente populares para la gestión de repositorios Git. Ambos clientes ofrecen versiones gratuitas cuyas funcionalidades son suficientes para el desarrollo del proyecto.

SourceTree es la opción preferida de muchos desarrolladores por su intuitividad y simpleza. SourceTree ofrece versiones para Windows y Mac, pero no para Linux, por lo que aquellos alumnos que quieran trabajar desde Linux y quieran utilizar un cliente gráfico de Git, deberán utilizar GitKraken.

Recursos
---------

  * `Gestión de repositorios Git con SourceTree <../misc/notAvailable.html>`_

Android Studio
===============

Entorno de Desarrollo Integrado (IDE) para la programación de aplicaciones Android.

Acción Requerida: Debe estar instalado y funcionando correctamente en la computadora personal de cada alumno. Además, se debe haber comprobado que es posible comunicarse con el repositorio remoto que se haya elegido para alojar el proyecto.

Analizador SonarQube para proyectos Android (enlace)
=====================================================

Herramienta cliente para el análisis de calidad de producto software de proyectos Android.

Acción Requerida: Debe estar instalado y funcionando correctamente en la computadora personal de cada alumno, de forma que se permita lanzar un análisis desde línea de comandos y subirlo al servidor SonarCloud.

Complemento SonarLint para Android Studio (enlace)
===================================================

Complemento que permite analizar la calidad de producto de proyectos Android Studio en base a un conjunto de reglas de calidad definidas en la organización.
Acción Requerida: Debe estar instalado y sincronizado con el servidor de la organización en SonarCloud en la computadora personal de cada alumno.


Magic Draw (enlace)
====================

Herramienta para la creación de modelos UML. El equipo docente puede proporcionar licencias gratuitas para los alumnos.

Acción Requerida: Debe estar instalado y funcionando correctamente en la computadora personal de cada alumno.

Advanced Rest Client (enlace) (opcional)
-----------------------------------------

App para Chrome que permite generar de forma cómoda e intuitiva peticiones HTTP.

Acción Requerida: Debe estar instalada y funcionando correctamente en la computadora personal de cada alumno que desee utilizarla.
