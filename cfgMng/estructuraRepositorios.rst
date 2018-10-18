================================
 Estructura de los Repositorios
================================

Para favorecer la gestión de los diferentes artefactos creados durante la ejecución del proyecto, los repositorios a cada proyecto deberán seguir la estructura que se muestra en la Figura 1. De acuerdo con dicha figura, el repositorio de cada equipo contendrá tres carpetas o directorios principales: ``Docs``, ``Releases`` y ``AndroidProject``. Cada uno de estos directorios almacenará el siguiente contenido.

``Docs``
  Contendrá todos la documentación generada durante el desarrollo del proyecto.

``Releases``
  Almacenará los ficheros binarios que es necesario instalar para ejecutar el producto generado al final de cada sprint.

``AndroidProject``
  Contendrá todo el código fuente asociado al proyecto, incluyendo el código correspondiente a los casos de prueba.

Cada carpeta se estructura a su vez tal como se indica en las siguientes secciones.

.. figure:: img/estructuraRepositorios.svg
   :align: center
   :alt: Estructura de los repositorios

   Figura 1. Estructura de los Repositorios

Carpeta ``Docs``
=================

La carpeta ``Docs`` es la que aloja toda la documentación generada con el desarrolo proyecto. Esta carpeta contendrá todaslas los subcarpetas que se detallan a continuación.

.. note:: En cada una de estas carpetas podrán existir, además de los archivos indicados, todos los ficheros fuentes, como documentos de *Word* o *LibreOffice*, que sean necesarios para generar los documentos que se solicitan.

Carpeta ``Mockups``
--------------------

.. note:: Esta carpeta es opcional, pudiendo existir por tanto repositorios que no la contengan. No obstante,se recomienda encarecidamente su utilización.

Esta carpeta contendrá una carpeta por cada historia de usuario desarrollada. Cada carpeta se nombrará de acuerdo con el patrón ``US<id>-<Name>``, donde ``id`` es el identificador numérico asignado por *ScrumDesk* a dicha historia de usuario  y ``name`` es un nombre que permita identificar dicha historia de usuario de manera más cómoda.

Dentro de cada una de estas subcarpetas se alojarán todos los *mockups* asociados a una la historia de usuario que corresponda a dicha subcarpeta. Se recomienda almacenar los *mockups* como imágenes ``.png``, dándoles un nombre significativo a cada una de ellas.

Carpeta ``Models``
--------------------

Esta carpeta contendrá todos los modelos generados durante el desarrollo de la aplicación.

Como mínimo, esta carpeta deberá contener un:

  #. Un modelo de dominio, representado como un diagrama de clases UML, con las entitidades que constituyen el *modelo* de la aplicación.
  #. Un modelo que describa la arquitectura de la aplicación, resaltando las conexiones entre las clases de la *vista*, el *modelo*, y el *presentador*; mediante un diagrama de clases UML.

Ambos modelos se almacenarán como imágenes en formato ``.png``. El nombre del fichero alojando el modelo de dominio será ``DomainModel.png`` y el nombre del fichero correspondiente al modelo arquitectónico será ``AppArchitecture.png``.

En caso de que el equipo haya generado un modelo de objetivos, deberá alojarlo en esta carpeta como un conjunto de imágenes en formato ``.png``. Cada imagen tendrá como nombre ``GoalModelXX.png``, donde ``XX`` se sustituirá por un identificador numérico autoincrementado comenzando en 0.

Carpeta ``Tutorials``
======================

Esta carpeta poseerá todo el material relacionado con el manual de usuario de la aplicación. Para elaborar el manual de usuario, se puede seguir cualquiera de las tres estrategias que se describen a continuación:

  #. Generar un manual de usuario clásico en formato ``pdf``.
  #. Elaborar una página web de ayuda donde la ayuda para cada historia de usuario se describa en una página HTML diferente.
  #. Crear una serie de videotutoriales, uno por cada historia de usuario, que ilustren el funcionamiento de la aplicación.

Manual de Usuario Clásico
--------------------------

En este caso la carpeta ``Tutorials`` contendrá un único documento denominado ``userManual.pdf``. Este documento  contendrá el manual de usuario de la aplicación, organizado de la manera que cada equipo considere más conveniente.

Manual de Usuario HTML
-----------------------

En este caso existirá una página de inicio para el manual, denominada ``index.html``, que estará situada en la carpeta tutorials. Esta página contendrá simplemente una lista de enlaces que apuntarán a las páginas de ayuda para cada historia de usuario desarrollada.

La página correspondiente a cada historia de usuario se alojará dentro de una subcarpeta de tutorials cuyo nombre seguirá el patrón ``US<id>-<Name>``, donde ``id`` es el identificador numérico asignado por *ScrumDesk* a dicha historia de usuario  y ``name`` es un nombre que permita identificar dicha historia de usuario de manera más cómoda.

Por último, destacar que dentro de la carpeta ``Tutorials`` y de las subcarpetas correspondientes a cada historia de usuario, podrán existir además archivos de otros tipos, tales como hojas de estilo o imágenes, necesarios para la elaboración de cada página web.

Videotutoriales
----------------

En este caso se elaborará un pequeño videotutorial por cada historia de usuario desarrollada. El vídeotutorial correspondiente a cada historia de usuario se alojará dentro de una subcarpeta de ``Tutorials`` cuyo nombre seguirá el patrón ``US<id>-<Name>``, donde ``id`` es el identificador numérico asignado por *ScrumDesk* a dicha historia de usuario  y ``name`` es un nombre que permita identificar dicha historia de usuario de manera más cómoda.

Como formato para los vídeos se puede escoger aquél que cada *Scrum Team* considere como más adecuado. En cualquier caso, se recomienda utilizar formatos sencillos que no impliquen la instalación de exóticos juegos de *codecs*.


Carpeta ``Test Plans``
========================

Esta carpeta contendrá toda la documentación relacionada con las pruebas sw diseñadas, implementadas y ejecutadas durante el desarrollo de cada historia de usuario. Por cada historia de usuario desarrollada se generarán dos documentos relacionados con las pruebas sw: el *plan de pruebas* y el *informe de pruebas*. Ambos documentos deberán estar en formato ``pdf``. El *plan de pruebas* tendrá como nombre ``US<id>-<Name>-TestPlan.pdf``, mientras que el del *informe de pruebas será ``US<id>-<Name>-TestReport.pdf``, donde, en ambos casos, donde ``id`` es el identificador numérico asignado por *ScrumDesk* a dicha historia de usuario  y ``name`` es un nombre que permita identificar dicha historia de usuario de manera más cómoda.

Carpeta ``Quality Reports``
============================

Esta carpeta alojará los informes de calidad generados para cada historia de usuario desarrollada. Los planes de prueba deberán estar en formato ``pdf``, y nombrados conformes al patrón ``US<id>-<Name>-QAReport.pdf``, donde ``id`` es el identificador numérico asignado por *ScrumDesk* a dicha historia de usuario  y ``name`` es un nombre que permita identificar dicha historia de usuario de manera más cómoda.

Carpeta ``Releases``
=====================

Carpeta ``AndroidProject``
===========================
