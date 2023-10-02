Espresso
=========

* `Hoja de referencia Espresso (Espresso Cheat Sheet) <https://developer.android.com/training/testing/espresso/cheat-sheet>`_

* En la versión actual de Espresso NO se puede desactivar programáticamente la wifi ni los datos

* Comprobar si un intent se abre con la info adecuada 

  ``intended(IntentMatchers.hasData(Uri.parse(uri)));``

* Abrir el menú de opciones 

  ``openActionBarOverflowOrOptionsMenu(ApplicationProvider.getApplicationContext());``

* Acceder al elemento i-ésimo de un listView 

  ``onData(anything()).inAdapterView(withId(R.id.listViewXX)).atPosition(i);``

* Acceder a un elemento gráfico dentro de un elemento de una listView 

  ``elementoLista = onData(anything()).inAdapterView(withId(R.id.listViewXX)).atPosition(i); 
  elementoLista.onChildView(withId(R.id.idElementoHijo));``

* Volver a la pantalla anterior 

  ``Espresso.pressBack();``

* Seleccionar una opción de un spinner 

  ``onView(withId(R.id.spinner)).perform(click());
  onData(allOf(is(instanceOf(String.class),is(“opción”))).perform(click());``

  Si el Spinner está dentro de un Dialog:

  ``onView(withId(R.id.spinner)).perform(click());
  onData(allOf(is(instanceOf(String.class),is(“opción”))).inRoot(isPlatformPopup()).perform(click());``

* Activar permisos de la aplicación 

  ``@Rule public GrantPermissionRule permissionRule = GrantPermissionRule.grant(android.Manifest.permission.ACCESS_FINE_LOCATION);``
  
  Es necesario añadir la siguiente dependencia en el build.gradle:
  
  ``androidTestImplementation 'androidx.test:rules:1.2.0'``

* Desactivar acceso a internet

  ``InstrumentationRegistry.getInstrumentation().getUiAutomation().executeShellCommand("svc wifi disable");``
  ``InstrumentationRegistry.getInstrumentation().getUiAutomation().executeShellCommand("svc data disable");``

  Para volver a activar internet:

  ``InstrumentationRegistry.getInstrumentation().getUiAutomation().executeShellCommand("svc wifi enable");``
  ``InstrumentationRegistry.getInstrumentation().getUiAutomation().executeShellCommand("svc data enable");``

* Para rotar la pantalla
  
  Añadir la dependencia a UIAutomator: ``androidTestImplementation 'androidx.test.uiautomator:uiautomator:2.2.0'``
  
  Para rotar: 
  
  ``UiDevice device = UiDevice.getInstance(getInstrumentation());``
  ``device.setOrientationLeft();``

* Comprobar que un Toast se ha mostrado correctamente

  ``onView(withText("String del toast")).inRoot(RootMatchers.withDecorView(not(decorView))).check(matches(isDisplayed()));``

  Para obtener el objeto decorView, añadir lo siguiente al método @Before

  ``activityRule.getScenario().onActivity(activity -> decorView = activity.getWindow().getDecorView());``

* Cerrar y volver a abrir la aplicación

  ``pressBackUnconditionally();``
  ``activityRule.getScenario().close();``
  ``ActivityScenario.launch(MainView.class);``

  donde activityRule es el objeto de tipo ActivityScenarioRule creada al inicio del test.

