---
title: PCX
description: Página de ayuda de código del detector de patrones
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 100%

---

# PCX {#pcx}

Complejidad de la página

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Complejidad de la página"
>abstract="PCX identifica las páginas que contienen un gran número de nodos en su estructura."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=es" text="Cambios importantes en AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=es" text="AEM as a Cloud Service: notas de la versión"

`PCX` identifica las páginas que contienen un gran número de nodos en su estructura.

Los subtipos se utilizan para identificar los diferentes tipos de información:

* `page.complexity.medium`: una página contiene un número moderadamente alto de nodos que pueden afectar al rendimiento del procesamiento.
* `page.complexity.high`: una página contiene un número muy alto de nodos que probablemente afecten al rendimiento del procesamiento.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Un gran número de nodos dentro de una página puede afectar al rendimiento de procesamiento.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar la estructura del contenido para reducir la complejidad de la página, lo que a su vez ayudaría a mejorar el rendimiento del procesamiento de páginas. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Realice los pasos necesarios para reducir el número total de nodos dentro de una página, incluyendo lo siguiente:
   * Compruebe que no hay contenedores innecesarios.
   * Compruebe si se puede lograr el mismo diseño con menos contenedores.
   * Simplifique el contenido de la página.
   * Reduzca la profundidad de la estructura del nodo.
   * Refactorice cualquier fragmento de experiencia incluido para simplificar.
* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
