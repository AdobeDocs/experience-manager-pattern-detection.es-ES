---
title: CTEM
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 4%

---


# CTEM {#ctem}

Plantilla personalizada

## Fondo {#background}

`CTEM` identifica las plantillas personalizadas que se han instalado en AEM. Esta información se proporciona a los efectos de la evaluación de las prácticas recomendadas.

Las plantillas se identifican con un valor de tipo principal &quot;cq:Template&quot;. Con este código se utiliza un subtipo para identificar la categoría de la plantilla:

* `custom.editable.template`: La ruta de la plantilla no comienza con &quot;/apps&quot;.
* `custom.static.template`: La ruta de la plantilla comienza con &quot;/apps&quot;.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Una práctica recomendada es mover todas las plantillas estáticas a plantillas editables.

## Posibles soluciones {#solutions}

* Aproveche las [AEM Herramientas de modernización](https://opensource.adobe.com/aem-modernize-tools/) para migrar plantillas estáticas a plantillas editables.
* Encontrará más información sobre las plantillas editables en [Plantillas](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html).
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
