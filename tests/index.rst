===============================
  Pruebas Sw
===============================

Niveles de prueba
=================

Los niveles de prueba a aplicar son los siguientes:

* Pruebas unitarias. Estas pruebas tratan de verificar el comportamiento de clases de manera aislada, usando para ello el framework JUnit y, en caso de ser necesario simular el comportamiento de clases de las que se dependa, la librería Mockito. 

* Pruebas de integración: Estas pruebas tratan de verificar la interacción entre diferentes clases del proyecto. Se llevarán a cabo usando el framework JUnit y la librería Mockito si es necesaria. 

* Pruebas de interfaz de usuario (UI Tests): Estas pruebas se pueden ver cómo el nivel más avanzado de las pruebas de integración, cuando se prueban todos los componentes de la aplicación de manera conjunta. Se llevarán a cabo usando el framework Espresso. 

En este caso, cómo la fuente de datos de la que se depende es dinámica, es complejo el diseño de un conjunto de pruebas con comportamiento determinista, por lo que podría ser necesaria la utilización de Mocks para poder trabajar con un conjunto de datos conocidos (en ese caso seguirían siendo pruebas de integración pero las distinguimos de las anteriores por involucrar a la interfaz gráfica). 

* Pruebas de aceptación: Son las pruebas llevadas a cabo por los Product Owners durante el Sprint Review para comprobar si las historias de usuario elegidas para el Sprint se han realizado correctamente. Se ejecutarán de forma manual en el propio dispositivo del Product Owner u otro que se le proporcione. Las pruebas a realizar deberán definirse en durante el Spring Initial Meeting.


Nomenclatura y organización de las clases de prueba
===================================================

Las clases de prueba correspondientes a pruebas unitarias:

* Se almacenan en la carpeta test dentro del mismo paquete que la clase bajo prueba.

* Se denominan <NombreClase>Test.java.

Las clases de prueba correspondientes a pruebas de integración:

* Se almacenan en la carpeta test si no requieren la ejecución del emulador o en la carpeta androidTest en caso contrario. 

* El nombre de la clase de prueba será:
  - <NombreClase>ITest.java si se trata de la prueba de una clase completa (se aplica estrategia de integración incremental). En este caso se almacenará en el mismo paquete que la clase de prueba.
  - <NombreEscenario>ITest.java si la clase prueba un determinado escenario de ejecución de una historia de usuario (se aplica estrategia de integración funcional). En este caso se almacenará en el mismo paquete dónde esté almacenada la vista que lanza el escenario.

Las clases de prueba correspondientes a pruebas de interfaz de usuario:

* Se almacenarán en la carpeta androidTest.

* Llevarán por nombre <NombreEscenario>UITest.java y se almacenarán en el mismo paquete dónde esté almacenada la vista que lanza el escenario.
