==============
 Herramientas
==============

Esta página contiene una lista de las herramientas que se utilizarán para el desarrollo del proyecto integrado; así como las instrucciones necesarias para su instalación y configuración. Por cada herramienta se proporciona una breve descripción de la misma y se detalla las acciones que el alumno deberá realizar para configurar dicha herramienta de cara a la correcta realización del proyecto.

ScrumDesk
==========

`Scrumdesk <https://www.scrumdesk.com/>`_ es una herramienta para la gestión de proyectos Scrum. ScrumDesk ofrece las siguientes facilidades:

  * Especificación y seguimiento de *Historias de Usuario*.
  * Definición y gestión de *Products Backlogs* y *Sprint Backlogs*.
  * Definición y gestión de tareas.
  * Monitorización de las tareas mediante tablero *Kanban*.
  * Visualización del estado actual de un proyecto mediante *Burndown Chart*.

ScrumDesk es una herramienta de pago para la que disponemos de una licencia académica que nos permite utilizarla gratuitamente.

Acciones Requeridas
--------------------

Scrumdesk es una herramienta web, por lo que no es necesario instalar nada. Cada alumno deberá simplemente abrirse una cuenta en ScrumDesk. Para poder hacer uso de la licencia académica de la cual disponemos, cada alumno, al abrir su cuenta, deberá incorporarse a la organización ``University of Cantabria``.

.. warning:: El nombre de la organización es ``University of Cantabria``, en inglés y no ``Universidad de Cantabria``, en castellano.

Además, antes del inicio del proyecto, un miembro del equipo, que ejercerá de administrador de Scrumdesk, deberá:

  #. Crear un proyecto que se llame igual que el equipo al que pertenece;
  #. Añadir todos los miembros del correspondiente equipo (con el rol de ``Scrum Master``).
  #. Añadir el *Product Owner* asignado a su equipo (con el rol de ``Product Owner``).
  #. El profesor responsable de la asignatura de Métodos de Desarrollo (con el rol de ``Product Owner``).

Recursos
---------

  * `Cómo añadir miembros a un proyecto Scrumdesk <https://youtu.be/AHn4nkAC7ig>`_.

Slack/Discord
==============

`Slack <https://slack.com/>`_ y `Discord <https://discord.com/>`_ son  herramientas para facilitar la comunicación asíncrona dentro de un equipo de trabajo. Ambas herramientas siguen un estilo de comunicación parecido al de los chats, favoreciendo la comunicación remota, distribuida y asíncrona. 

Slack es ampliamente utilizado a nivel profesional, ofrece la posibilidad de integración con múltiples herramientas comúnmente utilizadas dentro del mundo del desarrollo software (e.g. Travis o Trello, entre otros). Discord está más orientada al mundo de los videojuegos, que es donde nace, pero tiene cada vez más aceptación a nivel profesional. Slack proporciona algunas funciones que permiten ordenar mejor las comunicaciones dentro de un canal de texto, haciendo que canales con muchas personas sean más fácilmente gestionables. Por otro lado, Discord ofrece canales de voz para comunicación síncrona, característica que no está incluida de manera nativa en Slack, mucho más orientado a la comunicación asíncrona.

Acciones Requeridas
--------------------

Un miembro de cada equipo Scrum, que ejercerá como *administrador Slack/Discord* deberá crear un *espacio de trabajo* propio en Slack, o un servidor en Discord, y añadir a dicho espacio de trabajo o servidor al resto de  miembros de su equipo.


.. .. note:: El equipo docente de la asignatura recomienda la utilización de Slack como  herramienta de comunicación remota al ser ésta la de mayor aceptación a nivel empresarial. No obstante, si todo el equipo de trabajo estuviese de acuerdo, pueden utilizarse alternativas como `Discord <https://discordapp.com/>`_.

Git
====

`Git <https://git-scm.com/>`_ es un popular sistema de control de versiones, ampliamente utilizado en la actualidad. La instalación de Git permite utilizar dicho control de versiones sólo desde línea de comandos, siendo necesario instalarse un cliente gráfico si se quiere utilizar Git en modo ventana y no en modo consola.

Acciones Requeridas
--------------------

Cada alumno deberá instalar Git en su computadora personal y comprobar que éste funciona correctamente. Además se recomienda encarecidamente que haya realizado los tutoriales impartidos en la asignatura Métodos de Desarrollo.

GitHub
=======

`GitHub <https://github.com/>`_ es un popular sistema de alojamiento en la web de repositorios Git. GitHub ofrece además una serie de facilidades para la gestión de los proyectos asociados a cada repositorio que aloja. Por ejemplo,
Github ofrece una serie de facilidades para la gestión de peticiones de mantenimiento asociadas a un determinado repositorio, o la posibilidad de interconexión automática de los repositorios con sistemas de integración continua.

GitHub permite a cualquier persona crear y alojar de manera gratuita un repositorio Git en su sistema, siempre y cuando dicho repositorio sea público. Si se quiere que dicho repositorio sea privado, habría que pagar entonces por el alojamiento. No obstante, GitHub tiene un paquete académico, denominado  `Student Pack <https://education.github.com/pack>`_ que permite a aquellos alumnos que se inscriban en él crear repositorios privados, además de otras numerosas ventajas.

Acciones Requeridas
--------------------

Cada alumno deberá disponer de una cuenta en GitHub y proporcionar su nombre de usuario a los docentes.

Antes del inicio del proyecto, el equipo docente creará un repositorio inicial para cada equipo de trabajo dentro de la organización `isunican`_.
El propio equipo docente añadirá a cada repositorio como colaboradores a los miembros del correspondiente *Scrum Team*, siendo por tanto la única responsabilidad de los alumnos  comprobar que son capaces de acceder desde su computadora personal a dicho repositorio tanto para lectura como para escritura.

GitHub Actions
=======

`GitHub Actions <https://docs.github.com/en/actions>`_ es un entorno de integración continua proporcionado por GitHub, que permite su utilización gratuita y sin restricciones sobre repositorios públicos de GitHub. Si se desea trabajar sobre repositorios privados, hay un límite de minutos que se pueden utilizar de forma gratuita. A partir de ese límite, es necesario contratar algún plan de pago.

Acciones Requeridas
--------------------

Los docentes proporcionarán la configuración necesaria para realizar la integración continua del repositorio inicial. Esto incluye la parte de configuración del servidor y el fichero local de configuración ``.travis.yml``.

Los alumnos deberán comprobar que se realiza la integración continua de su proyecto inical de forma satisfactoria. Para ello deberán subir algún cambio al repositorio github (en la rama ``master`` o ``develop``) y comprobar el resultado de la integración en la organización de Travis `isunican <https://travis-ci.org/isunican>`_.

SourceTree/GitKraken/SmartGit
==============================

.. note:: La utilización de estas herramientas es opcional, no siendo estrictamente necesarias para el desarrollo del proyecto. No obstante, se recomienda su instalación y utilización ya que facilitan enormemente ciertas tareas relacionadas con la gestión de repositorios Git, como la visualización de su estructura de ramificación.

`SourceTree <https://www.sourcetreeapp.com/>`_,
`GitKraken <https://www.gitkraken.com/>`_y
`SmartGit <https://www.syntevo.com/smartgit/>`_ son tres clientes gráficos bastante populares para la gestión de repositorios Git. Todos estos clientes ofrecen versiones gratuitas cuyas funcionalidades son suficientes para el desarrollo del proyecto.

SourceTree es la opción preferida de muchos desarrolladores por su simpleza y facilidad de uso. SourceTree ofrece versiones para Windows y Mac, pero no para Linux. Para aquellos alumnos que quieran trabajar desde Linux, la opción recomendada inicial sería GitKraken. No obstante, GitKraken, en su versión gratuita, no permite trabajar con repositorios privados, por lo que si algún grupo optase por utilizar dicha opción, la opción recomendada para los alumnos que trabajen desde Linux sería SmartGit en lugar de GitKraken.

..    Recursos
    ---------

    * `Gestión de repositorios Git con SourceTree <../misc/notAvailable.html>`_

Android Studio
===============

`Android Studio <https://developer.android.com/studio/>`_ es el entorno de desarrollo integrado (IDE) más comúnmente utilizado para el desarrollo de aplicaciones Android. Incluye funcionalidades específicas para el desarrollo de este tipo de aplicaciones tales como diseñadores de interfaces gráficas móviles o ejecución de las aplicaciones en  emuladores.

Acción Requerida
-----------------

Cada alumno deberá instalar Android Studio en su computadora antes del comienzo del desarrollo del proyecto. Además, deberá comprobarse que dicha instalación funciona correctamente y el alumno es capaz de compilar, ejecutar y empaquetar una aplicación Android básica.

SonarQube para proyectos Android
=================================

Herramienta para el análisis de calidad de producto software de proyectos Android. Cuenta con una parte servidor alojada en `sonarcloud <https://sonarcloud.io>`_  donde consultar el resultado de los informes y con una parte cliente donde podremos lanzar el análisis de nuestro proyecto subiendo el resultado al servidor. Además existen complementos como SonarLint que permiten integrar en nuestro IDE el análisis y gestión de las incidencias de calidad, pudiendo además sincronizar dicho complemento con nuestro servidor de modo que se utilicen las reglas definidas en nuestra organización.

.. note:: Durante el desarrollo del proyecto integrado, no será necesario que el alumno lance el analizador desde terminal, ya que en el proceso de integración continua se realiza automáticamente, tal y como está configurado en el fichero ``.travis.yml`` proporcionado en el proyecto inicial.

Acciones Requeridas
--------------------

* Los alumnos deberán ser capaces de lanzar un análisis desde línea de comandos y subirlo al servidor SonarCloud. Para ello, en el proyecto inicial se les propocionará el fichero ``gradle.build`` con la configuración necesaria, de modo que únicamente deberán ejecutar el comando ``gradlew.bat sonarqube`` o ``./gradlew sonarqube`` en la raíz del proyecto.

.. note:: Para hacer que el informe de sonar incluya la cobertura de pruebas habrá que lanzar antes ``gradlew.bat test`` para que genere los ficheros correspondientes. El resto de parámetros de configuración necesarios ya estan incluidos en el fichero ``gradle.build``.

* Los alumnos deberán comprobar que en el servidor SonarCloud, dentro de la organización `isuc <https://sonarcloud.io/organizations/isuc/projects>`_, aparece el informe del análisis que han lanzado.

* Los alumnos deberán tener instalado el complemento SonarLint para Android Studio y tener configurada la conexión con nuestro servidor de SonarCloud de modo que se utilicen las reglas de calidad definidas en nuestra organización.

.. Ninja Mock
.. ===========

.. .. note:: La utilización de esta herramienta es opcional. Se aceptarán durante el desarrollo del proyecto *mockups* realizados con cualquier otra herramienta que sea capaz de crear prototipos básicos de una interfaz de usuario, así como diseños de mockups realizados sobre papel y posteriormente escaneados.

.. `Ninja Mock <https://ninjamock.com/>`_ es una herramienta web para el diseño de *mockups*. Ninja Mock goza de cierta popularidad para el diseño de prototipos de interfaces de usuario, siendo además muy intutitivo y fácil de utilizar. NinjaMock ofrece una versión gratuita con una serie de funcionalidades básicas que son suficientes para el desarrollo del proyecto integrado.

.. Acciones Requeridas
.. --------------------

.. Los miembros de los equipos que decidan utilizar NinjaMock deberán abrirse una cuenta en dicha aplicación. Además, un miembro del equipo, que ejercerá de administrador de NinjaMock, será el responsable de crear un proyecto y añadir al resto de miembros del equipo a dicho proyecto.

..
    Recursos
    ---------

    * `Crear una cuenta en Ninja Mock <../misc/notAvailable.html>`_
    * `Crear un proyecto en Ninja Mock <../misc/notAvailable.html>`_
    * `Inivitar a un usuario a un proyecto <../misc/notAvailable.html>`_

Magic Draw
============

`Magic Draw <https://www.nomagic.com/products/magicdraw>`_ es una herramienta para la creación de modelos UML. En comparación con otras herramientas es bastante ligera, cómoda y fácil de utilizar. MagicDraw es una herramienta de pago para la que disponemos de licencia académica, la cual estará disponible a través de los cursos de Moodle de cada una de las asignaturas que conforman el proyecto integrado.

Acción Requerida
-----------------

MagicDraw deberá estar instalado y funcionando correctamente en la computadora personal de cada alumno antes del comienzo del proyecto.

.. warning:: Actualmente dispobemos de licencia para la versión Personal Edition 18.0, por lo que los alumnos deberán descargarse dicha versión.

.. Recursos
.. ---------

..  * `Cómo descargar la versión correcta de MagicDraw <../misc/notAvailable.html>`_

Advanced Rest Client
=====================

.. note:: La utilización de esta herramienta es opcional, aunque la utilización de una herramienta de este tipo puede ayudar a reducir la carga de trabajo asociada al desarrollo del proyecto.

`Advanced Rest Client <https://install.advancedrestclient.com/#/install>`_ es una sencilla app para Chrome que permite generar de forma cómoda e intuitiva peticiones HTTP y observar sus resultados. Puede resultar de utilidad para ver qué está retornando la fuente externa de datos con la que se trabajará durante el proyecto.

Acción Requerida
-----------------

Los alumnos que opten por la utilización de esta herramienta deberán instalarla antes del comienzo del proyecto y verificar su correcto funcionamiento.
