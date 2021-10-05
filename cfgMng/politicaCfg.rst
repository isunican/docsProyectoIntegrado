==========================================
 Política de Gestión de la Configuración
==========================================

Estructura de Ramas
---------------------

.. _gitflow: https://nvie.com/posts/a-successful-git-branching-model/
.. _definición de completado: ../scrum/definicionCompletado.html#definicion-de-completado
.. _normas establecidas para nombrar fichero apk: estructuraRepositorios.html#carpeta-releases

La política de *Gestión de la Configuración* que se utilizará durante el desarrollo del proyecto integrado estará basada en el esquema de ramificación  GitFlow_. De acuerdo con dicho esquema, en el repositorio de cada equipo de trabajo deberán existir las ramas que se describen a continuación.

**Ramas Principales**

``master``
  Constituye la rama principal del proyecto. Esta rama debe contener únicamente versiones del producto software que sean resultados finales de la ejecución de un *sprint*. Cada elemento del *Product Backlog* incluido en estas versiones debe satisfacer la `definición de completado`_, de manera que cualquier versión incluida en esta rama pueda publicarse como una *release* en caso de que el *Product Owner* así lo desee. Esta rama estará activa durante toda la duración del proyecto.

``develop``
  Constituye una *rama de integración* en la cual los desarrolladores irán incorporando los cambios realizados en las distintas ramas destinadas al desarrollo de cada elemento del *Product Backlog*. El objetivo de esta rama es poder verificar periódicamente, conforme a un *esquema de integración continua*, que no existen problemas de integración entre los diferentes elementos del *Product Backlog* que se puedan estar desarrollando en un momento dado. Esta rama estará activa durante toda la duración del proyecto.

**Ramas Secundarias**

``feature branches``
  Una ``feature branch`` es una rama que se utiliza para desarrollar un elemento concreto del *Product Backlog*. Por tanto, por cada ítem del *Product Backlog* a desarrollar dentro de un sprint, se deberá crear una ``feature branch`` nueva. Todos los cambios que sean necesarios realizar para desarrollar dicho elemento del *Product Backlog* se almacenarán dentro de esta ``feature branch`` recién creada. Cada ``feature branch`` se deberá tratar de mantener tan independiente como sea posible de las otras ``feature branches`` que se encuentren activas durante el desarrollo de un sprint. El tiempo de vida de una ``feature branch`` está limitado al *sprint* donde se desarrolla su correspondiente ítem del *Product Backlog*.

``release branches``
  Una ``release branches`` se utiliza para realizar en ella todas las tareas que sean comunes a la preparación de una nueva versión operativa del producto, de manera previa a su integración en ``master``. Ejemplos de estos trabajos para el caso concreto del proyecto integrado se detallan en la sección `trabajos en la release branch`_. El tiempo de vida de una ``release branch`` está limitado a un *sprint*.

``hotfix branches`` [#f0]_
  Una ``hotfix branch`` se utiliza para solucionar *bugs* críticos detectados en versiones en producción del producto y que necesitan ser solucionados de manera urgente, sin poder esperar a ser planificados para su desarrollo dentro de un *sprint*. En este caso, se crea una rama directamente desde la versión de ``master`` que haya que corregir y se realiza en ella todo el trabajo que sea necesario para eliminar el *bug* detectado. Aunque el *bug* se corrija sin planificación previa, es convenientemente que satisfaga también la `definición de completado`_. El tiempo de vida de una ``hotfix branch`` está limitado al tiempo necesario para corregir el *bug*.

.. [#f0] Este tipo de ramas se incluyen en el esquema de ramificación del proyecto integrado por completitud, al formar parte de *GitFlow*, pero no se hará inicialmente uso de las mismas, salvo en ocasiones excepcionales.

Reglas de Gestión de la Configuración
---------------------------------------

.. note::
    Estas reglas asumen que las ramas ``master`` y ``develop`` existen en el repositorio centralizado del equipo.

#. Cada elemento del *Product Backlog* a desarrollar deberá desarrollarse en una ``feature branch`` independiente. Por tanto, al comienzo de cada sprint, se deberá crear una ``feature branch`` por cada elemento seleccionado para su desarrollo en ese *sprint*. Además, cada ``feature branch`` deberá tener como nombre ``feature/featureID-featureName``, donde ``featureID`` es el identificador numérico adjudicado por *ScrumDesk* al elemento del *Product Backlog* que corresponda; y, ``featureName`` es un nombre corto que se le dará a la rama para que su identificación sea menos críptica.
#. Los trabajos correspondientes a cada elemento del *Product Backlog* se realizarán en su correspondiente ``feature branch``. Una ``feature branch`` podrá ser subramificada tanto como se desee a criterio de cada *Scrum Team*.
#. De acuerdo con los *esquemas de integración continua*, cada ``feature branch`` deberá ser integrada en ``develop`` periódicamente. Por ello, se establece como norma, que ninguna ``feature branch`` que esté recibiendo trabajo puede estar más de dos días sin que haya sido integrada en ``develop``. Este proceso  se realizará siguiendo el procedimiento para la `integración de una feature branch en develop`_.
#. Cuando el desarrollo de un elemento del *Product Backlog* esté completo, se creará una *Pull Request* para solicitar formalmente la integración de su correspondiente *feature branch* en ``develop``. Este proceso se ejecutará siguiendo el procedimiento para la `integración de una Pull Request en develop`_.
#. Cuando el trabajo contenido en ``develop`` esté listo para crear una nueva versión operativa del producto, se procederá a crear una ``release branch``. Dicha rama tendrá como nombre ``release/SR<id>``, donde ``id`` es el número del sprint para el cual se produce la *release*. En esta rama se realizarán todos los trabajos finales que sean necesarios para crear una nueva versión operativa del software. Estos trabajos se detallan en la sección `trabajos en la release branch`_.git tag c
#. Cuando el trabajo contenido en la rama ``release`` esté terminado, dicha rama se fusionará con las ramas ``master`` y ``develop``. En ambos casos la fusión debe hacerse siempre de forma recursiva [#f1]_, por lo que deberá aparecer un único *commit* nuevo en la rama destino como resultado de la fusión.
#. Tras integrar la ``release branch`` en ``master``, el *commit* generado en la rama *master* deberá etiquetarse como ``vXX.YY.ZZ``, donde ``XX.YY.ZZ`` es el correspondiente número de versión. Este número de versión deberá ser conforme al `esquema de versionado`_ del proyecto integrado.

Integración de una ``feature branch`` en ``develop``
-----------------------------------------------------

Las integraciones de una ``feature branch`` en ``develop`` se realizarán de acuerdo al siguiente procedimiento:

#. Antes de realizar una integración de una ``feature branch`` en ``develop``, se deberá verificar que el último commit de ``develop`` esté marcado como ``Success`` por el entorno de integración continua *GitHub Actions*. En caso de no estarlo, habrá que esperar a que lo esté.
#. A continuación, se verificará que la versión local de la rama ``develop`` esté complementamente actualizada.
#. Tras realizar las comprobaciones anteriores, se deberá integrar, de manera local, la ``feature branch`` que corresponda dentro de ``develop``. Esta fusión deberá ser siempre recursiva, es decir, generar un nuevo *commit de merge* [#f1]_.
#. Si la fusión generase conflictos, estos deberán resolverse de manera consensuada con el resto del equipo.
#. La nueva rama ``develop``, con la ``feature branch`` integrada, deberá subirse al repositorio remoto. Al detectarse un nuevo *commit* en ``develop``, se ejecutará automáticamente el entorno de integración continua *GitHub Actions*. Al final de su ejecución, *GitHub Actions* marcará el correspondiente *commit* como ``Success`` o ``Failure``.

   a. Si el resultado es ``Success``, todo el trabajo existente en ``develop`` está libre de problemas de integración y este proceso se da por terminado.
   b. Si el resultado es ``Failure``, existen problemas de integración que han de resolverse. En este caso, la rama ``develop`` queda bloqueada, no pudiendo recibir nuevas integraciones hasta que se solucionen dichos problemas de integración. Por tanto, se deberá trabajar en la solución de estos problemas con la mayor prontitud posible.

   Para resolver dichos problemas de integración, los responsables de la ``feature branch`` que haya generado el conflicto deberán realizar los cambios que sean necesarios en dicha ``feature branch``. Una vez realizados esos cambios, volverán a repetir este procedimiento desde el punto 3.

#. En caso de haberse detectado conflictos,  una vez resueltos los mismos, los diferentes miembros del equipo deberán actualizar los archivos conflictivos en sus correspondientes ``feature branches``, de manera que se eviten nuevos conflictos en el futuro [#f2]_.

.. [#f2] Para obtener un único fichero de una versión determinada se puede utilizar el comando ``git checkout version fichero`` o realizar un *cherry pick*.

Integración de una *Pull Request* en ``develop``
-------------------------------------------------

Las *Pull Request* se crean cuando el trabajo de una ``feature branch`` está completamente terminado con el propósito de indicar que es conveniente realizar una revisión detallada de ese trabajo antes de integrarlo por última vez en ``develop``. En esta revisión detallada, la persona encargada de procesar la *Pull Request* deberá comprobar, por ejemplo, que la correspondiente ``feature branch`` tiene todo el trabajo requerido para cumplir con la `definición de completado`_. Si faltasen elementos para cumplir con dicha definición, o se detectasen otros elementos a subsanar, se comentarán estas incidencias en la propia *Pull Request* y se esperará a que los elementos faltantes se completen o modifiquen antes de proceder a su integración. Obviamente, una vez que se subsanen las incidencias reportadas, hay que volver a verificar que dichas incidencias realmente hayan sido subsanadas.

Una vez verificado que la ``feature branch`` está libre de incidencias, y por tanto lista para ser integrada de manera definitiva en ``develop``, esta integración se realizará siguiendo el procedimiento general para la `integración de una feature branch en develop`_.

Trabajos en la ``release branch``
----------------------------------

Los trabajos que se recomiendan realizar en la *release branch* son:

#. Revisar ortografía de todos los documentos creados así como de la interfaz gráfica del producto.
#. Generar las versiones ``.pdf`` de todos los informes solicitados.
#. Generar las imágenes ``.png`` de todos los modelos solicitados.
#. Generar las imágenes ``.png`` correspondientes a los *mock-ups* elaborados, si los hubiere.
#. Generar el correspondiente fichero *apk*. Cada fichero *apk* deberá nombrarse de acuerdo a las `normas establecidas para nombrar fichero apk`_ .
#. Instalar el producto en diferentes terminales y verificar su correcto funcionamiento.

Esquema de Versionado
----------------------

Toda versión se identificará con tres números separados por puntos, conforme al patrón ``XX.YY.ZZ``, donde cada número posee el siguiente significado:

XX
  Un producto cambiará de versión principal cuando el conjunto de cambios que aporta con respecto a la versión principal anterior es bastante significativo desde el punto de vista del cliente. Por ejemplo, un cambio estético completo en la interfaz del producto podría implicar un cambio de versión principal. Los cambios de versiones principales suelen requerir un número de *sprints* considerable y una cuidadosa planificación a largo plazo. No se cambiará de versión principal a lo largo del proyecto integrado.

YY
  Representa el número de *versión secundaria* o subversión de un producto. Una *versión secundaria* dentro de una versión principal difiere de la versión secundaria anterior, dentro de esa misma versión principal, en un número de funcionalidades pequeño. Éste será el número de versión que se incremente al final de cada *sprint* durante el desarrollo del proyecto integrado.

ZZ
 Representa una actualización de una versión concreta ``XX.YY`` del producto software con un conjunto determinado de parches que solucionan una serie de *bugs* identificados en esa versión tras haber sido puesta en funcionamiento.

Dentro del proyecto integrado se comenzará con la versión ``00.00`` del producto y al finalizar cada *sprint* se deberá incrementar el número de versión secundaria del producto.

.. [#f1] Para forzar a que una fusión sea siempre recursiva, se debe especificar el parámetro ``--no-ff`` a la hora de ejecutar el comando de ``merge``, de manera que aunque sea posible realizar la fusión por *fast-forward*, ésta se realice de manera recursiva. Todos los clientes gráficos de Git tienen una opción para forzar la fusión no recursiva. En caso de duda, se aconseja preguntar al profesor.
