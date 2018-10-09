===============================
  Gestión de la Calidad
===============================

Introducción
===================

La aplicación Android desarrollada como proyecto integrado de las asignaturas de intensificación de Ingeniería del Software, ha de satisfacer unos umbrales de calidad mínimos. Por lo tanto, dentro de las tareas a realizar habrá que analizar la calidad de producto y llevar a cabo las correcciones necesarias para que cumpla los criterios de calidad.

La manera de proceder será por historia de usuario, de modo que para cada una se designará un responsable de calidad. Dicho responsable deberá tomar el código implementado para dicha historia, realizar el análisis de calidad, interpretarlo y en caso de no cumplir los criterios de calidad exigidos, realizar las correcciones necesarias y volver a realizar el análisis.

Como herramienta utilizaremos SonarQube, que realiza análisis estático del código fuente detectando aspectos como código clonado, concordancia con estándares de programación, búsqueda de bugs o cobertura de pruebas. A cada uno de estos aspectos detectados, le asigna un valor de tiempo llamado “deuda técnica”, que podríamos definir como el coste y los intereses a pagar por hacer mal las cosas (el sobre esfuerzo a pagar por mantener un software mal hecho). Hay que tener en cuenta que sólo una parte de esta deuda es intrínseca al código y podemos medirla mediante analizadores, y que también puede venir asociada a aspectos relacionados con el proceso, arquitectura, diseño, tecnologías, etc.

Dispondremos de un servidor donde alojar los informes de los análisis de nuestro proyecto. Este servidor corresponde a la organización isuc de  `SonarCloud <https://sonarcloud.io/organizations/isuc/projects>`_ y en él están configurados los umbrales de calidad y el conjunto de reglas a usar en nuestros proyectos Android.
Por otro lado, en el cliente podremos lanzar el análisis de SonarQube mediante línea de comandos o de forma automatizada dentro del proceso de integración contínua. Además, dispondremos del complemento SonarLint para Android Studio que permitirá enlazar con la configuración de nuestro servidor y así gestionar las incidencias de forma cómoda desde nuestro IDE.


Configuración del servidor
=============================

Para utilizar SonarQube debemos tener por un lado un servidor donde se configurarán las reglas y umbrales a aplicar y se alojarán los distintos análisis realizados para cada proyecto. Por otro lado, se requiere de un cliente que analice el código y suba los resultados al servidor.

Podemos optar por instalar nuestro propio servidor utilizando las fuentes oficiales (existen versiones para distintos sistemas operativos) o utilizar servicios en la nube que lo proporcionan. Nosotros utilizaremos `SonarCloud <https://sonarcloud.io>`_, que es el servicio en la nube oficial y se ofrece de forma gratuita para proyectos públicos de código abierto. Dentro de SonarCloud hemos creado una organicación `isuc <https://sonarcloud.io/organizations/isuc/projects>`_ con todo lo necesario, así que únicamente deberéis compilar el proyecto con la configuración proporcionada, los análisis se subirán y podréis acceder a ellos en la dirección pública de la organización `isuc <https://sonarcloud.io/organizations/isuc/projects>`_.



Configuración del cliente
===============================

El analizador desde el cliente puede lanzarse desde línea de comandos o como parte del proceso de integración contínua. En ambos casos, la configuración necesaria para lanzar dichos análisis está proporcionada en el proyecto inicial aunque a continuación se detalla.

Tal y como puede observarse en el fichero de configuración ``gradle.build``, se hace uso del `complemento oficial de SonarQube para gradle <https://plugins.gradle.org/plugin/org.sonarqube>`_ y de una serie de propiedades que establecen datos como la url del servidor, la organización, en nombre y clave del proyecto y un token de autorización.


build.gradle
-------------

::

  plugins {
      id "org.sonarqube" version "2.6.2" }

  apply plugin: "jacoco"

  sonarqube {
      properties {
          property "sonar.host.url", "https://sonarcloud.io"
          property "sonar.organization", "isuc"
          property "sonar.login", "120537998e2c122476f30cade8d4a25865210fa6"
          property "sonar.projectKey", "CalculadoraTest"
          property "sonar.projectName", "CalculadoraTest"
          property "sonar.jacoco.reportPaths", "${project.buildDir}/jacoco/testDebugUnitTest.exec"
      }
  }


.. note:: Para hacer que el informe de sonar incluya la cobertura de pruebas se utilizará el complemento ``jacoco``. Habrá que lanzar ``gradlew.bat test`` antes que ``gradlew.bat sonarqube`` para que genere los ficheros correspondientes a los informes de cobertura, que mediante un parámetro de configuración indicamos para que se transmitan al servidor.

Complemento SonarLint para Android Studio
-----------------------------------------

Existe un complemento que podemos instalar en Android Studio para analizar la calidad del código, mostrándonos las incidencias con su clasificación (tipo, severidad, etc.), descripción de la regla que la ha activado, etc. Es bastante útil ya que nos permite seleccionar una incidencia e ir directamente a la parte del código donde se encuentra. Otra ventaja importante es que además de poder trabajar con una configuración por defecto, permite conectarnos a un servidor (propio o SonarCloud) y usar las reglas y quality gate configuradas para tu organización.

Para instalarlo la forma más sencilla es desde Preferencias -> Plugins -> Browse Repositories -> SonarLint, y al finalizar, reiniciar Android Studio. Debería aparecernos la pestaña de SonarLint en la parte baja de la interfaz.

Para la conexión con el servidor habrá que ir a Preferences -> Other Settings ->

*	SonarLint General Settings. Permitirá agregar el servidor SonarCloud o propio, meter nuestra clave y seleccionar nuestra organización (dichos valores aparecen en el fichero ``gradle.build``).

*	SonarLint Project Settings. Una vez realizado el paso anterior podremos seleccionar un proyecto en concreto.

Tras la configuración, podremos ejecutar análisis para un único fichero o el proyecto completo, mediante el menú contextual del proyecto (botón derecho) dentro de las opciones de SonarLint.



Análisis de la calidad de producto
========================================

Durante el desarrollo del proyecto integrado se realizarán Sprints en los que se desarrollarán historias de usuario. Para cada historia de usuario se nombrará un responsable de calidad que deberá realizar las acciones necesarias para que la codificación realizada cumpla con los umbrales establecidos, es decir, que pase de forma satisfactoria el quality gate.

Por lo tanto, los pasos que deberá realizar son:

*	Tomar el código desarrollado y subir el análisis al servidor SonarCloud, dentro de la organización isuc, con el id de su proyecto y su clave.

*	Observar los resultados del análisis, comprobando si ha pasado o no el quality gate establecido y que además, en la medida de lo posible, obtenga clasificación A en los 3 apartados: reliability (bugs), security (vulnerabilities) y maintainability (code smells).

*	Tras el análisis deberá decidir qué incidencias arreglar y hacerlo en el código. El complemento SonarLint facilita esta tarea. Tras hacer las mejoras se resubirá el análisis a SonarCloud para observar la situación actual, realizando este proceso hasta alcanzar la calidad exigida.

Informe de Calidad
===================

El proceso anterior se documentará en un informe que deberá estar en el repositorio del grupo y además ser entregado en Moodle. Este informe incluirá:

*	Los resultados del análisis inicial, indicando la situación actual y dónde están los principales problemas de calidad.

*	Las acciones que se han decidido llevar a cabo para mejorar la calidad y el motivo razonado de su elección.

*	Los resultados del análisis final, indicando la situación actual la cuál ha de cumplir los criterios de calidad exigidos.

El informe indicará el autor del mismo y la historia de usuario a la que se refiere. Formará parte de la evaluación de la asignatura Calidad y Auditoría, correspondiendo a la parte de calidad de producto.
