---
title: DOPI
description: Página de ayuda de código del detector de patrones.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 100%
---
# DOPI {#dopi}

Índice de propiedades ordenadas en desuso

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Índice de propiedades ordenadas en desuso"
>abstract="El código DOPI identifica el uso de definiciones de índice de propiedades ordenadas (`primaryType=oak:QueryIndexDefinition` Y `type="ordered"`). La definición quedó obsoleta en AEM 6.1 y se eliminó en AEM 6.2."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="Índice ordenado: obsoleto"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/operations/indexing" text="Indexación: AEM as a Cloud Service"

`DOPI`  Identifica el uso de definiciones de índice de propiedades ordenadas (`primaryType=oak:QueryIndexDefinition` Y `type="ordered"`). Las definiciones quedaron obsoletas en AEM 6.1 y se eliminaron en AEM 6.2.

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
>abstract="Revise el proyecto de WKND heredado para comprender cómo se pueden hacer compatibles las infracciones del DOPI con AEM Cloud Service. Además, revise el ejemplo de infracción de DOPI en GitHub. Puede ayudarle a comprender cómo se pueden convertir los índices ordenados heredados a índices basados en Lucene compatibles con AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Proyecto de WKND heredado"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Ejemplo de infracción de DOPI: GitHub"

* Edite la definición de índice para que se convierta (o reemplace el índice por) una definición de índice compatible. (Consulte [Consultas e indexación de Oak](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing)).
* Consulte el proyecto de [WKND heredado](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) y comprenda cómo las [infracciones del DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) pueden corregirse y hacerse compatibles con AEM as a Cloud Service.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
