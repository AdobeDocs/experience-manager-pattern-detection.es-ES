---
title: CIF
description: Página de ayuda de código de Pattern Detector
source-git-commit: b611b595267e60df8a15511a8a2b4b30b601df1b
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 3%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifica la versión clásica del uso de Commerce Integration Framework que es incompatible con AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" Contenido y comercio"

`CIF` CIF identifica la versión clásica del uso de Commerce Integration Framework que es incompatible con AEM as a Cloud Service. El mensaje para cada `CIF` la búsqueda identificará el uso y proporcionará información adicional.

Los subtipos se utilizan para identificar los diferentes tipos de información:

* `commerce.integration.framework.detected`: Una versión clásica de la incompatibilidad de Commerce Integration Framework con AEM as a Cloud Service.


## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar toda la versión clásica del uso de Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="Cambios importantes en el CIF"

* La versión clásica de Commerce Integration Framework ya no es compatible con AEM as a Cloud Service. Bloquearía la actualización a AEM as a Cloud Service.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Herramientas y recursos"
>abstract="Esta guía ayuda a identificar las áreas que debe actualizar para la migración de Experience Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="Guía de migración para CIF"

* Para el Experience Manager as a Cloud Service, el complemento CIF es la única solución de integración comercial compatible para Adobe Commerce y soluciones de comercio de terceros. El complemento CIF se implementa automáticamente para los clientes as a Cloud Service por el Experience Manager; no se necesita una implementación manual. Consulte [Introducción a AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html).
* Para apoyar proyectos que implementen el Adobe CIF proporciona [Componentes principales del CIF de AEM](https://github.com/adobe/aem-core-cif-components).
* El complemento CIF también está disponible para AEM 6.5 a través del [Portal de distribución de software](https://experience.adobe.com/#/downloads/content/software-distribution/es/aem.html). Es compatible y proporciona las mismas características que el complemento CIF para Experience Manager as a Cloud Service: no se requieren ajustes.
* El CIF clásico con sus dependencias ya no está disponible. El código que se basa en esta versión del CIF que utiliza las API Java de com.adobe.cq.commerce.api debe ajustarse al complemento CIF y a sus principios.
