==========================================
 Política de Gestión de la Configuración
==========================================

Estructura de Ramas
---------------------

La política de *Gestión de la Configuración* que se utilizará durante el desarrollo del proyecto integrado estará basada en el esquema de ramificación (*branching model*) GitFlow_.
De acuerdo con dicho esquema, en el repositorio de cada equipo de trabajo deberán existir dos ramas principales, denominadas ``master`` y ``develop``. Estas ramas estarán activas durante toda la duración del proyecto. Además, para el desarrollo de los sprints, se deberán crear una serie de ramas temporales, denominadas ``feature branches``, ``release branches`` y ``hotfix branches``. El tiempo de vida de estas ramas estará limitado, salvo circunstancias excepcionales, a un sprint. Describimos a continuación el contenido de cada una de estas ramas.

.. _gitflow: https://nvie.com/posts/a-successful-git-branching-model/

**Ramas Principales**

``master``
  Constituye la rama principal del proyecto y debe contener únicamente versiones del producto software, con todos sus artefactos asociados,  completamente operativas para pasar a producción. Es decir, cualquier versión contenida dentro de dicha rama podría ser una *release* del producto.

``develop``
  Constituye una *rama de integración* en la cual los desarrolladores irán incorporando los cambios realizados por cada uno de ellos, de manera que se pueda verificar periódicamente, conforme a un *esquema de integración continua*, que no existen problemas de integración entre dichos cambios.

**Ramas Secundarias**

``feature branches``
  Una ``feature branch`` es una rama que se utiliza para desarrollar un  elemento concreto del *Product Backlog*. Por tanto, por cada ítem del *Product Backlog* a desarrollar dentro de un sprint, se deberá crear una ``feature branch`` nueva. Todos los cambios que sea necesario realizar para desarrollar dicho elemento del *Product Backlog* se almacenarán dentro de la nueva ``feature branch`` creada. Cada ``feature branch`` se deberá tratar de  mantener tan independiente como sea posible de las otras ``feature branches`` que se encuentren activas durante el desarrollo de un sprint. El tiempo de vida de una ``feature branch`` está limitado al sprint donde se desarrolla su correspondiente ítem del *Product Backlog*.

``release branches``
  Una ``release branches`` se utiliza para realizar todas las tareas que sean comunes a la preparación de una nueva versión operativa del producto, de manera previa a su integración en ``master``. Un ejemplo de estas tareas podría ser la creación de un instalador del producto, o la generación de un nuevo ejecutable.

``hotfix branches`` [#f0]_
  Una ``hotfix branch`` se utiliza para solucionar *bugs* críticos detectados en versiones en producción del producto y que necesitan ser solucionados urgentemente, sin existir una planificación previa. En este caso, se crea una rama directamente desde la versión de master que haya que corregir y se realiza en ella todo el trabajo que sea necesario para eliminar el *bug* detectado.

.. [#f0] Este tipo de ramas se incluyen en el esquema de ramificación del proyecto integrado por completitud, al formar parte de *GitFlow*, pero no se hará uso de las mismas durante el desarrollo del proyecto integrado.

Reglas de Gestión de la Configuración
---------------------------------------

.. https://proyecto-integrado-ingenieria-del-sw.readthedocs.io/es/latest/cfgMng/politicaCfg.html#integracion-de-una-feature-branch-en-develop

.. note::
    Estas reglas asumen que las ramas ``master`` y ``develop`` existen en el repositorio centralizado del equipo.

#. Cada elemento de un *Product Backlog* deberá desarrollarse en una ``feature branch`` independiente. Por tanto, al comienzo de cada sprint, se deberá crear una ``feature branch`` por cada elemento a desarrollar dentro de ese sprint, es decir, por cada elemento contenido dentro del *Sprint Backlog*. Además, cada ``feature branch`` deberá tener como nombre ``feature/featureID-featureName``, donde ``featureID`` es el identificador numérico adjudicado por *ScrumDesk* al correspondiente ítem del *Sprint Backlog*; y, ``featureName`` es un nombre corto que se le dará a la rama para que su identificación sea menos críptica.
#. Los trabajos correspondientes a cada elemento del *Sprint Backlog* se realizarán en su correspondiente ``feature branch``. Una ``feature branch`` podrá ser subramificada tanto como se desee a criterio de cada *Scrum Team*.
#. De acuerdo con los *esquemas de integración continua*, cada ``feature branch`` deberá ser integrada en ``develop`` periódicamente. Por ello, se establece como norma, que ninguna ``feature branch`` que esté recibiendo trabajo puede estar más de dos días sin que haya sido integrada en ``develop``. Este proceso de integración se realizará siguiendo el procedimiento para la `integración de una feature branch en develop`_.
#. Cuando un elemento del *Sprint Backlog* esté completo, se creará un *Pull Request* para solicitar formalmente la  integración de su correspondiente *feature branch* en ``develop``. Este *Pull Request* se procesará siguiendo el procedimiento para la `integración de un Pull Request en develop`_.
#. Cuando el trabajo contenido en ``develop`` esté listo para crear una nueva versión operativa del producto, se procederá a crear una ``release branch``. Dicha rama tendrá como nombre ``release/SR<id>.yy-mm-dd``, donde ``id`` es el número del sprint para el cual se produce la *release*; e ``yy-mm-dd`` es la fecha, en formato anglosajón, de la *Product Review* de dicho sprint. En esta rama se realizarán todos los trabajos finales que sean  necesarios para crear una nueva versión operativa del software. Estos trabajos se detallan en la sección `trabajos en la release branch`_.
#. Cuando el trabajo contenido en la rama ``release`` esté terminado, dicha rama se fusionará con las ramas ``master`` y ``develop``. En ambos casos la fusión debe hacerse siempre de forma recursiva [#f1]_, por lo que deberá aparecer un único  nuevo *commit* en la rama destino.
#. Tras integrar la ``release branch``, el *commit* generado en la rama *master* deberá etiquetarse como ``vXX.YY.ZZ``, donde ``XX.YY.ZZ`` es el correspondiente número de versión. este número de versión deberá ser conforme al `esquema de versionado`_ del proyecto integrado.
#. Finalmente, todas las ramas que no sean ``features branches`` o ``release branches`` que hayan sido creadas durante el transcurso del sprint deberán ser eliminadas del repositorio remoto.

Integración de una ``feature branch`` en ``develop``
-----------------------------------------------------

Las integraciones de una ``feature branch`` en ``develop`` se realizarán de acuerdo al siguiente procedimiento:

#. Antes de realizar una integración de una ``feature branch`` en ``develop``, se deberá verificar que el último commit de ``develop`` esté marcado como ``Success`` por el entorno de integración continua *GitHub Actions*. En caso de no estarlo, habrá que esperar a que lo esté.
#. A continuación, se verificará que la versión local de la rama ``develop`` esté complementamente actualizada.
#. Tras realizar las comprobaciones anteriores, se deberá integrar, de manera local, la ``feature branch`` que corresponda dentro de ``develop``. Esta fusión deberá ser siempre recursiva, es decir, generar un nuevo *commit de merge* [#f1]_.
#. Si la fusión generase conflictos, estos deberán resolverse de manera consensuada con el resto del equipo.
#. La nueva rama ``develop``, con la ``feature branch`` integrada, deberá subirse al repositorio remoto. Al detectarse un nuevo *commit* en ``develop``, se ejecutará automáticamente el entorno de integración continua *GitHub Actions*. Al final de su ejecución, *GitHub Actions* marcará el correspondiente *commit* como ``Success`` o ``Failure``.

   a. Si el resultado es ``Success``, todo el trabajo existente en ``develop`` está libre de problemas de integración y este proceso se da por terminado.
   b. Si el resultado es ``Failure``, es porque existen problemas de integración. En este caso, la rama ``develop`` queda bloqueada, no pudiendo recibir nuevas integraciones hasta que se solucionen dichos problemas de integración. Por tanto, se deberá trabajar en la solución de estos problemas con la mayor prontitud posible.

   Para resolver dichos problemas de integración, los responsables de la ``feature branch`` que haya generado el conflicto deberán realizar los cambios que sean necesarios en dicha ``feature branch``. Una vez realizados esos cambios, volverán a repetir este procedimiento desde el punto 3.

#. En caso de haberse detectado conflictos,  una vez resueltos los mismos, los diferentes miembros del equipo deberán actualizar los archivos conflictivos en sus correspondientes ``feature branches``, de manera que se eviten nuevos conflictos en el futuro [#f2]_.

.. [#f2] Para obtener un único fichero de una versión determinada se puede utilizar el comando ``git checkout version fichero``.

Integración de un Pull Request en ``develop``
----------------------------------------------

Antes de integrar un *Pull Request* en en ``develop``, la persona encargada de realizar la integración de la rama deberá comprobar que la correspondiente ``feature branch`` tiene todo el trabajo requerido para cumplir con la `definición de completado <https://proyecto-integrado-ingenieria-del-sw.readthedocs.io/es/latest/scrum/definicionCompletado.html>`_. Si faltasen elementos para cumplir con dicha definición, deberá comentarlo en el *Pull Request* y esperar a que los elementos faltantes se completen o modifiquen.

Una vez verificado que están todo los elementos requeridos para cumplir con la definición de completado, la integración del *Pull Request*  se realizará siguiendo el procedimiento general para la `integración de una feature branch en develop`_.

 .. pero antes de proceder a dicha integración sobre la rama ``develop``, un miembro del equipo que no haya participado en el desarrollo de esa ``feature branch`` revisará, con la ayuda de *Sonar*, que el trabajo realizado se ajuste a las normas de calidad de la empresa.

Trabajos en la ``release branch``
----------------------------------

#. Revisar ortografía de todos los documentos creados así como de la interfaz gráfica del producto.
#. Generar las versiones ``.pdf`` de todos los informes solicitados.
#. Generar las imágenes ``.png`` de todos los modelos solicitados.
#. Generar las imágenes ``.png`` correspondientes a los *mock-ups* elaborados, si los hubiere.
#. Generar el correspondiente fichero *apk*. Cada fichero *apk* deberá nombrarse conforme al patrón ``<nombreApp>-<GG>-<XX.YY.ZZ>``, donde ``nombreApp`` es el nombre que cada equipo quiera darle a su aplicación; ``GG`` será el número asignado al equipo de trabajo; y, ``XX.YY.ZZ`` es el correspondiente número de versión, que deberá ser conforme al `esquema de versionado`_ del proyecto integrado.
#. Instalar el producto en diferentes terminales y verificar su correcto funcionamiento.

Esquema de Versionado
----------------------

Toda versión se identificará con tres números separados por puntos, conforme al patrón ``XX.YY.ZZ``, donde cada número posee el siguiente significado:

XX
  Un producto cambiará de versión principal cuando el conjunto de cambios que aporta con respecto a la versión principal anterior es bastante significativo desde el punto de vista del cliente.

  Por ejemplo, un cambio estético completo en la interfaz del producto podría implicar un cambio de versión principal.

  Los cambios de versiones principales suelen requerir un número de *sprints* considerable y una cuidadosa planificación a largo plazo.

YY
  Representa el número de *versión secundaria* o subversión de un producto. Una *versión secundaria* dentro de una versión principal difiere de la versión secundaria anterior, dentro de esa misma versión principal, en un número de funcionalidades pequeño.

ZZ
 Representa una actualización de una versión concreta ``XX.YY`` del producto software con un conjunto determinado de parches que solucionan una serie de *bugs* identificados en esa versión tras haber sido puesta en funcionamiento.

Dentro del proyecto integrado se comenzará con la versión ``00.00`` del producto y al finalizar cada sprint se deberá incrementar el número de versión secundaria del producto.

.. [#f1] Para forzar a que una fusión sea siempre recursiva, se debe especificar el parámetro ``--no-ff`` a la hora de ejecutar el comando de ``merge``, de manera que aunque sea posible realizar la fusión por *fast-forward*, ésta se realice de manera recursiva.
