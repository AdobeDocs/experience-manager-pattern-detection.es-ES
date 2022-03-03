---
title: DOPI
description: Página de ayuda de código del detector de patrones
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: ht
source-wordcount: '305'
ht-degree: 100%

---

# DOPI {#dopi}

Índice de propiedades ordenadas en desuso

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Índice de propiedades ordenadas en desuso"
>abstract="El código DOPI identifica el uso de definiciones de índice de propiedad ordenadas (primaryType=oak:QueryIndexDefinition AND type=&quot;ordered&quot;), que han quedado obsoletas desde la versión 6.1 y se eliminaron en la 6.2."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=es#the-ordered-index" text="Índice ordenado: obsoleto"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=es" text="Indexación: AEM as a Cloud Service"

`DOPI` identifica el uso de definiciones de índice de propiedad ordenadas (`primaryType=oak:QueryIndexDefinition` Y `type="ordered"`), que han quedado obsoletas desde la versión 6.1 y se han eliminado en la versión 6.2.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Directrices de implementación"
>abstract="La práctica recomendada es revisar todos los índices ordenados obsoletos y moverlos a la forma compatible de índices de Lucene para evitar problemas de rendimiento significativos o requisitos de cliente no funcionales."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/practices/best-practices-for-queries-and-indexing.html?lang=es" text="Prácticas recomendadas: consultas e indexación"

* Es posible que algunas consultas no respondan.
* Es posible que la funcionalidad del cliente no funcione correctamente.
* Puede haber advertencias transversales o incluso errores y sanciones de rendimiento significativas, ya que los índices obsoletos no tienen ningún efecto.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Herramientas y recursos"
>abstract="Revise el proyecto de WKND heredado para comprender cómo se pueden hacer compatibles las infracciones del DOPI con AEM Cloud Service. Además, revise el ejemplo de infracción de DOPI en Github para comprender cómo se pueden convertir los índices ordenados heredados a índices basados en Lucene compatibles con AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Proyecto de WKND heredado"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Ejemplo de infracción de DOPI: Github"

* Modifique la definición del índice para que se convierta en una definición de índice compatible, o sustitúyalo por ella. (Consulte [Consultas e indexación de Oak](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=es)).
* Consulte el proyecto de [WKND heredado](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) y comprenda cómo las [infracciones del DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) pueden corregirse y hacerse compatibles con AEM as a Cloud Service.
* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
