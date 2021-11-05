Robolectric
===========

  * Modo de uso de Robolectric:

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
