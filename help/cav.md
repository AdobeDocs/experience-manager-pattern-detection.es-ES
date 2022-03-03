---
title: CAV
description: Página de ayuda de código del detector de patrones
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 1966a3e83ab6b2247d9f1095c8965eac399e3b6e
workflow-type: ht
source-wordcount: '366'
ht-degree: 100%

---

# CAV {#cav}

Infracción de área de contenido

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Infracción de área de contenido"
>abstract="El código CAV identifica el patrón en el que se utilizan diferentes áreas de contenido de una manera que infringe las reglas de la clasificación de contenido. Esta infracción le daría una visión general de las superposiciones, el contenido restringido que podría necesitar cambios una vez que pasemos a AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=es#platform" text="Fusión de recursos de Sling"

`CAV` identifica el patrón en el que se utilizan distintas áreas de contenido de forma que se infringen las reglas de la clasificación de contenido.

El procesamiento de solicitudes de Sling define el modo en que el contenido de un recurso, su propiedad `sling:resourceType` en particular, se utiliza para determinar la secuencia de comandos que se utilizará para procesar el contenido. Consulte [Localización de la secuencia de comandos](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html?lang=es#locating-the-script) para obtener más información. Sling también proporciona técnicas para acceder y combinar recursos a través de Superposiciones y Anulaciones. Estas se describen como parte de [Fusión de recursos de Sling](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=es) y en [Superposiciones](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=es).

Para que sea más seguro y fácil para los clientes comprender qué áreas de `/libs` son seguras de usar y superponer, el contenido en `/libs` se ha clasificado con propiedades de “mezcla”: Público, Abstracto, Final e Interno. Cada clasificación implica reglas acerca de cómo se puede usar, heredar o superponer el contenido. Consulte [Actualizaciones sostenibles](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=es) para obtener una descripción detallada.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Una actualización de AEM puede provocar problemas de procesamiento de páginas y otros comportamientos no deseados.
* Las actualizaciones de seguridad no son efectivas.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Directrices de implementación"
>abstract="Deben revisarse los patrones identificados con CAS en los que existen diferentes infracciones de área de contenido. Deben evitarse las áreas clásicas de contenido Final e Interno. Póngase en contacto con el Soporte de Adobe para obtener ayuda y aclaraciones."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=es" text="Actualizaciones sostenibles"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Minimice el uso de la superposición de contenido en los casos en que sea necesario.
* En particular, evite superponer el contenido restringido (clasificación Final e Interno).
* Considere la posibilidad de adaptar los cambios procedentes de `/libs` después de las actualizaciones de AEM o las instalaciones de ServicePack o CumulativeFixPack.
* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
