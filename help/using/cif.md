---
title: CIF
description: Página de ayuda de código del detector de patrones.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 76%

---

# CIF {#cif}

Commerce Integration Framework clásico

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework clásico"
>abstract="CIF identifica la versión clásica del uso de Commerce Integration Framework que no es compatible con AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Content and Commerce"

`CIF` Identifica la versión clásica del uso de Commerce Integration Framework que no es compatible con AEM as a Cloud Service. El mensaje para cada hallazgo de `CIF` identifica el uso y proporciona información adicional.

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

* Para Experience Manager as a Cloud Service, el complemento CIF es la única solución de integración comercial compatible para Adobe Commerce y soluciones de comercio de terceros. El complemento CIF se implementa automáticamente para los clientes de Experience Manager as a Cloud Service; no se necesita una implementación manual. Consulte [Introducción a AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started).
* Para apoyar proyectos que implementen CIF, Adobe proporciona [Componentes principales del CIF de AEM](https://github.com/adobe/aem-core-cif-components).
* El complemento CIF también está disponible para AEM 6.5 a través del [Portal de distribución de software](https://experience.adobe.com/#/downloads/content/software-distribution/es/aem.html). Es compatible y proporciona las mismas características que el complemento CIF para Experience Manager as a Cloud Service: no se requieren ajustes.
* El CIF clásico con sus dependencias ya no está disponible. El código que se basa en esta versión del CIF que utiliza las API Java™ de com.adobe.cq.commerce.api debe ajustarse al complemento CIF y a sus principios.

Además, a continuación encontrará las posibles soluciones para los diferentes subtipos:

* `commerce.bundles.detected`: estos paquetes se desinstalarán durante la actualización
* `commerce.packages.detected`: estos paquetes se eliminarán durante la actualización
* `commerce.packages.dependency`: elimine cualquier dependencia de Commerce de los paquetes personalizados
* `commerce.nodes.detected`: actualice el código personalizado para no crear nodos de CQ Commerce
* `commerce.configs.detected`: no utilice las propiedades de configuración de CQ Commerce en el código personalizado
* `commerce.users.detected` - No usar usuarios del servicio CQ Commerce en código personalizado
* `commerce.overlays.detected` - Quitar el uso de superposiciones de CQ Commerce
* `commerce.paths.detected`: elimine las rutas de comercio después de asegurarse de que no se están utilizando en AEM
* `commerce.resource.type.detected` - Quitar uso de tipo de recurso de comercio
* `commerce.usage`: elimine las API de CQ Commerce en su código personalizado.
