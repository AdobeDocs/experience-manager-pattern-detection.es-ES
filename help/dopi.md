---
title: DOPI
description: Página de ayuda de código de Pattern Detector
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# DOPI {#dopi}

Índice de propiedades ordenadas en desuso

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Índice de propiedades ordenadas en desuso"
>abstract="El código DOPI identifica el uso de definiciones de índice de propiedad ordenadas (primaryType=oak:QueryIndexDefinition AND type=&quot;ordered&quot;), que han quedado obsoletas desde la versión 6.1 y se eliminaron en la versión 6.2."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=en#the-ordered-index" text="Índice ordenado - Obsoleto"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html" text="Indexación: AEM como Cloud Service"

`DOPI` identifica el uso de definiciones de índice de propiedad ordenadas (`primaryType=oak:QueryIndexDefinition` AND  `type="ordered"`), que han quedado obsoletas desde la versión 6.1 y se eliminaron en la versión 6.2.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Directrices de implementación"
>abstract="La práctica recomendada es revisar todos los índices ordenados obsoletos y moverlos a la forma compatible de índices de lucene para evitar problemas de rendimiento significativos o requisitos de cliente no funcionales."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/practices/best-practices-for-queries-and-indexing.html" text="Prácticas recomendadas: consultas e indexación"

* Es posible que algunas consultas no respondan.
* Es posible que la funcionalidad del cliente no funcione correctamente.
* Las advertencias transversales o incluso los errores y las sanciones de rendimiento significativas, ya que los índices obsoletos no tienen ningún efecto.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Herramientas y recursos"
>abstract="Revise el proyecto heredado de WKND para comprender cómo se pueden hacer compatibles las infracciones de DOPI con AEM Cloud Service. Además, revise el ejemplo de violación de DOPI en Github para comprender cómo se pueden convertir los índices ordenados heredados a índices basados en Lucene compatibles con AEM como Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Proyecto WKND-Legacy"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Ejemplo de violación de DOPI - Github"

* Modifique la definición del índice para que se convierta o reemplace el índice por una definición de índice admitida. (Consulte [Consultas e indexación de Oak](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html)).
* Revise el proyecto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) y comprenda cómo se pueden corregir las [violaciones del DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) y hacerlas compatibles con AEM como Cloud Service.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
