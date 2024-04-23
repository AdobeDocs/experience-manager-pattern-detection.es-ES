---
title: NCC
description: Página de ayuda de código de Pattern Detector.
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 65%

---

# NCC {#ncc}

Cambios no compatibles

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Cambios no compatibles"
>abstract="NCC identifica la situación en la que algunos nodos o paquetes JCR se cambian de una manera no compatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Cambios importantes en AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notas de la versión para AEM as a Cloud Service"

NCC identifica la situación en la que algunos nodos o paquetes JCR se cambian de una manera no compatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La funcionalidad que depende de cualquier componente que utilice cambios no compatibles puede romperse y es posible que no se resuelva correctamente.
* Es posible que algunas funciones de la aplicación del cliente o algunas funcionalidades de AEM no funcionen correctamente después de una actualización.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar el código personalizado y asegurarse de que solo se superponen o hacen referencia a los componentes de Sling compatibles. Póngase en contacto con el Soporte técnico de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Superposiciones"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Superponga o haga referencia únicamente a componentes de Sling compatibles.
* Considere la posibilidad de adaptar los recursos procedentes de `/libs` o paquetes después de una actualización AEM.
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclaraciones o para que se aborden las preocupaciones.
