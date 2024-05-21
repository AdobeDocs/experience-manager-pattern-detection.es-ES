---
title: LOCP
description: Página de ayuda de código del detector de patrones.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 65%

---

# LOCP {#locp}

/libs Sobrescribir paquetes personalizados

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Sobrescribir paquetes personalizados"
>abstract="LOCP identifica la detección de un paquete personalizado que entrega contenido a `/libs`, que es un antipatrón (excepto si hay ACL)."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Actualizaciones sostenibles"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Fusión de recursos de Sling"

`LOCP` Identifica la detección de un paquete personalizado que envía contenido a `/libs`, que es un antipatrón (excepto en el caso de las ACL).

## Posibles implicaciones y riesgos {#implications-and-risks}

* El código de cliente puede eliminarse o reemplazarse para cualquier actualización importante de CFP, SP o AEM.
* En algunos casos, es posible que el nuevo contenido no esté instalado correctamente.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Directrices de implementación"
>abstract="Los clientes deben revisar su código personalizado y sus paquetes para identificar si el contenido se entrega a `/libs`. AEM Si es necesario, refactorícelo para depender de la superposición del contenido en /apps y hacer que sea compatible con el as a Cloud Service. Póngase en contacto con el equipo de soporte de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Superposiciones"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Los paquetes de clientes deben implementar contenido en `/apps` en lugar de `/libs`.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
