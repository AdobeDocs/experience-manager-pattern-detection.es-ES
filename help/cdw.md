---
title: CDW
description: Página de ayuda de código del detector de patrones
source-git-commit: 04709ba74eedad903669aae589c605542e1e3b09
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 44%

---

# CDW {#cdw}

Widget de diálogo personalizado

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Widget de diálogo personalizado"
>abstract="CDW identifica los widgets de cuadro de diálogo personalizados que deben actualizarse para que sean compatibles con AEM as a Cloud Service."

`CDW`  Los widgets de cuadro de diálogo personalizados identifican los widgets de cuadro de diálogo personalizados CoralUI y Classic . Se deben actualizar para que sean compatibles con AEM as a Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de información, como:

* `custom.coral.widget`: Identifique los widgets de cuadro de diálogo personalizados según CoralUI 2 o CoralUI 3.
* `custom.classic.widget`: Identifique los widgets de diálogo personalizados en función de ExtJs.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La IU clásica ya no está disponible en AEM as a Cloud Service. La interfaz estándar para la creación es la IU táctil.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Directrices de implementación"
>abstract="Póngase en contacto con el Servicio de atención al cliente para obtener ayuda."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Los widgets de cuadro de diálogo personalizados Classic deben convertirse de ExtJS a [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html).
* Los widgets de diálogo de coral personalizados deben evaluarse para actualizarse a CoralUI 3.
* Póngase en contacto con nuestro [Equipo de servicio de atención al cliente de Experience Manager](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
