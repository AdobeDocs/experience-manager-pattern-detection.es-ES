---
title: URC
description: Página de ayuda de código de Pattern Detector.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 24%

---

# URC {#urc}

Configuración del modo de ejecución no admitida

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configuración de modo de ejecución no admitida"
>abstract="AEM URC identifica el uso de configuraciones que se basan en un nombre de modo de ejecución no admitido en el modo de ejecución de as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Modos de ejecución admitidos"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Modos de ejecución"

AEM URC identifica el uso de configuraciones que se basan en un nombre de modo de ejecución no admitido en el modo de ejecución de as a Cloud Service.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es comprobar si todos los modos de ejecución utilizados en la aplicación son compatibles y asegurarse de que siguen las directrices de resolución del modo de ejecución"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Directrices de resolución del modo de ejecución"

* AEM El conjunto de nombres que se puede utilizar para ejecutar varios modos en el as a Cloud Service de la es limitado.
* AEM Las configuraciones basadas en nombres de modo de ejecución no admitidos no tienen ningún efecto cuando se implementan en el modo de ejecución as a Cloud Service de la.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Herramientas y recursos"
>abstract="Revise el proyecto de WKND heredado para comprender cómo se pueden hacer compatibles las violaciones de URC con AEM Cloud Service. AEM Además, revise el ejemplo de infracción de URC en GitHub para comprender cómo se pueden actualizar las configuraciones de OSGi basadas en un modo de ejecución personalizado para adherirse a las normas as a Cloud Service de la."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Proyecto de WKND heredado"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Ejemplo de infracción de URC: GitHub"

* Revise el uso de esta configuración para poder determinar si es necesario.
* Cambie el nombre de la configuración mediante uno de los [nombres del modo de ejecución](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) y seguir [directrices de resolución del modo de ejecución](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Consulte el proyecto de [WKND heredado](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) y comprenda cómo las [infracciones de URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) pueden corregirse y hacerse compatibles con AEM as a Cloud Service.
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclaraciones o para que se aborden las preocupaciones.
