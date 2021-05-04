---
title: CAV
description: Página de ayuda de código de Pattern Detector
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
translation-type: tm+mt
source-git-commit: 1966a3e83ab6b2247d9f1095c8965eac399e3b6e
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# CAV {#cav}

Infracción de área de contenido

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Infracción de área de contenido"
>abstract="El código CAV identifica el patrón en el que se utilizan diferentes áreas de contenido de una manera que infringe las reglas de la clasificación de contenido. Esta infracción le daría una visión general de las superposiciones, el contenido restringido que podría necesitar cambios una vez que pasemos a AEM como Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Fusión de recursos de Sling"

`CAV` identifica el patrón en el que se utilizan distintas áreas de contenido de forma que se infringen las reglas de la clasificación de contenido.

El procesamiento de solicitudes de Sling define cómo se utiliza el contenido de un recurso, su propiedad `sling:resourceType` en particular, para determinar la secuencia de comandos que se utilizará para procesar el contenido. Consulte [Locating the script](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) para obtener más información. Sling también proporciona técnicas para acceder y combinar recursos a través de &quot;Superposiciones&quot; y &quot;Anulaciones&quot;. Estos se describen como parte de la [fusión de recursos de Sling](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) y en [Superposiciones](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html).

Para que sea más seguro y fácil para los clientes comprender qué áreas de `/libs` son seguras de usar y superponer el contenido en `/libs` se ha clasificado con propiedades de &quot;mezcla&quot;: Público, Abstracto, Final e Interno. Cada clasificación implica reglas sobre cómo se puede usar, heredar o superponer el contenido. Consulte [Actualizaciones sostenibles](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html) para obtener una descripción detallada.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Una actualización AEM puede provocar problemas de procesamiento de páginas y otros comportamientos no deseados.
* Las actualizaciones de seguridad no son efectivas.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Directrices de implementación"
>abstract="Deben revisarse los patrones identificados con CAS en los que existen diferentes violaciones de área de contenido. Deben evitarse las áreas clásicas de contenido final e interno. Póngase en contacto con el soporte de Adobe para obtener ayuda y aclaraciones."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html" text="Actualizaciones sostenibles"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"

* Minimice el uso de la superposición de contenido en los casos en que sea necesario.
* En particular, evite superponer el contenido restringido (clasificación final e interna).
* Considere la posibilidad de adaptar los cambios procedentes de `/libs` después de AEM actualizaciones, ServicePack o instalaciones de CumulativeFixPack.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
