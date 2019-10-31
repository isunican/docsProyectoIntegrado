====================
 Actividades Scrum
====================

Esta sección describe las actividades que se deberán realizar para el desarrollo del proyecto integrado de acuerdo con la metodología de desarrollo Scrum. Estas actividades se descomponen en dos conjuntos diferenciados, que son *actividades de preparación de los sprints* y *actividades para el desarrollo de un sprint*. A continuación se describen ambos conjuntos de actividades.

Actividades de preparación de los sprints
=============================================

Constitución de los equipos
--------------------------------

**Descripción de la Actividad**

En primer lugar, se constituirán los equipos de desarrollo. La formación de cada equipo la decidirá el equipo docente asociado al proyecto integrado y tan pronto como se tenga confeccionada se notificará a través de la plataforma moodle. La única resposabilidad del alumno a este respecto es estar pendiente de las notificaciones de moodle para ponerse en contacto con sus compañeros una vez que haya recibido dicha notificación.

.. todo: Poner enlace a lo que es un pacto de equipo.

Una vez constituido, cada equipo de desarrollo deberá elegir un nombre, consensuar un `Pacto de Equipo <../misc/pactoEquipo.html>`_ y firmarlo. Tras la firma de dicho pacto, todos los miembros del equipo se obligan a su cumplimiento. Su incumplimiento significará la expulsión automática del grupo; y, como consecuencia, el suspenso del proyecto integrado [#f1]_.

.. [#f1] En caso de llegar a esta desgradable situación, en cada caso particular se pactarán unas condiciones específicas de recuperación del proyecto integrado de manera que se puedan tanto alcanzar los objetivos de aprendizaje de la asignatura como reutilizar parte del trabajo que se hubiese realizado.

A continuación, cada equipo deberá preparar la infraestructura necesaria para el desarrollo del proyecto. Dicha infraestructura comprende tanto una serie de herramientas que deberán estar instaladas en los equipos de los alumnos, como una serie de herramientas en la nube en las cuales los alumnos deberán abrir la correspondiente cuenta. En la sección de `Herramientas <../tools/index.html>`_ del presente documento se describen todas las herramientas necesarias para el desarrollo del proyecto, qué debe hacer el alumno para instalarlas y cómo debe configurarlas.

Esta infraestructura deberá estar completamente operativa antes del inicio del proyecto.
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

:Fecha y Hora: Primer Lunes del Sprint, de 9.30 a 10.30.

**Descripción de la Actividad**

Al inicio de cada sprint, cada *Scrum Team* realizará, con la colaboración de su respectivo *Product Owner*, la selección de los elementos del *Product Backlog* a desarrollar en dicho sprint. Esta selección deberá ser aquella que, ajustándose a la *velocidad de equipo*, aporte mayor valor al nuevo producto generado. .

Una vez realizada la selección de elementos que conformarán el *Sprint Backlog*, el *Scrum Team* deberá conversar con el *Product Owner* para saber con todo detalle cómo han de desarrollar cada uno de los elementos seleccionados. Para que el desarrollo de los sprints sea sostenible, la metodología *Scrum* no permite ni modificar el contenido del *Sprint Backlog* durante el desarrollo de un sprint, ni que sus elementos se renegocien. Por tanto, en esta actividad deben quedar perfectamente definidos todos los elementos que sean necesarios para un correcto desarrollo de los elementos seleccionados.

.. warning:: Se recomienda prestar especial atención en esta actividad a la definición de los test de aceptación de cada una de las historias de usuario seleccionadas. Estos tests deben incluir escenarios tanto de éxito como alternativos, excepcionales y de no éxito.

**Elementos a Entregar**

Como resultado de esta actividad cada equipo deberá producir un *Sprint Backlog* para el desarrollo del correspondiente sprint.
Dicho *Sprint Backlog* tendrá que estar en la herramienta *ScrumDesk* y listo para su evaluación a las 14:00 horas del día siguiente al que se realice la actividad. Las historias de usuario incluidas en ese *Sprint Backlog* deben estar completamente especificadas, incluyendo obligatoriamente todos los tests de aceptación que sean necesarios; y, opcionalmente, toda la información recogida durante la negociación con el *Product Owner*  y qeu se considere relevante, como, por ejemplo, los *mock-ups* creados.

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

Si un *Scrum Team* no realizara esta actividad, no tendría material para poder continuar desarrollando el *sprint*. Por tanto, la no realización de esta actividad implica que el equipo completo obtendría una calificación de 0 puntos en todos los elementos evaluables asociados a ese sprint.

Sprint Planning Meeting II
---------------------------

:Fecha y Hora: Primer Lunes del sprint, de 10:30 a 11:30

**Descripción de la Actividad**

Una vez definido el *Sprint Backlog* cada equipo descompondrá sus elementos en tareas. Por cada elemento, se deberán incluir todas las tareas necesarias para que se pueda alcanzar la `definición de completado <definicionCompletado.html>`_. A continuación, se estimará el esfuerzo de cada tarea en horas utilizando la técnica de *Planning Poker*. Finalmente, se distribuirán las tareas entre los diferentes miembros del *Scrum Team* de manera que:

  * se satisfagan las restricciones impuestas por el proyecto integrado;
  * la carga de trabajo de cada uno de los miembros del equipo resulte lo más equilibrada posible;
  * se facilite el trabajo concurrente durante el desarrollo del sprint.

.. warning:: La estimación de las tareas en horas debe realizarse utilizando una escala discreta de espacio creciente, tal como la escala de fibonacci modificada [0, 0.5, 1, 2, 3, 5, 8, 13, 20, 50, 100].

**Elementos a Entregar**

Como resultado de esta actividad cada equipo deberá producir un conjunto de tareas a realizar, las cuales constituirán la planificación del sprint. Dicho descomposición en tareas tendrá que estar incluida en la herramienta *ScrumDesk* y lista para su evaluación a las 14:00 horas del día siguiente al de la realización de la actividad.

**Procedimiento de Evaluación**

Dentro de esta actividad se evaluarán y calificarán los siguientes ítems:

  * Capacidad de Liderazgo.
  * Ortografía, Gramática y Maquetación.
  * Planificación de Tareas.
  * Ejecución del Planning Poker.

Si un *Scrum Team* no realizase esta actividad, no tendría material para poder continuar desarrollando el *sprint*. Por tanto, la no realización de esta actividad implicaría que el equipo completo obtendría una calificación de 0 puntos en todos los elementos evaluables que reste realizar dentro de ese sprint.

Gestión y Seguimiento del Sprint
---------------------------------------------

:Fecha y Hora: Diario.

**Descripción de la Actividad**

Tras concluir la planificación del sprint, cada miembro del equipo podrá comenzar a trabajar en las tareas que tenga asignadas. Durante el desarrollo de estas tareas, el alumno deberá prestar atención a tres actividades concretas de interés para la asignatura de *Métodos de Desarrollo*:

  #. Gestión del tablero *Kanban*.
  #. Monitorización de la evolución del sprint.
  #. Gestión de la Configuración.

Para la *gestión del tablero Kanban*, cada miembro del equipo deberá actualizar regularmente el estado de sus tareas. Para ello deberá tanto mover de manera adecuada las tarjetas asociadas a sus tareas y actualizar correctamente y de manera regular sus valores de *spent* y *remaining*.

Para la *monitorización de la evolución del sprint*, el equipo deberá revisar, al menos una vez al día, el *sprint burndown chart* para, en función de su estado, decidir si es necesario adoptar algún tipo de acción correctora o no.

Para la *gestión de la configuración*, cada miembro del equipo deberá observar escrupulosamente las `reglas de gestión de la configuración <https://proyecto-integrado-ingenieria-del-sw.readthedocs.io/es/latest/cfgMng/politicaCfg.html#reglas-de-gestion-de-la-configuracion>`_ especificadas para el desarrollo del proyecto integrado.

Además, merece la pena destacar que, idealmente, cada miembro del equipo debería trabajar individualmente, en silencio e interaccionando lo mínimo posible con sus compañeros. No obstante, siempre que se trabaja en equipo es necesario llevar a cabo ciertas acciones de coordinación. Estas acciones de coordinación deberán realizarse principalmente dentro de los *Daily Scrum Meeting*. Para la coordinación remota, se aconseja utilizar una herramienta de comunicación asíncrona y/o remota tipo *Slack* o similar.

**Elementos a Entregar**

Como consecuencia de la realización de esta actividad, la herramienta utilizada para la gestión del proyecto deberá reflejar fielmente el estado de ejecución actual del sprint. La veracidad de la información contenida dentro de la herramienta de gestión de proyectos podrá ser contrastada por el equipo docente en cualquier momento durante el desarrollo de un sprint. Además, el repositorio Git utilizado para el desarrollo del proyecto debe ser conforme a las normas de la gestión de la configuración.

**Procedimiento de Evaluación**

Dentro de esta actividad se evaluarán y calificarán los siguientes ítems:

  * Gestión de la Configuración.
  * Gestión de tareas y tablero Kanban.
  * Interpretación Sprint Burndown Chart.

La evaluación de los dos primeros ítems se realizará de manera individual a lo largo del desarrollo del proyecto, mediante pequeñas pruebas orales en el aula.
El tercer ítem se evaluará de manera global para cada equipo, atendiendo a la evolución del repositorio Git conforme a las normas de gestión de la configuración durante el desarrollo del sprint.

Daily Scrum Meeting
---------------------

:Fecha y Hora: Diario (salvo inicio y fin de cada sprint), 9:30 – 9:45

Al comienzo de cada día de un sprint, a excepción de los días de comienzo y fin de dicho sprint, cada equipo deberá realizar un *Daily Scrum Meeting*. Se recomienda que esta reunión se haga a primera hora de cada jornada, aunque esto puede ajustarse en función de las necesidades de cada equipo, ya que es importante la presencia de todos sus miembros durante su celebración.

El objetivo final de esta actividad es que cada miembro del grupo conozca qué hizo el equipo el día anterior, qué va a hacer hoy, y, qué dificultades está atravesando actualmente. En caso de encontrar dificultades, el equipo deberá idear un plan para solventar dichas dificultades.

Para realizar correctamente un *Daily Scrum Meeting*, bajo la dirección del moderador, primero interviene cada miembro del equipo. Cada mimebro del equipo, durante su intervención, deberá describir brevemente primero qué hizo ayer, luego qué piensa hacer hoy, y, por último, qué obstáculos y riesgos ha identificado hasta el momento. Tras estas intervenciones iniciales, se deberá esbozar, de manera breve y efectiva, un plan de acción para eliminar o inimizar los obstáculos y riesgos detectados.

Se recomienda, de acuerdo con las directrices de Scrum, que los *Daily Scrum Meeting* se celebren fuera del aula y con todos los miembros del equipo de pie.

**Elementos a Entregar**

Como resultado de esta actividad no se deberá entregar nada. Serán los miembros del equipo docente lo que acudan periódicamente a la ejecución de esta actividad para evaluarla.

**Procedimiento de Evaluación**

Dentro de esta actividad se evaluarán y calificarán los siguientes ítems:

  * Ejecución de los Daily Scrum Meeting

Product Backlog Refinement
----------------------------

:Fecha y Hora: Segundo Lunes del Sprint, 9:30 - 10:30

**Descripción de la Actividad**

Durante el desarrollo de cada sprint, y de cara a preparar el *Product Backlog* para el próximo *Sprint Planning Meeting I*, cada *Scrum Team*, con la colaboración de su correspondiente *Product Owner*, revisará el estado actual del *Product Backlog*. Durante esta actividad, en base a la experiencia adquirida, se podrán añadir, modificar y eliminar elementos del *Product Backlog*. Además, se deberá revisar y modificar si fuese necesario los puntos de esfuerzo y valores de negocio asignados a cada elemento del *Product Backlog*. Tras la realización de esta reunión, el *Product Backlog* debería quedar listo para poder ejecutar el siguiente *Sprint Planning Meeting*, salvo por la inclusión de los posibles *tickets de mantenimiento* que pudiesen surgir tras la *Product Review* del presente sprint.

.. warning:: Merece la pena destacar que esta reunión no está destinada a resolver dudas sobre las historias de usuario que se estén desarrollando en ese momento.

**Elementos a Entregar**

Como resultado de esta actividad cada equipo deberá producir un *Product Backlog* revisado que pueda ser utilizado para el siguiente *Sprint Planning Meeting I*. Dicho *Product Backlog* tendrá que estar alamacenado en la herramienta *ScrumDesk* y listo para su evaluación a las 00:00 horas del mismo día en el que se realice esta actividad.

**Procedimiento de Evaluación**

Dentro de esta actividad se evaluarán y calificarán los siguientes ítems:

  * Relación con el Product Owner.
  * Capacidad de Liderazgo.
  * Capacidad de Comunicación.
  * Ortografía, Gramática y Maquetación.
  * Conformidad del Product Backlog.
  * Especificación de las Historias de Usuario.
  * Planning Poker (opcional)

Sprint Review
--------------

:Fecha y Hora: Segundo Viernes del Sprint, 9:30-10:30

**Descripción de la Actividad**

Durante la *Product Review* cada *Scrum Team* mostrará el trabajo realizado en ese sprint a su correspondiente *Product Owner*. El objetivo debe ser conocer si el producto creado se adecúa realmente a lo esperado por el *Product Owner*; o, por el contrario, es necesario realizar algunas modificaciones.

Para ello, el *Scrum Team* deberá mostrar cada una de las funcionalidades desarrolladas al *Product Owner* y verificar delante suya su correcto funcionamiento. Además, el *Scrum Team* deberá permitir al *Product Owner* instalar en su propio terminal el producto desarrollado, de manera que pueda experimentar con él si así lo desease.

Durante la revisión del producto, el *Product Owner* podrá solicitar todas las explicaciones, tanto técnicas como no técnicas, que considere necesarias sobre el desarrollo del producto. Una vez revisado el producto y aclaradas las dudas que puedan surgir, el *Product Owner* podrá sugerir cambios, que serán debatidos con el *Scrum Team*. Si finalmente el *Product Owner* estima necesario incorporar ciertos cambios,  éstos deberán ser incorporados al *Product Backlog* como *tickets de mantemiento*

.. Finalmente, hay que tener en cuenta que el *Product Owner*, al final de la *Product Review*, podría decidir poner el producto en funcionamiento real. Por tanto, cada equipo de desarrollo debe estar preparado para liberar el producto tan pronto como el *Product Owner* lo requiera.

**Elementos a Entregar**

Como resultado de esta actividad deberá existir una nueva versión operativa del producto software desarollado. Esta versión operativa incluirá todos los artefactos requeridos por la  `definición de completado <https://proyecto-integrado-ingenieria-del-sw.readthedocs.io/es/latest/scrum/definicionCompletado.html>`_, y estará alojada en el repositorio *Git* de cada equipo, el cual deberá ser conforme a las `normas de gestión de la configuración <https://proyecto-integrado-ingenieria-del-sw.readthedocs.io/es/latest/cfgMng/politicaCfg.html#politica-de-gestion-de-la-configuracion>`_ para el desarrollo del proyecto integrado.

Además, se deberán incluir en el *Product Backlog* todos los tickets de mantenimiento que hayan podido surgir durante la *Product Review*. Los tickets de mantenimiento actualizados deberán estar listos para su calificación el mismo día en el cual se celebre la *Product Review* a las 16:00.

**Procedimiento de Evaluación**

Dentro de esta actividad se evaluarán y calificarán los siguientes ítems:

  * Relación con el Product Owner.
  * Capacidad de Liderazgo.
  * Capacidad de Comunicación.
  * Ortografía, Gramática y Maquetación.
  * Conformidad del Product Backlog.
  * Cumplimiento de Definición de Completado.
  * Satisfacción del Product Owner.
  * Manual de Usuario.
  * Planning Poker (opcional).

.. warning:: La no realización de esta actividad supondrá una calificación de 0 en el correspondiente sprint.

Sprint Retrospective
---------------------

:Fecha y Hora: Segundo Viernes del Sprint, 10:30-11:30

**Descripción de la Actividad**

Tras las *Product Review*, cada equipo reflexionará sobre sus métodos de trabajo con el objetivo de identificar qué ha hecho bien y qué ha hecho mal durante el desarrollo del sprint. Tras esta reflexión, se deberán adoptar medidas que permitan tanto potenciar los aspectos positivos como corregir los errores. La reflexión deberá estar organizado en torno a alguna dinámica de grupo tipo *brainstorming*. A este respecto se recomienda revisar las dinámicas de grupo existentes dentro del libro Gamestorming_.

.. _Gamestorming: https://gamestorming.com/

Tras la realización de esta actividad se puede dar el sprint por concluido. Se recomienda realizar alguna actividad lúdica que resulte del agrado del equipo, tal como tomarse una simple bebida con un pincho de tortilla, como recompensa al trabajo realizado. Esta actividad debe hacerse fuera del horario lectivo.

**Elementos a Entregar**

Como resultado de esta actividad cada *Scrum Team* entregará un *plan de mejora continua* con las medidas a adoptar durante el desarrollo del próximo sprint. Este plan, tal como se comentó anteriormente, debe tener acciones tanto para potenciar los aspectos positivos como para mitigar o erradicar los negativos.
Este *plan de mejora continua* se entregará a través de una actividad de moodle habilitada a tal efecto. Las entregas de este plan se realizarán antes de las 00:00 del Lunes siguiente a la celebración de la *Sprint Retrospective*.

**Procedimiento de Evaluación**

Dentro de esta actividad se evaluarán y calificarán los siguientes ítems:

  * Capacidad de Liderazgo.
  * Ortografía, Gramática y Maquetación.
  * Completitud del Análisis de la Retrospectiva.
  * Plan de Mejora Continua.
