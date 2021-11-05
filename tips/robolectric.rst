Robolectric
===========

* Modo de uso de Robolectric:

  - Añadir las siguientes anotaciones a la clase de prueba:

    .. code-block:: java

        @RunWith(RobolectricTestRunner.class)
        @Config(sdk = {Build.VERSION_CODES.O_MR1})
        public class ExampleUnitTestWithRobolectric { . . . }


  - Añadir la siguiente configuración al build.gradle

    ::

      android  {
         testOptions {
            unitTests {
               includeAndroidResources = true
            }
         }
      }

      testImplementation 'org.robolectric:robolectric:4.6'

Texto de prueba para intentar averiguar cuál es el problema.
