====================
 Actividades Scrum
====================

Esta página describe las actividades que se deberán realizar para el desarrollo del proyecto integrado de acuerdo con la metodología de desarrollo Scrum. Estas actividades se descomponen en dos conjuntos diferenciados, que son *actividades de preparación de los sprints* y *actividades para el desarrollo de un sprint*. El desarrollo de los sprints incluyen de manera natural actividades relacionadas tanto con la planificación, el diseño y la ejecución de pruebas sw, como con la gestión de la calidad. A continuación se describen ambos conjuntos de actividades.

Actividades de preparación de los sprints
=============================================

Constitución de los equipos
--------------------------------

**Descripción de la Actividad**

En primer lugar, se constituirán los equipos de desarrollo. La formación de cada equipo la decidirá el equipo docente asoaciado al proyecto integrado y tan pronto como se tenga confeccionada se notificará a través de la plataforma moodle. La única resposabilidad del alumno a este respecto es estar pendiente de las notificaciones de moodle para ponerse en contacto con sus compañeros una vez que haya recibido dicha notificación.

.. todo: Poner enlace a lo que es un pacto de equipo.

Una vez constituido, cada equipo de desarrollo deberá elegir un nombre, consensuar un `Pacto de Equipo <../misc/pactoEquipo.html>`_ y firmarlo. Tras la firma de dicho pacto, todos los miembros del equipo se obligan a su cumplimiento. Su incumplimiento significará la expulsión automática del grupo; y, como consecuencia, el suspenso del proyecto integrado [#f1]_.

.. [#f1] En caso de llegar a esta desgradable situación, en cada caso particular se pactarán unas condiciones específicas de recuperación del proyecto integrado de manera que se puedan tanto alcanzar los objetivos de aprendizaje de la asignatura como reutilizar parte del trabajo que se hubiese realizado.

A continuación, cada equipo deberá preparar la infraestructura necesaria para el desarrollo del proyecto. Dicha infraestructura comprende tanto una serie de herramientas que deberán estar instaladas en los equipos de los alumnos, como una serie de herramientas en la nube en las cuales los alumnos deberán abrir la correspondiente cuenta. En la sección de `Herramientas <../tools/index.html>`_ del presente documento se describen todas las herramientas necesarias para el desarrollo del proyecto, qué debe hacer el alumno para instalarlas y cómo debe configurarlas.

Esta infraestructura deberá estar complementamente operativa antes del inicio del proyecto.
Además, la herramienta `ScrumDesk <../tools/index.html#scrumdesk>`_ deberá estar funcionando antes de la actividad `Initial Product Backlog Refinement <actividadesScrum.html#initial-product-backlog-refinement>`_

**Elementos a Entregar**

Como resultado de esta actividad, cada equipo deberá entregar su correspondiente *Pacto de Equipo* a través de la actividad porporcionada en moodle para ello. Además el equipo docente verificará que ciertos elementos de la infraestructura de desarrollo están adecuadamente creados.

**Procedimiento de Evaluación**

Esta actividad se evaluará como realizada o no realizada. La evaluación como no realizada conlleva una penalización de 100 puntos en la calificación final del proyecto.

Initial Product Backlog Refinement
---------------------------------------

**Descripción de la Actividad**

Antes del comienzo de los sprints, cada equipo, junto con su *Product Owner*, deberá crear un *Product Backlog* inicial. Para ello, cada *Scrum Team*, junto con su correspondiente *Product Owner*, deberá refinar la visión del sistema, que será proporcionada por el *Product Owner*, hasta
descomponerla en un conjunto de historias de usuario sencillas. Se consideran historias de usuario sencillas aquellas que no sean `épicas <https://www.agilealliance.org/glossary/epic/>`_, es decir, que estén al `nivel del mar <https://wiki.nci.nih.gov/display/seminfra/Use+Case+Leveling+Definitions>`_. Una vez descompuesta la visión del sistema en historias de usuario, éstas deberán ser valoradas por el *Product Owner*, con la ayuda del *Scrum Team*, para poder obtener así su *valor de negocio*. Por último, el equipo deberá estimar, en puntos, el `esfuerzo asociado al desarrollo de cada historia de usuario <calculoCargaTrabajo.html#como-estimar-una-historia-de-usuario-en-puntos>`_.

**Elementos a Entregar**

Como resultado de esta actividad se deberá generar un *Product Backlog* inicial sobre el cual se pueda empezar a realizar los sprints. Dicho *Product Backlog* deberá estar cargado en el proyecto ScrumDesk de cada equipo y listo para su calificación en la fecha que se indique en la correspondiente actividad de Moodle. Además, se recomienda elaborar como salida de esta actividad un diagrama de objetivos, aunque este paso es opcional.

**Procedimiento de Evaluación**

La no realización de esta actividad por parte de un equipo supone el suspenso automático del proyecto. Dentro de esta actividad se evaluarán y calificarán los siguientes ítems:

  * Relación con el Product Owner.
  * Capacidad de Liderazgo.
  * Capacidad de Comunicación.
  * Ortografía, Gramática y Maquetación.
  * Conformidad del Product Backlog.
  * Especificación de las Historias de Usuario.

Además, aquellos equipos que elaboren un diagrama de objetivos podrán obtener una bonificación extra en la calificación de la asignatura de hasta 15 puntos, en función de la calidad del diagrama de objetivos entregado.

Actividades dentro de un sprint Scrum
======================================

Sprint Planning Meeting I
--------------------------

:Fecha y Hora: Primer Lunes de cada sprint, de 8:30 a 9:30.

** Descripción de la Actividad**

Al inicio de cada sprint, cada *Scrum Team* realizará, con la colaboración de su respectivo *Product Owner*, la selección de los elementos del *Product Backlog* que se incluirán dentro del desarrollo de ese sprint. Esta selección debe realizarse de manera que se maximize el valor del trabajado generado dentro de las restricciones impuestas por la *velocidad de equipo*.

Una vez realizada la selección de elementos que conformará el *Sprint Backlog*, el *Scrum Team* deberá de extraer del *Product Owner* toda la información que necesite para su correcto desarrollo. Hay que tener cuenta que para que el desarollo de los sprints sea sostenible, la metodología *Scrum* no permite modificar el contenido del *Sprint Backlog* durante el desarrollo de un sprint, ni que sus elementos se renegocien. Por tanto, en esta actividad deben quedar perfectamente definidos todos los aspectos necesarios para el desarrollo de los elementos seleccionados.

.. warning:: Se recomienda prestar especial atención en esta actividad a la definición de los test de aceptación para cada historia de usuario seleccionada. Estos tests deben incluir escenarios tanto de éxito como alternativos, excepcionales y de no éxito.

**Elementos a Entregar**

Como resultado de esta actividad cada equipo deberá producir un *Sprint Backlog* para el desarrollo del correspondiente sprint.
Dicho *Sprint Backlog* tendrá que estar en la herramienta *ScrumDesk* y listo para su evaluación a las 14:00 horas del mismo día en el que se relice la actividad. Las historias de usuario incluidas en ese *Sprint Backlog* deben estar ya complementamente especificadas, incluyendo obligatoriamente todos los tests de aceptación que sean necesarios; y, opcionalmente, toda la informacion recogida durante la negociacion con el *Product Owner*, como *mock-ups*, que se considere relevante para su desarrollo.

**Procedimiento de Evaluación**

Dentro de esta actividad se evaluarán y calificarán los siguientes ítems:

  * Relación con el Product Owner.
  * Capacidad de Liderazgo.
  * Capacidad de Comunicación.
  * Ortografía, Gramática y Maquetación.
  * Conformidad del Product Backlog.
  * Especificación de las Historias de Usuario.
  * Creación del Sprint Backlog
  * Negociación de Historias de Usuario

Si un *Scrum Team* no realizase esta actividad, no tendría material para poder continuar desarrollando el *sprint*. Por tanto,   la no realización de esta actividad implicaría que el equipo completo obtendría una calificación de 0 puntos en todos los elementos evaluables asociados a actividades de ese sprint.

Sprint Planning Meeting II
---------------------------

:Fecha y Hora: Primer Lunes de cada sprint, de 9:30 a 10:30

**Descripción de la Actividad**

Una vez definido el *Sprint Backlog* cada equipo descompondrá sus elementos en tareas. Por cada elemento, se deberán incluir todas las tareas necesarias para que se pueda alcanzar la `definición de completado <definicionCompletado.html>`_. A continuación, se estimará el esfuerzo de cada tarea en horas utilizando la técnica de *Planning Poker*. A continuación, se distribuirán las tareas entre los diferentes miembros del *Scrum Team* de manera que:

  * se satisfagan las restricciones impuestas por el proyecto integrado;
  * la carga de trabajo de cada uno de los miembros del equipo resulte lo más equilibrada posible;
  * se facilite el trabajo concurrente durante el desarrollo del sprint.

.. warning:: La estimación de las tareas en horas debe realizarse utilizando una escala discreta de espacio creciente, tal como la escala de fibonacci modificada [0, 0.5, 1, 2, 3, 5, 8, 13, 20, 50, 100].

**Elementos a Entregar**

Como resultado de esta actividad cada equipo deberá producir un conjunto de tareas a realizar, las cuales constituirán la planificación del sprint. Dicho descomposición en tareas tendrá que estar incluida en la herramienta *ScrumDesk* y lista para su evaluación a las 14:00 horas del mismo día en el que se relice la actividad.

**Procedimiento de Evaluación**

Dentro de esta actividad se evaluarán y calificarán los siguientes ítems:

  * Capacidad de Liderazgo.
  * Ortografía, Gramática y Maquetación.
  * Planificación de Tareas.
  * Ejecución del Planning Poker.

Si un *Scrum Team* no realizase esta actividad, no tendría material para poder continuar desarrollando el *sprint*. Por tanto,   la no realización de esta actividad implicaría que el equipo completo obtendría una calificación de 0 puntos en todos los elementos evaluables asociados a actividades de ese sprint.

Daily Scrum Meeting
---------------------

:Fecha y Hora: Diario (salvo inicio y fin de cada sprint), 8:30 – 8:45

Al comienzo de cada día de un sprint, a excepción de los días de comienzo y fin del sprint, cada equipo deberá realizar un *Daily Scrum Meeting*. Se recomienda que esta reunión se haga a primera hora de cada jornada, aunque esto puede ajustarse en función de las necesidades de cada equipo, ya que es importante la presencia de todos sus miembros durante su celebración.

El objetivo final de esta actividad es que cada miembro del grupo conozca qué hizo el equipo el día anterior; qué va a hacer hoy; y qué dificultades está atravesando actualmente. Además, el equipo deberá idear un plan para solventar dichas dificultades. Para ello, los miembros del grupo intervendrán por orden y expondrán, sin interrupción por parte de otros mimebros, qué hicieron ayer, qué harán hoy y qué problemas tienen para desarrollar su trabajo. Al final de todas las intervenciones se debatirán las acciones de coordinación entre miembros del grupo que se consideren necesarias.

La celebracíón del *Daily Scrum Meeting* se realizará fuera del aula y de pie, de acuerdo con las recomendaciones de la metodología *Scrum*.

**Elementos a Entregar**

Como resultado de esta actividad no se debe entregar nada. Serán los miembros del equipo docente lo que acudan periódicamente a la ejecución de esta actividad para evaluarla.

**Procedimiento de Evaluación**

Dentro de esta actividad se evaluarán y calificarán los siguientes ítems:

  * Capacidad de Liderazgo.
  * Ejecución de los Daily Scrum Meeting

.. :Fecha y Hora: Primer Lunes de cada sprint, de 9:30 a 10:30

.. **Descripción de la Actividad**
.. **Elementos a Entregar**
.. **Procedimiento de Evaluación**
