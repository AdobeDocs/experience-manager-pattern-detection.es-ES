---
title: DOPI
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# DOPI {#dopi}

Índice de propiedades ordenadas en desuso

## Fondo {#background}

`DOPI` identifica el uso de definiciones de índice de propiedad ordenadas (`primaryType=oak:QueryIndexDefinition` AND  `type="ordered"`), que han quedado obsoletas desde la versión 6.1 y se eliminaron en la versión 6.2.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Es posible que algunas consultas no respondan.
* Es posible que la funcionalidad del cliente no funcione correctamente.
* Las advertencias transversales o incluso los errores y las sanciones de rendimiento significativas, ya que los índices obsoletos no tienen ningún efecto.

## Posibles soluciones {#solutions}

* Modifique la definición del índice para que se convierta o reemplace el índice por una definición de índice admitida. (Consulte [Consultas e indexación de Oak](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html)).
* Revise el proyecto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) y comprenda cómo se pueden corregir las [violaciones del DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) y hacerlas compatibles con AEM como Cloud Service.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
