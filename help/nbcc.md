---
title: NBCC
description: Página de ayuda de código de Pattern Detector
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 3%

---

# NBCC {#nbcc}

Cambios no compatibles con versiones anteriores

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Cambios no compatibles con versiones anteriores"
>abstract="NBCC identifica la situación en la que algunos nodos o paquetes JCR se cambian de una manera no compatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Cambios importantes: AEM como Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=es" text="Notas de la versión: AEM como Cloud Service"

`NBCC` identifica la situación en la que algunos nodos o paquetes JCR se cambian de una manera no compatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La funcionalidad que depende de cualquier componente que utilice cambios no compatibles con versiones anteriores puede romperse y es posible que no se resuelva correctamente.
* Es posible que algunas funciones de la aplicación del cliente o algunas AEM no funcionen correctamente después de una actualización.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar el código personalizado y asegurarse de que solo se superponen o hacen referencia a los componentes de Sling compatibles con versiones anteriores. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Superposiciones"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"

* Superponga o haga referencia únicamente a componentes Sling compatibles con versiones anteriores.
* Considere la posibilidad de adaptar los recursos procedentes de `/libs` o paquetes después de una actualización AEM.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
