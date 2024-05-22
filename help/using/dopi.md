---
title: DOPI
description: Página de ayuda de código del detector de patrones.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 69%

---

# DOPI {#dopi}

Índice de propiedades ordenadas en desuso

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Índice de propiedades ordenadas en desuso"
>abstract="El código DOPI identifica el uso de definiciones de índice de propiedades ordenadas (`primaryType=oak:QueryIndexDefinition` Y `type="ordered"`). AEM AEM La definición quedó obsoleta en la versión 6.1 del y se eliminó en la versión 6.2."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="Índice ordenado: obsoleto"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/operations/indexing" text="Indexación: AEM as a Cloud Service"

`DOPI`  Identifica el uso de definiciones de índice de propiedades ordenadas (`primaryType=oak:QueryIndexDefinition` Y `type="ordered"`). AEM AEM Las definiciones quedaron obsoletas en la versión 6.1 del y se eliminaron en la versión 6.2.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Directrices de implementación"
>abstract="La práctica recomendada consiste en revisar todos los índices ordenados obsoletos y moverlos a la forma compatible de índices de Lucene para evitar problemas de rendimiento significativos o requisitos de cliente no funcionales."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/practices/best-practices-for-queries-and-indexing" text="Prácticas recomendadas: consultas e indexación"

* Es posible que algunas consultas no respondan.
* Es posible que la funcionalidad del cliente no funcione correctamente.
* Puede haber advertencias transversales o incluso errores y sanciones de rendimiento significativas, ya que los índices obsoletos no tienen ningún efecto.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Herramientas y recursos"
>abstract="Revise el proyecto de WKND heredado para comprender cómo se pueden hacer compatibles las infracciones del DOPI con AEM Cloud Service. Además, revise el ejemplo de infracción de DOPI en GitHub. AEM Puede ayudarle a comprender cómo se pueden convertir los índices ordenados heredados a índices basados en Lucene compatibles con el as a Cloud Service de la."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Proyecto de WKND heredado"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Ejemplo de infracción de DOPI: GitHub"

* Edite la definición de índice para que se convierta (o reemplace el índice por) una definición de índice compatible. (Consulte [Consultas e indexación de Oak](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing)).
* Consulte el proyecto de [WKND heredado](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) y comprenda cómo las [infracciones del DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) pueden corregirse y hacerse compatibles con AEM as a Cloud Service.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
