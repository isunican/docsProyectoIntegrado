Robolectric
============

Utilización de Robolectric
---------------------------

Si el código de una clase hace uso de librerías *Android* no se permite la ejecución de su correspondiente clase de prueba desde el directorio test (aunque no sea necesario un emulador para su ejecución).
Para evitar esto, se hace uso de *Robolectric*. Para incorporar *Robolectric* a un proyecto Android:

  1. Añadir las siguientes anotaciones a la clase de prueba:

    .. code-block:: java

        @RunWith(RobolectricTestRunner.class)
        @Config(sdk = {Build.VERSION_CODES.O_MR1})
        public class ExampleUnitTestWithRobolectric { . . . }

  2. Añadir la siguiente configuración al build.gradle

    ::

      android  {
         testOptions {
            unitTests {
               includeAndroidResources = true
            }
         }
      }

      testImplementation 'org.robolectric:robolectric:4.6'

Obtener una referencia al `Context` desde una clase de prueba *Robolectric*
----------------------------------------------------------------------------

  1. Poner en el código: ``Context context  = ApplicationProvider.getApplicationContext();``
  2. Añadir la siguiente dependencia a build.gradle: ``testImplementation 'androidx.test:core:1.0.0'``
