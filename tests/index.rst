===============================
  Pruebas Sw
===============================

Niveles de prueba
=================

Los niveles de prueba a aplicar son los siguientes:

* Pruebas unitarias. Estas pruebas tratan de verificar el comportamiento de clases de manera aislada, usando para ello el framework JUnit y, en caso de ser necesario simular el comportamiento de clases de las que se dependa, la librer�a Mockito. 
* Pruebas de integraci�n: Estas pruebas tratan de verificar la interacci�n entre diferentes clases del proyecto. Se llevar�n a cabo usando el framework JUnit.
* Pruebas de interfaz de usuario (UI Tests): Estas pruebas se pueden ver c�mo el nivel m�s avanzado de las pruebas de integraci�n, cuando se prueban todos los componentes de la aplicaci�n de manera conjunta. Se llevar�n a cabo usando el framework Espresso. C�mo la fuente de datos de la que se depende es din�mica, es compleja el dise�o de un conjunto de pruebas con comportamiento determinista, por lo que puede ser necesaria la utilizaci�n de Mocks que simulen el comportamiento de la fuente de datos. 
* Pruebas de aceptaci�n: Son las pruebas llevadas a cabo por los Product Owners durante el Sprint Review para comprobar si las historias de usuario elegidas para el Sprint se han realizado correctamente. Se ejecutar�n de forma manual en el propio dispositivo del Product Owner u otro que se le proporcione. Las pruebas a realizar deber�n definirse en durante el Spring Initial Meeting.


Nomenclatura y organizaci�n de las clases de prueba
===================================================
* Las clases de prueba correspondientes a pruebas unitarias se almacenan en la carpeta test, en el mismo paquete que la clase bajo prueba  y deben denominarse <NombreClase>Test.java.
* Las clases de prueba correspondientes a pruebas de integraci�n se almacenar�n en la carpeta test si no requieren la ejecuci�n del emulador o en la carpeta androidTest en caso contrario. El nombre de la clase de prueba ser�:
  * <NombreClase>ITest.java si la clase prueba una clase completa utilizando una estrategia de integraci�n incremental.
  * <NombreEscenario>ITest.java si la clase prueba un determinado escenario de ejecuci�n utilizando una estrategia de integraci�n funcional.
* Las clases de prueba correspondientes a pruebas de interfaz de usuario se almacenar�n en la carpeta androidTest y llevar�n por nombre <NombreEscenario>UITest.java.
