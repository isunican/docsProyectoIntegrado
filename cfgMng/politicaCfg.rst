==========================================
 Política de Gestión de la Configuración
==========================================

Estructura de Ramas
---------------------

La política de *Gestión de la Configuración* que se utilizará durante el desarrollo del proyecto integrado estará basada en el esquema de ramificación (*branching model*) GitFlow_.
De acuerdo con dicho esquema de ramificación, existirán en el repositorio de cada equipo de trabajo dos ramas principales, denominadas ``master`` y ``develop``, que estarán activas  toda la duración del proyecto, más una serie de ramas, denominadas ``feature branches``, ``release branches`` y ``hotfix branches`` cuyo tiempo de vida estará limitado, salvo circunstancias excepcionales, a un sprint. Describimos a continuación el contenido de cada una de estas ramas.

.. _gitflow: https://nvie.com/posts/a-successful-git-branching-model/

**Ramas Principales**

``master``
  Constituye la rama principal del proyecto y debe contener únicamente versiones del producto software, con todos sus artefactos asociados, que estén completamente listas para pasar a producción, es decir, ser puestas en funcionamiento real. La cabeza ``HEAD`` de dicha rama debe contener la última versión estable del producto, que debe estar lista para ser puesta en funcionamiento en cuanto el *Product Owner* lo indique.

``develop``
  Constituye una *rama de integración* en la cual los desarrolladores irán volcando el trabajo realizado de manera que, conforme a un *esquema de integración continua*, se pueda verificar periodicamente que no existen problemas de integración entre los cambios realizados en paralelo por diferentes miembros del equipo de trabajo.

**Ramas Secundarias**

``feature branches``
  Se utilizan para realizar el desarrollo de un elemento del *Product Backlog* como puede ser una *historia de usuario* o un *ticket de mantenimiento*. Todos los cambios que se tengan que realizar para implementar dicho elemento se llevarán a cabo dentro de una de estas ramas, que se tratará de mantener tan independiente como sea posible de otras ``feature branches``.

  Cada ``feature branch`` que se cree deberá tener como nombre ``feature/featureID-featureName``, donde ``featureID`` es el identificador numérico adjudicado por *ScrumDesk* al correspondiente item del *Sprint Backlog* y ``featureName`` es un nombre corto que se le dará a la rama para que su identificación sea menos críptica.

``release branches``
  Se utilizan para preparar una futura versión de producto que estará lista para ser puesta en producción. Su objetivo es permitir la realización pequeñas tareas relacionadas con la creación de una nueva versión oprativa del producto, como la generación de un ejecutable o el desarrollo de un nuevo instalador.

``hotfix branches`` [#f0]_
  Se utilizan para solucionar *bugs* críticos detectados en versiones en producción del producto que se está desarrollando que necesitan ser solucionados urgentemente. Todo el trabajo que sea necesario realizar para eliminar dicho *bug* se realizará dentro de una de estas ramas.

.. [#f0] Este tipo de ramas se incluyen en el esquema de ramificación del proyecto integrado por conformidad con GitFlow, pero no se tiene previsto su utilización.

Reglas de Gestión de la Configuracion
---------------------------------------

.. note::
    Estas reglas asumen que las ramas ``master`` y ``develop`` existen en el repositorio centralizado del equipo.

#. Cada elemento de un *product backlog* deberá desarrollarse en una ``feature branch`` independiente. Por tanto, al comienzo de cada sprint, se deberá crear una ``feature branch`` por cada elemento a desarrollar dentro de ese sprint, es decir, por cada elemento contenido dentro del *sprint backlog*.
#. Los trabajos correspondientes a cada elemento del *Sprint Backlog* se realizarán en su correspondiente ``feature branch``. Una ``feature branch`` podrá ser subramificada tanto como se desee a criterio de cada *Scrum Team*.
#. De acuerdo con los *esquemas de integración continua*, cada ``feature branch`` deberá ser integrada en ``develop`` periódicamente. Ninguna ``feature branch`` que esté recibiendo trabajo puede pasar más de dos días sin que haya sido integrada en ``develop``. El proceso de integración de una ``feature branch`` en develop se realizará siguiendo el procedimiento para la `integración de una feature branch en develop`_.
#. Cuando una ``feature branch`` esté completa, se creará un *Pull Request* para solicitar una integración más formal de dicha rama en ``develop``. El proceso de integración de este *Pull Request* en develop se realizará siguiendo el procedimiento para la `integración de un Pull Request en develop`_.
#. Cuando el trabajo contenido en ``develop`` esté listo para crear una nueva versión operativa del producto, se procederá a crear una ``release branch``. Dicha rama tendrá como nombre ``release/SR<id>-yy/mm/dd``, donde ``id`` es el número del sprint para el cual se produce la *release* e ``yy/mm/dd`` es la fecha, en formato anglosajón, de la *Product Review* para dicho sprint. En esta rama se realizarán todos los trabajos finales que sean  necesarios para crear una nueva versión operativa del software. Estos trabajos se detallan en la sección `trabajos en la release branch`_.
#. Cuando el trabajo contenido en la rama ``release`` esté terminado, dicha rama se fusionará con las ramas ``master`` y ``develop``. En ambos casos la fusión debe hacerse siempre de forma recursiva [#f1]_, de manera que genere siempre un nuevo *commit* en la rama destino.
#. Tras integrar la ``release branch``, los *commits* generados en la rama *master* y *develop* deberán etiquetarse como ``vXX.YY.ZZ-yy/mm/dd``, donde ``XX.YY.ZZ`` es el correspondiente número de versión, generado conforme al `esquema de versionado`_ del proyecto integrado, e ``yy/mm/dd`` es la fecha, en formato anglosajón, de la *Product Review* para dicho sprint.
#. Finalmente, las ``features branches`` y la ``release branch`` creadas para el desarrollo de un sprint, así como cualquier otra subrama creada durante el desarrollo de un sprint, se eliminarán justo antes del comienzo del siguiente sprint.

Integración de una ``feature branch`` en ``develop``
-----------------------------------------------------

Las integraciones de una ``feature branch`` en ``develop`` se realizarán de acuerdo al siguiente procedimiento:

#. Antes de realizar una integración de una ``feature branch`` en ``develop`` hay que verificar que el último commit de esta rama esté marcado como ``Success`` por el entorno de integración continua, *Travis* en nuestro caso.
#. La fusión de una ``feature branch`` en ``develop`` deberá ser siempre recursiva, es decir, generar un nuevo *commit de merge* [#f1]_.
#. Si la fusión generase conflictos, estos deberán resolverse de manera consensuada con el resto del equipo. Además, una vez resueltos los conflictos, los diferentes miembros del equipo deberán actualizar los archivos conflictivos en sus correspondientes ``feature branches``, de manera que se eviten nuevos futuros conflictivos [#f2]_.
#. Siempre que se integre nuevo trabajo en la rama ``develop`` del repositorio centralizado se ejecutará automáticamente el entorno de integración continua *Travis*. Al final de su ejecución, *Travis* marcará el correspondiente *commit* como ``Sucess`` o ``Failure``.

   a. Si el resultado es ``Sucess``, todo el trabajo existente en ``develop`` está libre de problemas de integración y el proceso se puede dar por terminado.
   b. Si el resultado es ``Failure``, existen problemas de integración que deben ser solucionados. En este caso, la rama ``develop`` queda bloqueada, no pudiendo recibir nuevas integraciones hasta que se solucionen dichos problemas de integración.

      Para resolver dichos problemas de integración, los responsables de la ``feature branch`` que haya generado el conflicto deberán realizar los cambios que sean necesarios en dicha ``feature branch``. Una vez realizados esos cambios, deberán repetir la fusión con la rama ``develop`` tantas veces como sea necesario hasta que *Travis* marque el correspondiente *commit* como ``Sucess``, momento en el cual la rama queda desbloqueada y puede recibir nuevas integraciones.

.. [#f2] Para obtener un único fichero de una versión determinada se puede utilizar el comando ``git checkout version fichero``.

Integración de un Pull Request en ``develop``
----------------------------------------------

La integración del *Pull Request* de una ``feature branch`` en ``develop`` se realizará siguiendo el mismo procedimiento general de integración de las ``feature branch`` en ``develop``, pero antes de proceder a dicha integración sobre la rama ``develop``, un miembro del equipo que no haya participado en el desarrollo de esa ``feature branch`` revisará, con la ayuda de *Sonar*, que el trabajo realizado se ajuste a las normas de calidad de la empresa.

Trabajos en la ``release branch``
----------------------------------

#. Generar las versiones ``.pdf`` de todos los informes solicitados.
#. Generar las imágenes ``.png`` de todos los modelos solicitados.
#. Generar las imágenes ``.png`` correspondientes a los *mock-ups* elaborados, si los hubiere.
#. Revisar ortografía de todos los documentos creados así como de la interfaz gráfica del producto.
#. Generar el correspondiente fichero *apk*.
#. Instalar el producto en diferentes terminales y verificar su correcto funcionamiento.

Esquema de Versionado
----------------------

Toda versión se identificará con tres números separados por puntos, conforme al patrón ``XX.YY.ZZ``, donde cada número posee el siguiente significado:

XX
  Un producto cambiará de versión principal cuando el conjunto de cambios que aporta con respecto a la versión principal anterior es bastante significativo desde el punto de vista del cliente.

  Por ejemplo, un cambio estético completo en la interfaz del producto podría implicar un cambio de versión principal.

  Los cambios de versiones principales suelen requerir un número de *sprints* considerable y una cuidadosa planificación a largo plazo.

YY
  Representa el número de *versión secundaria* o subversión de un producto. Una *versión secundaria* dentro de una versión principal difiere de la versión secundario anterior, dentro de esa misma versión principal, en un número de funcionalidades pequeño.

ZZ
 Representa una actualización de una versión concreta ``XX.YY`` del producto software con un conjunto determinado de parches que solucionan una serie de *bugs* identificados en esa versión tras haber sido puesta en funcionamiento.

Dentro del proyecto integrado se comenzará con la versión ``00.00`` del producto y al finalizar cada sprint se deberá incrementar el número de versión secundaria del producto.

.. [#f1] Para forzar a que una fusión sea siempre recursiva, se debe especificar el parámetro ``--no-ff`` a la hora de ejecutar el comando de ``merge``, de manera que aunque sea posible realizar la fusión por *fast-forward*, ésta se realice de manera recursiva.
