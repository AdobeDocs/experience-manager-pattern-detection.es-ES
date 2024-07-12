---
title: PCX
description: Página de ayuda de código del detector de patrones.
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 100%

---

# PCX {#pcx}

Complejidad de la página

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Complejidad de la página"
>abstract="PCX identifica las páginas que contienen un gran número de nodos en su estructura."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Cambios importantes en AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service: Notas de la versión"

`PCX` Identifica las páginas que contienen muchos nodos en su estructura.

Los subtipos se utilizan para identificar los diferentes tipos de información:

* `page.complexity.medium`: una página contiene un número moderadamente alto de nodos que pueden afectar al rendimiento del procesamiento.
* `page.complexity.high`: una página contiene un número muy alto de nodos que probablemente afecten al rendimiento del procesamiento.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Muchos nodos dentro de una página pueden afectar al rendimiento del procesamiento.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar la estructura de contenido para reducir la complejidad de la página. A su vez, puede ayudar a mejorar el rendimiento de procesamiento de la página. Póngase en contacto con la Asistencia de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Reduzca el número total de nodos dentro de una página realizando la siguiente acción:
   * Compruebe que no hay contenedores innecesarios.
   * Compruebe si se puede lograr el mismo diseño con menos contenedores.
   * Simplifique el contenido de la página.
   * Reduzca la profundidad de la estructura del nodo.
   * Refactorice cualquier fragmento de experiencia incluido para simplificar.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
