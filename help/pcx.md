---
title: PCX
description: Página de ayuda de código de Pattern Detector
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 3%

---

# PCX {#pcx}

Complejidad de la página

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Complejidad de la página"
>abstract="PCX identifica las páginas que contienen un gran número de nodos en su estructura."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Cambios importantes: AEM como Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=es" text="AEM as a Cloud Service: Notas de la versión"

`PCX` identifica las páginas que contienen un gran número de nodos en su estructura.

Los subtipos se utilizan para identificar los diferentes tipos de información:

* `page.complexity.medium`: Una página contiene un número moderadamente alto de nodos que pueden afectar al rendimiento de la renderización.
* `page.complexity.high`: Una página contiene un número muy alto de nodos que probablemente afecten al rendimiento de la renderización.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Un gran número de nodos dentro de una página puede afectar al rendimiento de procesamiento.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar la estructura de contenido para reducir la complejidad de la página, lo que a su vez ayudaría a mejorar el rendimiento de la representación de páginas. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"

* Realice los pasos necesarios para reducir el número total de nodos dentro de una página, incluidos:
   * Compruebe que no hay contenedores innecesarios.
   * Compruebe si se puede lograr el mismo diseño con menos contenedores.
   * Simplifique el contenido de la página.
   * Reduzca la profundidad de la estructura del nodo.
   * Refactorice cualquier fragmento de experiencia incluido para simplificar.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
