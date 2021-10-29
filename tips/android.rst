Android
=========

  * `Obtener localización actual <https://developer.android.com/training/location/retrieve-current>`_
  * Cargar una imagen a partir de su URL en un ImageView: ``Picasso.get().load("URL de la imagen").into(imageView);``
  * Acceso al sistema de ficheros para leer/escribir ficheros: cada app en Android tiene asignada una región privada en la que puede crear ficheros. La `documentación oficial <https://developer.android.com/training/data-storage/app-specific#internal-access-files>`_ incluye información sobre cómo acceder a estos ficheros.
  * Ventanas emergentes flotantes: básicamente tenéis que crear un objeto ``AlertDialog.Builder``, y llamar a sus métodos para incluir botones, título, *checkboxes*, etc. Por último, el diálogo se crea con el método ``create()``, y se lanza con ``show()``. Podéis ampliar información en la `entrada correspondiente de la guía oficial de Android <https://developer.android.com/guide/topics/ui/dialogs>`_ o en este `tutorial alternativo <https://www.tutorialspoint.com/android/android_alert_dialoges.htm>`_.
  * Menu deslizante (*DrawerLayout*): `Ejemplo sencillo incluyendo Espresso <https://github.com/rivasjm/DrawerLayoutExample>`_, `guía oficial <https://developer.android.com/guide/navigation/navigation-ui#add_a_navigation_drawer>`_, y un `tutorial en castellano <https://danielme.com/2018/12/19/diseno-android-menu-lateral-con-navigation-drawer/>`_
  * *SharedPreferences*: `guardar/leer preferencias de la aplicación (key-value) <https://developer.android.com/training/data-storage/shared-preferences>`_.
  * Base de datos: La forma recomendada es mediante la librería `Room <https://developer.android.com/training/data-storage/room>`_. Se puede utilizar `SQLite directamente también <https://developer.android.com/training/data-storage/sqlite>`_
  * `Ofuscación (con ProGuard) <https://www.raywenderlich.com/7449-getting-started-with-proguard>`_
  * `Autenticación (con Firebase) <https://firebase.google.com/docs/auth/?utm_source=studio>`_
  * `Asegurar comunicaciones de datos en red (https) <https://www.raywenderlich.com/5634-securing-network-data-tutorial-for-android>`_
  * `Varios tutoriales en castellano: <http://www.sgoliver.net/blog/curso-de-programacion-android/indice-de-contenidos/>`_
  * `Ideas para usar SharedPreferences manteniendo el Presenter independiente de la interfaz de Android <https://stackoverflow.com/questions/52367436/android-mvp-share-preference>`_
