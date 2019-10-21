====================================================
 Definición de Completado
====================================================

El desarrollo de una historia de usuario, u otro elemento del backlog, se considerará como completado cuando cumpla con la siguiente *Definición de Completado*:

#. Se ha creado una implementación para dicha historia de usuario.
#. Se ha definido un plan de pruebas, incluyendo pruebas unitarias, de integración, de interfaz de usuario y de aceptación, para los elementos que forman parte de la implementación de dicha historia de usuario.
#. El plan de pruebas ha sido aprobado por el correspondiente comité, compuesto en este caso por los profesores de la asignatura de *Procesos de Ingeniería Sw*.
#. La implementación creada supera satisfactoriamente las pruebas unitarias contempladas en el plan de pruebas para esa historia de usuario.
#. La implementación creada supera satisfactoriamente las pruebas de integración contempladas en el plan de pruebas para esa historia de usuario.
#. La implementación creada supera satisfactoriamente las pruebas de interfaz de usuario contempladas en el plan de pruebas para esa historia de usuario.
#. La implementación creada supera satisfactoriamente las pruebas de aceptación contempladas en el plan de pruebas para esa historia de usuario.
#. Si ha habido algún cambio en el esquema de la base de datos de la aplicación, los cambios están reflejados en el modelo conceptual de datos.
#. Si ha habido cambios relevantes a nivel arquitectónico, estos cambios se han reflejado en el modelo que describe la arquitectura del sistema.
#. La rama correspondiente a la historia de usuario implementada se ha integrado en la rama ``develop``.
#. Se ha comprobado que, tras integrar la historia de usuario en la rama ``develop``, el producto completo sigue superando todos los test de aceptación.
#. Se ha verificado que la implementación creada, una vez unida al resto del producto, satisface los criterios de calidad de producto definidos por la organización.
#. Se ha generado el correspondiente `informe de calidad <../quality/index.html#informe-de-calidad>`_.
#. Se ha actualizado el manual de usuario de la aplicación para que refleje la nueva historia de usuario implementada.
#. Se ha generado un fichero .apk  que contiene el producto completo desarrollado hasta el momento más la nueva historia de usuario creada. Este .apk debería poder ser hecho público si el Product Owner así lo desease.
#. La nueva versión del producto está integrada en la rama ``master`` y convenientemente etiquetada.
#. El Product Owner ha confirmado que la historia de usuario se ajusta a sus necesidades.
