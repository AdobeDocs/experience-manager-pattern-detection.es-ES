---
title: OCU
description: Página de ayuda de código de Pattern Detector
exl-id: cb28c727-415d-436c-ab74-cf7f1f34f7c7
translation-type: tm+mt
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# OCU {#ocu}

Uso de código obsoleto

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_overview"
>title="Uso de código obsoleto"
>abstract="OCU identifica la situación en la que algunos nodos JCR, como Sling o componentes AEM o exportaciones OSGi de API, se cambian o eliminan de forma no compatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización. Pueden actualizarse a una versión incompatible o no estar disponibles."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Cambios importantes: AEM como Cloud Service"

`OCU` identifica la situación en la que algunos nodos JCR, como Sling o AEM componentes o las exportaciones de OSGi de API, se cambian o eliminan de forma incompatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización. Pueden actualizarse a una versión incompatible o no estar disponibles.

Como las versiones anteriores no están instaladas de forma predeterminada, es posible que la aplicación del cliente no funcione correctamente.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La funcionalidad que depende de cualquier componente que utilice componentes o API obsoletos puede romperse y es posible que no se resuelva correctamente después de una actualización.
* Es posible que algunas características de la aplicación del cliente o algunas funciones de AEM no funcionen correctamente o que no estén activas después de una actualización.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar y adaptar el código del cliente para utilizar la versión más reciente de AEM componentes o API. Póngase en contacto con el soporte de Adobe para obtener ayuda y aclaraciones."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API de SDK de Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"

* A corto plazo: La instalación del paquete de compatibilidad podría ayudar.
* A largo plazo: Adapte el código de cliente para utilizar la versión más reciente de AEM componentes o API.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
