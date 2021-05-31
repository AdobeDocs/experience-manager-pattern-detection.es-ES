---
title: CIF
description: Página de ayuda de código de Pattern Detector
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 84aea5b24e51ce5672826bad4ec126074bf24a09
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifica la versión clásica del uso de Commerce Integration Framework que es incompatible con AEM como Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" Contenido y comercio"

`CIF` CIF identifica la versión clásica del uso de Commerce Integration Framework que es incompatible con AEM como Cloud Service. El mensaje para cada búsqueda `CIF` identificará el uso y proporcionará información adicional.

Los subtipos se utilizan para identificar los diferentes tipos de información:

* `commerce.integration.framework.detected`: Versión clásica de la incompatibilidad de Commerce Integration Framework con AEM como Cloud Service.


## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar toda la versión clásica del uso de Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="Cambios importantes en el CIF"

* La versión clásica de Commerce Integration Framework ya no es compatible con AEM como Cloud Service. Bloquearía la actualización a AEM como Cloud Service.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Herramientas y recursos"
>abstract="Esta guía ayuda a identificar las áreas que debe actualizar para la migración de Experience Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="Guía de migración para CIF"

* Para Experience Manager como Cloud Service, el complemento CIF es la única solución de integración comercial compatible para soluciones de comercio de Adobe y de terceros. El complemento CIF se implementa automáticamente para los clientes en Experience Manager como Cloud Service; no se necesita una implementación manual. Consulte [Introducción a AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html).
* Para admitir proyectos que implementen el Adobe CIF, proporciona [AEM componentes principales del CIF](https://github.com/adobe/aem-core-cif-components).
* El complemento CIF también está disponible para AEM 6.5 a través del [Portal de distribución de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). Es compatible y proporciona las mismas características que el complemento CIF para Experience Manager como Cloud Service: no se requieren ajustes.
* El CIF clásico con sus dependencias ya no está disponible. El código que se basa en esta versión del CIF que utiliza las API Java de com.adobe.cq.commerce.api debe ajustarse al complemento CIF y a sus principios.
