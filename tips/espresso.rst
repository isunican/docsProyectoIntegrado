Espresso
=========

* En la versión actual de Espresso NO se puede desactivar programáticamente la wifi ni los datos

* Comprobar si un intent se abre con la info adecuada 

  ``intended(IntentMatchers.hasData(Uri.parse(uri)));``

* Abrir el menú de opciones 

  ``openActionBarOverflowOrOptionsMenu(InstrumentationRegistry.getInstrumentation().getContext());``

* Acceder al elemento i-ésimo de un listView 

  ``onData(anything()).inAdapterView(withId(R.id.listViewXX)).atPosition(i);``

* Acceder a un elemento gráfico dentro de un elemento de una listView 

  ``elementoLista = onData(anything()).inAdapterView(withId(R.id.listViewXX)).atPosition(i); 
  elementoLista.onChildView(withId(R.id.idElementoHijo));``

* Volver a la pantalla anterior 

  ``Espresso.pressBack();``

* Seleccionar una opción de un spinner 

  ``onView(withId(R.id.spinner)).perform(click());
  onView(withId(R.id.textview_in_custom_spinner)).perform(click());``

* Activar permisos de la aplicación 

  ``@Rule public GrantPermissionRule permissionRule = GrantPermissionRule.grant(android.Manifest.permission.ACCESS_FINE_LOCATION);``

* Desactivar acceso a internet

  ``InstrumentationRegistry.getInstrumentation().getUiAutomation().executeShellCommand("svc wifi disable");``
  ``InstrumentationRegistry.getInstrumentation().getUiAutomation().executeShellCommand("svc data disable");``

  Para volver a activar internet:

  ``InstrumentationRegistry.getInstrumentation().getUiAutomation().executeShellCommand("svc wifi enable");``
  ``InstrumentationRegistry.getInstrumentation().getUiAutomation().executeShellCommand("svc data enable");``

* Para rotar la pantalla
  
  Añadir la dependencia a UIAutomator: ``androidTestImplementation 'androidx.test.uiautomator:uiautomator:2.2.0'``
  
  Para rotar: 
  
  .. code-block:: java
     UiDevice device = UiDevice.getInstance(getInstrumentation());
     device.setOrientationLeft();

