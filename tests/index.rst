===============================
  Pruebas de Software
===============================

Niveles de prueba
=================

Los niveles de prueba a aplicar son los siguientes:

* Pruebas unitarias. Estas pruebas verifican el comportamiento de clases de manera aislada, usando para ello el framework JUnit y, en caso de ser necesario, las librerías Mockito, PowerMock o Robolectric. 

* Pruebas de integración. Estas pruebas verifican la interacción entre clases. Se llevarán a cabo usando el framework JUnit y las librerías Mockito, PowerMock o Robolectric si fuesen necesarias. 

* Pruebas de interfaz de usuario (UI Tests). Estas pruebas se pueden ver cómo el nivel más avanzado de las pruebas de integración, cuando se prueba la funcionalidad de todos los componentes de la aplicación de manera conjunta. Se llevarán a cabo usando el framework Espresso sobre JUnit.

* Pruebas de aceptación. Son las pruebas llevadas a cabo por el Product Owner durante el Sprint Review para comprobar si las historias de usuario elegidas para el Sprint se han realizado correctamente. Se ejecutarán de forma manual en el propio dispositivo del Product Owner u otro que se le proporcione. Las pruebas a realizar deberán definirse durante el Sprint Meeting.


Nomenclatura y organización de las clases de prueba
===================================================

Las clases de prueba correspondientes a pruebas unitarias:

* Se almacenan en el directorio test.

* Se denominan <NombreClase>Test.java donde <NombreClase> es el nombre de la clase bajo prueba y se definen en el mismo paquete que la clase bajo prueba.

Las clases de prueba correspondientes a pruebas de integración:

* Se almacenan en el directorio test. 

* El nombre de la clase de prueba será <NombreClase>ITest.java donde <NombreClase> es el nombre de la clase bajo prueba principal (en el sentido que es ella quién usa al resto de clases de la prueba, por ejemplo, si se prueba la interaccción entre una clase de negocio y una clase DAO, la clase principal sería la de negocio, pues serían sus métodos los que se probarían de manera directa). En este caso se definirá en el mismo paquete que la clase de prueba principal.

Las clases de prueba correspondientes a pruebas de interfaz de usuario:

* Se almacenan en el directorio androidTest.

* Se denominan <NombreEscenario>UITest.java y se almacenan en el mismo paquete dónde esté almacenada la vista que lanza el escenario.
