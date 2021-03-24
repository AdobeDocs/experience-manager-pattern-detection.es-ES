---
title: NBCC
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# NBCC {#nbcc}

Cambios no compatibles con versiones anteriores

## Fondo {#background}

`NBCC` identifica la situación en la que algunos nodos o paquetes JCR se cambian de una manera no compatible. Es posible que el cliente no esté al tanto de este cambio antes de una actualización.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La funcionalidad que depende de cualquier componente que utilice cambios no compatibles con versiones anteriores puede romperse y es posible que no se resuelva correctamente.
* Es posible que algunas funciones de la aplicación del cliente o algunas AEM no funcionen correctamente después de una actualización.

## Posibles soluciones {#solutions}

* Superponga o haga referencia únicamente a componentes Sling compatibles con versiones anteriores.
* Considere la posibilidad de adaptar los recursos procedentes de `/libs` o paquetes después de una actualización AEM.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
