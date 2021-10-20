JUnit
======

* Si el código de alguna clase a probar hace uso de alguna librería de Android no se permite guardar la clase de prueba en el directorio test (aunque no sea necesario un emulador para su ejecución). Para evitar esto, se hace uso de Robolectric.
  Modo de uso de Robolectric:
  - Añadir las siguientes anotaciones a la clase de prueba:

.. code-block:: java

   @RunWith(RobolectricTestRunner.class)
   @Config(sdk = {Build.VERSION_CODES.O_MR1})
   public class ExampleUnitTestWithRobolectric { . . . }

   - Añadir lo siguiente al build.gradle

::

   android  {
      testOptions {
         unitTests {
            includeAndroidResources = true
         }
      }
   }

   testImplementation 'org.robolectric:robolectric:4.6'


