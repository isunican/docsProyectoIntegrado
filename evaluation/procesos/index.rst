==================================================================================
 Normas y Criterios de Evaluaci�n para la asignatura de Procesos de Ingenier�a Sw
==================================================================================

La evaluaci�n del trabajo en el proyecto integrado, en cuanto a la asignatura de Procesos de Ingenier�a Software se refiere, comprende dos partes: un 40% corresponde al trabajo del grupo en su conjunto y el otro 60% refleja el esfuerzo personal de cada alumno.

El trabajo en pruebas del software en cada sprint comprende los planes de prueba ``P`` y la implementaci�n y ejecuci�n de las pruebas ``E``.
Estas dos actividades se realizar�n para todas las historias de usuario implementadas y se evaluar�n seg�n los siguientes pesos ponderados ``P`` 40% y ``E`` 60%. 

A lo largo del desarrollo de cada sprint el grupo puede pedir asesor�a al profesor para mejorar su trabajo y al terminar recibir� indicadores cualitativos a considerar as� como una calificaci�n global. Esta calificaci�n final ser� un indicador de la calidad del trabajo en los sprints y la evoluci�n del grupo a lo largo del desarrollo del proyecto. 

Para la evaluaci�n personal de cada alumno, al terminar todos los sprints cada uno deber� haberse hecho cargo de, al menos:

* La especificaci�n del plan de pruebas de una historia de usuario.
* La codificaci�n y ejecuci�n de dos pruebas unitarias (o una unitaria y una de integraci�n).
* La codificaci�n y ejecuci�n de una prueba de interfaz de usuario (con Espresso).

Se podr� optar a mejorar la calificaci�n personal mediante la realizaci�n de m�s pruebas unitarias o de interfaz de usuario.

``P`` Planes de Prueba
========================

Cada Historia de Usuario ha de contar con un Plan de Pruebas, que incluir�:

 #. La especificaci�n de las pruebas de aceptaci�n acordadas con el *Product Owner*.
 #. Los casos de prueba concretos que se derivan del mismo (etiquetados convenientemente).
 #. La especificaci�n de las pruebas de interfaz de usuario.
 #. La especificaci�n de las pruebas de integraci�n (al menos dos).
 #. La especificaci�n de las pruebas unitarias definidas para las clases/m�todos involucrados (al menos dos). 
 #. Un breve texto que describa el cronograma de ejecuci�n planificado.
 #. Un reporte final que describa el resultado de la ejecuci�n de las pruebas para la historia de usuario, indicando los responsables (autores y/o ejecutores) de cada artefacto (si no son el mismo que el autor del plan de pruebas), los fallos encontrados y las soluciones dadas a los mismos. 

Este documento se complementa, y por tanto, debe ser totalmente coherente con los modelos arquitect�nico (AppArchitecture.png) y de dominio (DomainModel.png) entregados en la carpeta Docs/Models, pues las pruebas se definen para las unidades funcionales (componentes/clases/m�todos) all� descritas.

Una versi�n inicial de este documento se valida con el profesor durante la primera semana de cada sprint. En ella, las pruebas unitarias pueden no estar totalmente definidas, pues puede no conocerse todav�a la arquitectura a utilizar para implementar la historia de usuario. La versi�n final, con el plan de pruebas completo, se entrega al final de cada sprint. 

``E`` Implementaci�n y ejecuci�n de las pruebas
================================================

Es responsabilidad de cada grupo seguir los criterios indicados para la organizaci�n del c�digo correspondiente a pruebas, siendo muy importante que sean f�cilmente identificables el/los caso/s de prueba que cada test implementa.

Se exige que cada historia de usuario tenga codificados y ejecutados al menos dos tests unitarios y uno de interfaz de usuario.




