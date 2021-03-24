---
title: LOCP
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---


# LOCP {#locp}

/libs Sobrescribir paquetes personalizados

## Fondo {#background}

`LOCP` identifica la detección de un paquete personalizado que envía contenido a  `/libs`, que es un anti-patrón (excepto en el caso de las ACL).

## Posibles implicaciones y riesgos {#implications-and-risks}

* El código de cliente puede eliminarse o reemplazarse para cualquier actualización de CFP, SP o AEM principal.
* En algunos casos, es posible que el nuevo contenido no esté instalado correctamente.

## Posibles soluciones {#solutions}

* Los paquetes de clientes deben implementar contenido en `/apps` en lugar de en `/libs`.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
