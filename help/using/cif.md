---
title: CIF
description: Página de ayuda de código del detector de patrones.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 66%

---

# CIF {#cif}

Commerce Integration Framework clásico

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework clásico"
>abstract="CIF identifica la versión clásica del uso de Commerce Integration Framework que no es compatible con AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Content and Commerce"

`CIF`  Identifica la versión clásica del uso de Commerce integration framework AEM que es incompatible con el as a Cloud Service de la. El mensaje para cada `CIF` Esta búsqueda identifica el uso de y proporciona información adicional.

Los subtipos se utilizan para identificar los diferentes tipos de información:

* `commerce.integration.framework.detected`: una versión clásica de la incompatibilidad de Commerce Integration Framework con AEM as a Cloud Service.


## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar toda la versión clásica del uso de Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/content-and-commerce/changes" text="Cambios importantes en CIF"

* La versión clásica de Commerce Integration Framework ya no es compatible con AEM as a Cloud Service. Bloquearía la actualización a AEM as a Cloud Service.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Herramientas y recursos"
>abstract="Esta guía ayuda a identificar las áreas que se deben actualizar para la migración de Experience Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/content-and-commerce/migration" text="Guía de migración para CIF"

* Para Experience Manager as a Cloud Service CIF, el complemento de integración comercial es la única solución de integración comercial compatible para Adobe Commerce y soluciones de comercio de terceros. El complemento CIF se implementa automáticamente para los clientes de Experience Manager as a Cloud Service; no se necesita una implementación manual. Consulte [Introducción a AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started).
* CIF Para admitir la implementación de proyectos, el Adobe de proporciona lo siguiente: [AEM CIF Componentes principales de](https://github.com/adobe/aem-core-cif-components).
* CIF AEM El complemento también está disponible para la versión 6.5 de la versión en inglés, también a través de la versión de la versión de la aplicación de la versión en inglés. [Portal de distribución de software](https://experience.adobe.com/#/downloads/content/software-distribution/es/aem.html). Es compatible y proporciona las mismas características que el complemento CIF para Experience Manager as a Cloud Service: no se requieren ajustes.
* El CIF clásico con sus dependencias ya no está disponible. CIF CIF El código que se basa en esta versión de que utiliza las API Java™ de com.adobe.cq.commerce.api debe ajustarse al complemento de y a sus principios.
