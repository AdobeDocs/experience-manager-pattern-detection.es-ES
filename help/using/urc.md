---
title: URC
description: Página de ayuda de código del detector de patrones
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '319'
ht-degree: 100%

---

# URC {#urc}

Configuración de modo de ejecución no admitida

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configuración de modo de ejecución no admitida"
>abstract="URC identifica el uso de configuraciones que se basan en un nombre de modo de ejecución no admitido en AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=es#custom-runmodes" text="Modos de ejecución admitidos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=es#runmodes" text="Modos de ejecución"

`URC` identifica el uso de configuraciones que se basan en un nombre de modo de ejecución no admitido en AEM as a Cloud Service.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Directrices de implementación"
>abstract="La práctica recomendada es comprobar si todos los modos de ejecución utilizados en su aplicación son compatibles y asegurarse de que siguen las directrices de resolución del modo de ejecución."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=es#deploying" text="Directrices de resolución del modo de ejecución"

* El conjunto de nombres que se puede utilizar para los modos de ejecución en AEM as a Cloud Service es limitado.
* Las configuraciones basadas en nombres de modo de ejecución no compatibles no tendrán ningún efecto cuando se implementen en AEM as a Cloud Service.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Herramientas y recursos"
>abstract="Revise el proyecto de WKND heredado para comprender cómo se pueden hacer compatibles las violaciones de URC con AEM Cloud Service. Además, revise el ejemplo de infracción de URC en Github para comprender cómo se pueden actualizar las configuraciones de OSGi basadas en un modo de ejecución personalizado para adherirse a AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Proyecto de WKND heredado"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Ejemplo de infracción de URC: Github"

* Revise el uso de esta configuración para determinar si es necesario.
* Cambie el nombre de la configuración para utilizar una de los [nombres de modo de ejecución](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=es#custom-runmodes) admitidos y siga las [directrices de resolución del modo de ejecución](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=es#runmode-resolution).
* Consulte el proyecto de [WKND heredado](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) y comprenda cómo las [infracciones de URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) pueden corregirse y hacerse compatibles con AEM as a Cloud Service.
* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
