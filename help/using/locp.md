---
title: LOCP
description: Página de ayuda de código del detector de patrones.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 100%
---
# LOCP {#locp}

/libs Sobrescribir paquetes personalizados

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Sobrescribir paquetes personalizados"
>abstract="LOCP identifica la detección de un paquete personalizado que suministra contenido a `/libs`, que es un antipatrón (excepto si hay ACL)."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Actualizaciones sostenibles"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Combinación de recursos de Sling"

`LOCP` Identifica la detección de un paquete personalizado que envía contenido a `/libs`, que es un antipatrón (excepto en el caso de las ACL).

## Posibles implicaciones y riesgos {#implications-and-risks}

* El código de cliente puede eliminarse o reemplazarse para cualquier actualización importante de CFP, SP o AEM.
* En algunos casos, es posible que el nuevo contenido no esté instalado correctamente.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Directrices para la implementación"
>abstract="Los clientes deben revisar su código personalizado y los paquetes para identificar si el contenido se entrega a `/libs`. Si es necesario, refactorícelo para depender de la superposición del contenido en /apps y hacer que sea compatible con AEM as a Cloud Service. Póngase en contacto con la Asistencia de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Superposiciones"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Los paquetes de clientes deben implementar contenido en `/apps` en lugar de `/libs`.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
