---
title: LOCP
description: Página de ayuda de código de Pattern Detector
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# LOCP {#locp}

/libs Sobrescribir paquetes personalizados

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Sobrescribir paquetes personalizados"
>abstract="LOCP identifica la detección de un paquete personalizado que entrega contenido a /libs, que es un anti-patrón (excepto en el caso de ACL)."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html" text="Actualizaciones sostenibles"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Fusión de recursos de Sling"

`LOCP` identifica la detección de un paquete personalizado que envía contenido a  `/libs`, que es un anti-patrón (excepto en el caso de las ACL).

## Posibles implicaciones y riesgos {#implications-and-risks}

* El código de cliente puede eliminarse o reemplazarse para cualquier actualización de CFP, SP o AEM principal.
* En algunos casos, es posible que el nuevo contenido no esté instalado correctamente.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Directrices de implementación"
>abstract="Los clientes deben revisar su código personalizado y sus paquetes para identificar si el contenido se entrega a /libs y refactorizarlo para depender de la superposición del contenido en /apps y hacerlo compatible con AEM como Cloud Service. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Superposiciones"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"

* Los paquetes de clientes deben implementar contenido en `/apps` en lugar de en `/libs`.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
