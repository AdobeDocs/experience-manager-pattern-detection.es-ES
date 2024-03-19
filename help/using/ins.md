---
title: INS
description: Página de ayuda de código del detector de patrones
exl-id: d89e1589-3195-4b2d-98f4-136bedaecb0b
source-git-commit: 07af2303583072effbaaf23de1878e4d0dcfd2bd
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 100%

---

# INS {#ins}

Espacio de nombres no válido

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_overview"
>title="Espacio de nombres no válido"
>abstract="INS identifica los problemas de espacio de nombres en la instancia de AEM"

`INS` Espacio de nombres no válido identifica problemas de espacio de nombres en la instancia de AEM.

Los subtipos se utilizan para identificar los diferentes tipos de información, como:

* `uri`: identifica el URI del espacio de nombres no válido en AEM.

## Posibles implicaciones y riesgos {#implications-and-risks}

* No se puede replicar contenido (en varios niveles) ni copiar contenido (en varios niveles - a través de `/crx/packMgr` o una copia de contenido).

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="Directrices de implementación"
>abstract="Póngase en contacto con el Servicio de atención al cliente para obtener ayuda."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Corrige las definiciones de espacio de nombres según la [Especificación JCR](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html?lang=es). Sigue los pasos mencionados [aquí](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163)
* Póngase en contacto con nuestro [Equipo de servicio de atención al cliente de Experience Manager](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
