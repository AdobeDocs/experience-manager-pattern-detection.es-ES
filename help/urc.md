---
title: URC
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# URC {#urc}

Configuración de modo de ejecución no admitida

## Fondo {#background}

`URC` identifica el uso de configuraciones que se basan en un nombre de modo de ejecución que no se admite en AEM como Cloud Service.

## Posibles implicaciones y riesgos {#implications-and-risks}

* El conjunto de nombres que se puede utilizar para modos de ejecución en AEM como Cloud Service es limitado.
* Las configuraciones basadas en nombres de modo de ejecución no compatibles no tendrán ningún efecto cuando se implementen en AEM como Cloud Service.

## Posibles soluciones {#solutions}

* Revise el uso de esta configuración para determinar si es necesario.
* Cambie el nombre de la configuración para utilizar uno de los [nombres de modo de ejecución](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) admitidos y siga las [directrices de resolución de modo de ejecución](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution).
* Revise el proyecto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) y comprenda cómo se pueden corregir las [violaciones de URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) y hacerlas compatibles con AEM como Cloud Service.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
