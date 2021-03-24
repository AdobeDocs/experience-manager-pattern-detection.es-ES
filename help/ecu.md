---
title: ECU
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---


# ECU {#ecu}

OBSOLETO: Uso de contenido externo (reemplazado por CAV, infracción de área de contenido)

## Fondo {#background}

`ECU` identifica el patrón en el que se utilizan distintas áreas de contenido de forma que se infringen las reglas de la clasificación de contenido.

El procesamiento de solicitudes de Sling define cómo se utiliza el contenido de un recurso, su propiedad `sling:resourceType` en particular, para determinar la secuencia de comandos que se utilizará para procesar el contenido. (Consulte [Localización del script](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) para obtener más información). Sling también proporciona técnicas para acceder y combinar recursos a través de &quot;Superposiciones&quot; y &quot;Anulaciones&quot;. Estos se describen como parte de la [fusión de recursos de Sling](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) y en [Superposiciones](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html).

Para que sea más seguro y fácil para los clientes comprender qué áreas de `/libs` son seguras de usar y superponer el contenido en `/libs` se ha clasificado con propiedades de &quot;mezcla&quot;: Público, Abstracto, Final e Interno. Cada clasificación implica reglas sobre cómo se puede usar, heredar o superponer el contenido. Consulte [Actualizaciones sostenibles](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html) para obtener una descripción detallada.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Una actualización AEM puede provocar problemas de procesamiento de páginas y otros comportamientos no deseados.
* Las actualizaciones de seguridad no son efectivas.

## Posibles soluciones {#solutions}

* Minimice el uso de la superposición de contenido en los casos en que sea necesario.
* En particular, evite superponer el contenido restringido (clasificación final e interna).
* Considere la posibilidad de adaptar los cambios procedentes de `/libs` después de AEM actualizaciones, ServicePack o instalaciones de CumulativeFixPack.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
