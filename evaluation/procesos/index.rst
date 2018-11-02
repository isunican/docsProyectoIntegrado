==================================================================================
 Normas y Criterios de Evaluación para la asignatura de Procesos de Ingeniería Sw
==================================================================================

La evaluación del trabajo en el proyecto integrado, en cuanto a la asignatura de Procesos de Ingeniería Software se refiere, comprende dos partes: un 50% corresponde al trabajo del grupo en su conjunto y el otro 50% refleja el esfuerzo personal de cada alumno.

El trabajo en pruebas del software en cada sprint comprende los planes de prueba ``P``, la implementación y ejecución de las pruebas ``E`` y el reporte final ``R``.
Estas tres actividades se realizarán para todas las historias de usuario implementadas y se evaluarán según los siguientes pesos ponderados ``P`` 40%, ``E`` 40% y ``R`` 20%. A lo largo del desarrollo de cada sprint el grupo puede pedir asesoría al profesor para mejorar su trabajo y al terminar recibirá indicadores cualitativos a considerar así como una calificación global. La calificación final será un indicador de la calidad del trabajo en los sprints y la evolución del grupo a lo largo del desarrollo del proyecto. Para la evaluación personal de cada alumno, al terminar todos los sprints cada uno deberá haberse hecho cargo de la especificación de al menos el plan de pruebas de una historia de usuario, así como la codificación y realización de al menos dos pruebas unitarias o bien de una unitaria y otra de integración o bien de una prueba de alguno de estos dos tipos y el reporte de pruebas de alguna de las historias de usuario.

``P`` Planes de Prueba
========================

Cada Historia de Usuario ha de contar con un Plan de Pruebas, el cual incluirá:

 #. La especificación de las pruebas de aceptación acordadas con el *Product Owner*.
 #. Los casos de prueba concretos que se derivan del mismo (etiquetados convenientemente).
 #. La especificación de las pruebas de integración (y de ser el caso el orden de realización de las mismas).
 #. La especificación de las pruebas unitarias para los componentes/módulos/clases/métodos involucrados. 
 #. Un breve texto que describa el cronograma de ejecución planificado.

Una versión inicial de este documento se valida con el profesor durante la primera semana de cada sprint. En ella, las pruebas unitarias pueden no estar totalmente definidas, pues puede no conocerse todavía la arquitectura a utilizar para implementar la historia de usuario. La versión final, con el plan de pruebas completo, se entrega al final de cada sprint. 

``E`` Implementación y ejecución de las pruebas
================================================

Cada grupo debe definir sus criterios para organizar el código correspondiente a las pruebas unitarias y de integración. Es importante que sean fácilmente identificables el/los caso/s de prueba que cada test implementa. Se exige que cada historia de usuario tenga codificados y ejecutados al menos dos casos de prueba para tests unitarios y uno para test de integración


``R`` Reporte de pruebas
=========================

Al terminar cada sprint se redactará un documento que recoja el reporte de pruebas de cada historia de usuario realizada, el cual describe la ejecución del plan de pruebas para la historia de usuario. Indicando los responsables (autores y/o ejecutores) de cada documento o artefacto, los fallos encontrados y las soluciones dadas a los mismos. Se entiende que este documento está complementado con el modelo arquitectónico (AppArchitecture.png) y eventualmente el del dominio (DomainModel.png) entregados en la carpeta Docs/Models, pues las pruebas se definen para las unidades funcionales (componentes/objectos/métodos) allí descritas.
