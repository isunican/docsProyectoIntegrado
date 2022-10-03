===========================
 Definición de Completado
===========================

.. _plan de pruebas: ../evaluation/procesos/index.html#planes-de-prueba
.. _informe de calidad: ../quality/index.html#informe-de-calidad

El desarrollo de una *historia de usuario*, u otro elemento del *Product Backlog*, se considerará como completado cuando cumpla con la siguiente *Definición de Completado*:

#. Se ha creado una implementación para dicho elemento del *Product Backlog*.
#. Se ha definido un `plan de pruebas`_ para los elementos que forman parte de la implementación de dicho elemento del *Product Backlog*.
#. El `plan de pruebas`_ ha sido aprobado por el correspondiente comité, compuesto en este caso por los profesores de la asignatura de *Procesos de Ingeniería Software*.
#. La implementación creada supera satisfactoriamente al menos dos de las pruebas unitarias contempladas en el `plan de pruebas`_ de dicho elemento del *Product Backlog*.
#. La implementación creada supera satisfactoriamente al menos una de las pruebas de interfaz de usuario contempladas en el `plan de pruebas`_ de dicho elemento del *Product Backlog*.
#. La implementación creada supera satisfactoriamente las pruebas de aceptación contempladas en el `plan de pruebas`_ de dicho elemento del *Product Backlog*.
#. Si la implementación de dicho elemento del *Product Backlog* ha requerido de algún cambio en las clases que conforman el modelo de dominio de la aplicación, los cambios están reflejados en el modelo UML asociado.
#. Si la implementación de dicho elemento del *Product Backlog* ha requerido de algún cambio a nivel arquitectónico, los cambios están reflejados en el modelo UML asociado.
#. La rama correspondiente al elemento del *Product Backlog* implementado se ha integrado en la rama ``develop``.
#. Se ha comprobado que, tras integrar la historia de usuario en la rama ``develop``, el producto completo sigue superando todos los tests previamente definidos.
#. Se ha verificado que la implementación creada, una vez unida al resto del producto, satisface los criterios de calidad de producto definidos por la organización.
#. Se han generado los correspondientes `informe de calidad`_ para ese *sprint*. Se piden al menos 2 informes de calidad por *sprint*.
#. Se ha actualizado el *manual de usuario* de la aplicación para que refleje el nuevo elemento del *Product Backlog* implementado.
#. Se ha generado un fichero *.apk*  que contiene el producto completo desarrollado hasta el momento más el nuevo elemento del *Product Backlog* implementado.
#. La nueva versión del producto está integrada en la rama ``master`` y convenientemente etiquetada.
#. El *Product Owner* ha confirmado que el nuevo elemento del *Product Backlog* implementado se ajusta a lo esperado y acordado.
