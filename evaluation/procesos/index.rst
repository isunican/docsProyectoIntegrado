=======================================================================================
 Normas y Criterios de Evaluación para la asignatura de Procesos de Ingeniería Software
=======================================================================================

La evaluación del trabajo en el proyecto integrado, en cuanto a la asignatura de Procesos de Ingeniería Software se refiere, comprende dos partes: un 40% corresponde al trabajo del grupo en su conjunto y el otro 60% refleja el esfuerzo personal de cada alumno.

El trabajo en pruebas del software en cada sprint comprende los planes de prueba y la implementación y ejecución de las pruebas.
Estas dos actividades se realizarán para todas las historias de usuario implementadas y se evaluarán según los siguientes pesos ponderados: plan de pruebas 40% e implementación y ejecución de las pruebas 60%. 

A lo largo del desarrollo de cada sprint el grupo puede pedir asesoría al profesor para mejorar su trabajo y al terminar recibirá indicadores cualitativos a considerar así como una calificación global. Esta calificación final será un indicador de la calidad del trabajo en los sprints y la evolución del grupo a lo largo del desarrollo del proyecto. 

Para la evaluación personal de cada alumno, al terminar todos los sprints cada uno deberá haberse hecho cargo de, al menos:

* La especificación del plan de pruebas de una historia de usuario.
* La codificación y ejecución de dos pruebas unitarias (o una unitaria y una de integración).
* La codificación y ejecución de una prueba de interfaz de usuario (con Espresso).

Se podrá optar a mejorar la calificación personal mediante la realización de más pruebas unitarias o de interfaz de usuario.

Planes de Prueba
================

Cada Historia de Usuario ha de contar con un Plan de Pruebas, que incluirá:

 #. La especificación de las pruebas de aceptación acordadas con el *Product Owner*.
 #. Los casos de prueba concretos que se derivan del mismo (etiquetados convenientemente).
 #. La especificación de las pruebas de interfaz de usuario.
 #. La especificación de las pruebas unitarias definidas para las clases/métodos involucrados (al menos dos). 
 #. Un reporte final que describa el resultado de la ejecución de las pruebas para la historia de usuario, indicando los responsables (autores y/o ejecutores) de cada artefacto (si no son el mismo que el autor del plan de pruebas) y el número de fallos encontrados por cada prueba. 

Este documento se complementa, y por tanto, debe ser totalmente coherente con los modelos arquitectónico (AppArchitecture.png) y de dominio (DomainModel.png) entregados en la carpeta Docs/Models, pues las pruebas se definen para las unidades funcionales (componentes/clases/métodos) allí descritas.

Una versión inicial de este documento se valida con el profesor durante la primera semana de cada sprint. En ella, las pruebas unitarias pueden no estar totalmente definidas, pues puede no conocerse todavía la arquitectura a utilizar para implementar la historia de usuario. La versión final, con el plan de pruebas completo, se entrega al final de cada sprint. 

Implementación y ejecución de las pruebas
==========================================

Es responsabilidad de cada grupo seguir los criterios indicados para la organización del código correspondiente a pruebas, siendo muy importante que sean fácilmente identificables el/los caso/s de prueba que cada test implementa.

Se exige que cada historia de usuario tenga codificados y ejecutados al menos dos tests unitarios y uno de interfaz de usuario.




