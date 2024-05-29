---
title: OU
description: Página de ayuda de código del detector de patrones.
exl-id: 6ec96fab-dd6e-46af-864f-05dad387cbb6
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: ht
source-wordcount: '270'
ht-degree: 100%

---

# OU {#ou}

Uso obsoleto

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_overview"
>title="Uso obsoleto"
>abstract="OU identifica la situación en la que algunos nodos JCR, como componentes de Sling o de AEM o exportaciones OSGi de API, se cambian o eliminan de forma no compatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización. Pueden actualizarse a una versión no compatible o no estar disponibles."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Cambios importantes en AEM as a Cloud Service"

`OU` Identifica la situación en la que algunos nodos JCR, como componentes de Sling o de AEM o exportaciones OSGi de API, se cambian o eliminan de forma no compatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización. Pueden actualizarse a una versión no compatible o no estar disponibles.

Como las versiones anteriores no están instaladas de forma predeterminada, es posible que la aplicación del cliente no funcione correctamente.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La funcionalidad que depende de cualquier componente que utilice componentes o API obsoletos puede romperse y es posible que no se resuelva correctamente después de una actualización.
* Es posible que algunas características de la aplicación del cliente o algunas funciones de AEM no funcionen correctamente o que no estén activas después de una actualización.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar y adaptar el código del cliente para utilizar la versión más reciente de componentes de AEM o API. Póngase en contacto con la Asistencia de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API de SDK de Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* A corto plazo: la instalación de un paquete de compatibilidad podría resultar útil.
* A largo plazo: adapte el código de cliente para utilizar la versión más reciente de componentes de AEM o API.
* Póngase en contacto con el [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
