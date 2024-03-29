﻿=======================================================================================
 Normas de Evaluación para Procesos de Ingeniería Software
=======================================================================================

Procedimiento de Evaluación
===========================

La calificación del proyecto integrado en la asignatura de Procesos de Ingeniería Software se calcula del siguiente modo:

* Un 20% corresponde al trabajo del grupo en su conjunto. En este apartado se valoran cuatro aspectos: 

  - La completitud de las historias de usuario seleccionadas para el Sprint desde el punto de vista de las pruebas (ver `Planes de Prueba`_).
  
  - La organización y nomenclatura de las clases de prueba dentro del proyecto Android.

  - La coherencia del modelo de diseño (MagicDraw) con el código y con el plan de pruebas.

  - La validación del plan de pruebas con el profesor durante la primera semana del Sprint (ver `Planes de Prueba`_).


* Un 80% refleja el esfuerzo personal de cada alumno. Para la evaluación personal, al terminar el proyecto cada alumno deberá haberse hecho cargo de, al menos:
  
  - La especificación del plan de pruebas de UNA historia de usuario.

  - La codificación y ejecución de DOS pruebas unitarias, o UNA unitaria y UNA de integración (incluso del mismo método). En las pruebas unitarias, al menos una, debería incluir el uso de Mocks.

  - La codificación y ejecución de una prueba de interfaz de usuario utilizando Espresso.

A lo largo del desarrollo de cada sprint el grupo puede pedir asesoría al profesor para mejorar su trabajo y al terminar recibirá indicadores cualitativos a considerar así como una calificación global. Esta calificación final será un indicador de la calidad del trabajo en los sprints y la evolución del grupo a lo largo del desarrollo del proyecto. 


Planes de Prueba
================

Cada historia de usuario ha de contar con un plan de pruebas, que incluirá:

 #. La especificación de las pruebas de aceptación acordadas con el *Product Owner*.
 #. La especificación de las pruebas de interfaz de usuario.
 #. La enumeración de aquellos métodos que sean susceptibles de prueba unitaria (o de integración) a consecuencia de la implementación de la historia de usuario, bien por ser nuevos o por ser necesario modificar su comportamiento.
 #. De los métodos enumerados en el apartado anterior, la especificación de los casos de prueba unitarios o de integración de DOS métodos (no puede ser la misma prueba a nivel unitaria y de integración, pues los casos de prueba serían los mismos).
 #. Un reporte final que describa el resultado de la ejecución de las pruebas para la historia de usuario, indicando los responsables (autores y/o ejecutores) de cada artefacto (si no son el mismo que el autor del plan de pruebas) y una pequeña explicación de los fallos detectados gracias a la prueba. 

Este documento se complementa, y por tanto, debe ser totalmente coherente con el modelo de diseño disponible en la carpeta Docs/Models, pues las pruebas se definen para las unidades funcionales (componentes/clases/métodos) allí descritas.

Una versión inicial de este documento, junto con el modelo de arquitectura, deberá validarse con el profesor durante la primera semana de cada sprint. En ella, las pruebas unitarias y/o de integración pueden no estar totalmente definidas, pues puede no conocerse todavía la arquitectura a utilizar para implementar la historia de usuario. La versión final, con el plan de pruebas completo, se entrega al final de cada sprint. 


Implementación y ejecución de las pruebas
==========================================

Es responsabilidad de cada grupo seguir los criterios indicados para la organización del código correspondiente a pruebas, siendo muy importante que sean fácilmente identificables el/los caso/s de prueba que cada test implementa.

Se exige que cada historia de usuario tenga codificados y ejecutados al menos dos tests unitarios o de integración y uno de interfaz de usuario.

Mecanismo para mejorar la calificación individual obtenida en un sprint
=======================================================================

Para mejorar la calificación individual obtenida en un sprint existen dos opciones:

* La opción prioritaria consiste en encargarse en otro sprint, y por tanto en otra historia de usuario, de las tareas que hayan obtenido una mala calificación. Es decir, si en un sprint se tiene mala nota en una prueba unitaria, en el siguiente sprint esa persona volvería a encargarse de realizar pruebas unitarias, que serían obviamente distintas, aunque podría darse el caso de volver a encargarse de la mismas pruebas si en la nueva historia de usuario se usa también el mismo código.
* Si no hubiese suficientes historias de usuario para hacer esto (será lo habitual), la segunda opción consiste en solucionar los problemas detectados en las tareas con baja calificación. Esta opción debería llevarse a cabo sin contar como esfuerzo de los siguientes sprints. Para ello, el modo de proceder será el siguiente:

  - Crear un nuevo elemento en el Backlog de tipo "Technical" denominado, por ejemplo, "Mejora pruebas unitarias historia XXX" con effort 0 y business value alto, de manera que sea elegible en el siguiente sprint.
  - Su implementación se llevará a cabo en la feature branch correspondiente a la historia de usuario a la que pertenecían las pruebas a mejorar (será una historia de usuario de un sprint anterior).
  - Esa rama, una vez resueltos los errores, se fusionará con la rama develop en el sprint actual.




