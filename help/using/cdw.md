---
title: CDW
description: Página de ayuda de código del detector de patrones
exl-id: a9e9dae8-0aa2-4679-a3c1-418cab01cfda
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 100%

---

# CDW {#cdw}

Widget de diálogo personalizado

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Widget de diálogo personalizado"
>abstract="CDW identifica los widgets de diálogo personalizados que deben actualizarse para que sean compatibles con AEM as a Cloud Service."

`CDW` Los widgets de diálogo personalizados identifican los widgets de diálogo personalizados clásicos y de CoralUI. Se deben actualizar para que sean compatibles con AEM as a Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de información, como:

* `custom.coral.widget`: identifique los widgets de diálogo personalizados basados en CoralUI 2 o CoralUI 3.
* `custom.classic.widget`: identifique los widgets de diálogo personalizados basados en ExtJs.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La IU clásica ya no está disponible en AEM as a Cloud Service. La interfaz estándar para la creación es la IU táctil.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Directrices de implementación"
>abstract="Póngase en contacto con el Servicio de atención al cliente para obtener ayuda."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Los widgets de diálogo personalizados clásicos deben convertirse de ExtJS a [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html).
* Los widgets de diálogo personalizados de Coral deben evaluarse para actualizarse a CoralUI 3.
* Póngase en contacto con nuestro [Equipo de servicio de atención al cliente de Experience Manager](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
