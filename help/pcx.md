---
title: PCX
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# PCX {#pcx}

Complejidad de la página

## Fondo {#background}

`PCX` identifica las páginas que contienen un gran número de nodos en su estructura.

Los subtipos se utilizan para identificar los diferentes tipos de información:

* `page.complexity.medium`: Una página contiene un número moderadamente alto de nodos que pueden afectar al rendimiento de la renderización.
* `page.complexity.high`: Una página contiene un número muy alto de nodos que probablemente afecten al rendimiento de la renderización.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Un gran número de nodos dentro de una página puede afectar al rendimiento de procesamiento.

## Posibles soluciones {#solutions}

* Realice los pasos necesarios para reducir el número total de nodos dentro de una página, incluidos:
   * Compruebe que no hay contenedores innecesarios.
   * Compruebe si se puede lograr el mismo diseño con menos contenedores.
   * Simplifique el contenido de la página.
   * Reduzca la profundidad de la estructura del nodo.
   * Refactorice cualquier fragmento de experiencia incluido para simplificar.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
