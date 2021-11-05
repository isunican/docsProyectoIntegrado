Robolectric
===========

* Modo de uso de Robolectric:

  - Añadir las siguientes anotaciones a la clase de prueba:

    .. code-block:: java

        @RunWith(RobolectricTestRunner.class)
        @Config(sdk = {Build.VERSION_CODES.O_MR1})
        public class ExampleUnitTestWithRobolectric { . . . }

Texto de prueba para intentar averiguar cuál es el problema.
