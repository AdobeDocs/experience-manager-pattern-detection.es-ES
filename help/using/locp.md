---
title: LOCP
description: Página de ayuda de código de Pattern Detector.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 57%

---

# LOCP {#locp}

/libs Sobrescribir paquetes personalizados

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Sobrescribir paquetes personalizados"
>abstract="LOCP identifica la detección de un paquete personalizado que entrega contenido a /libs, que es un antipatrón (excepto en el caso de ACL)."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Actualizaciones sostenibles"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Fusión de recursos de Sling"

LOCP identifica la detección de un paquete personalizado que entrega contenido a `/libs`, que es un antipatrón (excepto en el caso de las ACL).

## Posibles implicaciones y riesgos {#implications-and-risks}

* AEM El código de cliente puede eliminarse o reemplazarse para cualquier actualización de CFP, SP o de la versión principal de los servicios de soporte técnico (CFP).
* En ocasiones, es posible que el nuevo contenido no esté instalado correctamente.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Directrices de implementación"
>abstract="Los clientes deben revisar su código personalizado y sus paquetes para identificar si el contenido se entrega a /libs y refactorizarlo para depender de la superposición del contenido en /apps y hacer que sea compatible con AEM as a Cloud Service. Póngase en contacto con el Soporte técnico de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Superposiciones"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Los paquetes de clientes deben implementar contenido en `/apps` en lugar de `/libs`.
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) si necesita aclaraciones o si tiene alguna duda.
