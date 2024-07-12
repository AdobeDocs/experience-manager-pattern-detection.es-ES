---
title: NBCC
description: Página de ayuda de código del detector de patrones.
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 100%

---

# NBCC {#nbcc}

OBSOLETO: cambios no compatibles con versiones anteriores (reemplazados por NCC, cambios no compatibles)

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Cambios no compatibles con versiones anteriores"
>abstract="NBCC identifica la situación en la que algunos nodos o paquetes de JCR se cambian de una manera no compatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización. "
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Cambios importantes en AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notas de la versión: AEM as a Cloud Service"

`NBCC` Identifica la situación en la que algunos nodos o paquetes JCR se cambian de una manera no compatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización. 

## Posibles implicaciones y riesgos {#implications-and-risks}

* La funcionalidad que depende de cualquier componente que utilice cambios no compatibles con versiones anteriores puede romperse y es posible que no se resuelva correctamente.
* Es posible que algunas funciones de la aplicación del cliente o algunas funcionalidades de AEM no funcionen correctamente después de una actualización.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada consiste en revisar el código personalizado y asegurarse de que solo los componentes de Sling compatibles con versiones anteriores se superponen o se hace referencia a ellos. Póngase en contacto con la Asistencia de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Superposiciones"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Superponga o haga referencia únicamente a componentes de Sling compatibles.
* Considere la posibilidad de adaptar los recursos procedentes de `/libs` o paquetes después de una actualización de AEM.
* Póngase en contacto con el [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
