---
title: URC
description: Página de ayuda de código del detector de patrones.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 100%

---

# URC {#urc}

Configuración del modo de ejecución no compatible

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configuración del modo de ejecución no compatible"
>abstract="URC identifica el uso de configuraciones que se basan en un nombre de modo de ejecución no admitido en AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Modos de ejecución admitidos"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Modos de ejecución"

`URC` Identifica el uso de configuraciones que se basan en un nombre de modo de ejecución no admitido en AEM as a Cloud Service.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar si se admiten todos los modos de ejecución utilizados en la aplicación. Asegúrese de que se siguen las directrices de resolución del modo de ejecución"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Directrices de resolución del modo de ejecución"

* El conjunto de nombres que se puede utilizar para ejecutar varios modos de ejecución en AEM as a Cloud Service es limitado.
* Las configuraciones que se basan en nombres de modo de ejecución no compatibles no tienen ningún efecto cuando se implementan en AEM as a Cloud Service.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Herramientas y recursos"
>abstract="Revise el proyecto de WKND heredado para comprender cómo se pueden hacer compatibles las violaciones de URC con AEM Cloud Service. Además, revise el ejemplo de infracción de URC en GitHub para conocer cómo se pueden actualizar las configuraciones de OSGi basadas en un modo de ejecución personalizado para adherirse a AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Proyecto de WKND heredado"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Ejemplo de infracción de URC: GitHub"

* Revise el uso de esta configuración para que pueda determinar si es necesaria.
* Cambie el nombre de la configuración utilizando uno de los [nombres de modo de ejecución](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) compatibles y siga las [pautas de resolución del modo de ejecución](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Revise el proyecto de [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) y comprenda cómo las [infracciones de URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) pueden corregirse y hacerse compatibles con AEM as a Cloud Service.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
