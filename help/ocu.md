---
title: OCU
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# OCU {#ocu}

Uso de código obsoleto

## Fondo {#background}

`OCU` identifica la situación en la que algunos nodos JCR, como Sling o AEM componentes o las exportaciones de OSGi de API, se cambian o eliminan de forma incompatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización. Pueden actualizarse a una versión incompatible o no estar disponibles.

Como las versiones anteriores no están instaladas de forma predeterminada, es posible que la aplicación del cliente no funcione correctamente.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La funcionalidad que depende de cualquier componente que utilice componentes o API obsoletos puede romperse y es posible que no se resuelva correctamente después de una actualización.
* Es posible que algunas características de la aplicación del cliente o algunas funciones de AEM no funcionen correctamente o que no estén activas después de una actualización.

## Posibles soluciones {#solutions}

* A corto plazo: La instalación del paquete de compatibilidad podría ayudar.
* A largo plazo: Adapte el código de cliente para utilizar la versión más reciente de AEM componentes o API.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
