===============================
  Pruebas Sw
===============================

Niveles de prueba
=================

Los niveles de prueba a aplicar son los siguientes:

* Pruebas unitarias. Estas pruebas tratan de verificar el comportamiento de clases de manera aislada, usando para ello el framework JUnit y, en caso de ser necesario simular el comportamiento de clases de las que se dependa, la librería Mockito. 
* Pruebas de integración: Estas pruebas tratan de verificar la interacción entre diferentes clases del proyecto. Se llevarán a cabo usando el framework JUnit.
* Pruebas de interfaz de usuario (UI Tests): Estas pruebas se pueden ver cómo el nivel más avanzado de las pruebas de integración, cuando se prueban todos los componentes de la aplicación de manera conjunta. Se llevarán a cabo usando el framework Espresso. Cómo la fuente de datos de la que se depende es dinámica, es compleja el diseño de un conjunto de pruebas con comportamiento determinista, por lo que puede ser necesaria la utilización de Mocks que simulen el comportamiento de la fuente de datos. 
* Pruebas de aceptación: Son las pruebas llevadas a cabo por los Product Owners durante el Sprint Review para comprobar si las historias de usuario elegidas para el Sprint se han realizado correctamente. Se ejecutarán de forma manual en el propio dispositivo del Product Owner u otro que se le proporcione. Las pruebas a realizar deberán definirse en durante el Spring Initial Meeting.


Nomenclatura y organización de las clases de prueba
===================================================
* Las clases de prueba correspondientes a pruebas unitarias se almacenan en la carpeta test, en el mismo paquete que la clase bajo prueba  y deben denominarse <NombreClase>Test.java.
* Las clases de prueba correspondientes a pruebas de integración se almacenarán en la carpeta test si no requieren la ejecución del emulador o en la carpeta androidTest en caso contrario. El nombre de la clase de prueba será:
  * <NombreClase>ITest.java si la clase prueba una clase completa utilizando una estrategia de integración incremental.
  * <NombreEscenario>ITest.java si la clase prueba un determinado escenario de ejecución utilizando una estrategia de integración funcional.
* Las clases de prueba correspondientes a pruebas de interfaz de usuario se almacenarán en la carpeta androidTest y llevarán por nombre <NombreEscenario>UITest.java.
