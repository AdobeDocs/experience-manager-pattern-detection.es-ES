---
title: URC
description: Página de ayuda de código de Pattern Detector
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# URC {#urc}

Configuración de modo de ejecución no admitida

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configuración de modo de ejecución no admitida"
>abstract="URC identifica el uso de configuraciones que se basan en un nombre de modo de ejecución que no se admite en AEM como Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes" text="Modos de ejecución admitidos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#runmodes" text="Modos de ejecución"

`URC` identifica el uso de configuraciones que se basan en un nombre de modo de ejecución que no se admite en AEM como Cloud Service.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Directrices de implementación"
>abstract="La práctica recomendada es comprobar si todos los modos de ejecución utilizados en su aplicación son compatibles y asegurarse de que siguen las directrices de resolución del modo de ejecución"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#deploying" text="Directrices de resolución del modo de ejecución"

* El conjunto de nombres que se puede utilizar para modos de ejecución en AEM como Cloud Service es limitado.
* Las configuraciones basadas en nombres de modo de ejecución no compatibles no tendrán ningún efecto cuando se implementen en AEM como Cloud Service.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Herramientas y recursos"
>abstract="Revise el proyecto heredado de WKND para comprender cómo se pueden hacer compatibles las violaciones de URC con AEM Cloud Service. Además, revise el ejemplo de infracción de URC en Github para comprender cómo se pueden actualizar las configuraciones de OSGi basadas en modo de ejecución personalizado para adherirse a AEM como Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Proyecto WKND-Legacy"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Ejemplo de infracción de URC: Github"

* Revise el uso de esta configuración para determinar si es necesario.
* Cambie el nombre de la configuración para utilizar uno de los [nombres de modo de ejecución](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) admitidos y siga las [directrices de resolución de modo de ejecución](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution).
* Revise el proyecto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) y comprenda cómo se pueden corregir las [violaciones de URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) y hacerlas compatibles con AEM como Cloud Service.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
