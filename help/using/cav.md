---
title: CAV
description: Página de ayuda de código del detector de patrones.
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 74%

---

# CAV {#cav}

Infracción de área de contenido

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Infracción de área de contenido"
>abstract="El código CAV identifica el patrón en el que se utilizan diferentes áreas de contenido de una manera que infringe las reglas de la clasificación de contenido. AEM Esta infracción le daría una visión general de las superposiciones, el contenido restringido que podría tener que cambiar después de moverlo a la posición as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Fusión de recursos de Sling"

`CAV` Identifica el patrón en el que se utilizan distintas áreas de contenido de forma que se infringen las reglas de la clasificación de contenido.

El procesamiento de solicitudes de Sling define el modo en que el contenido de un recurso, su propiedad `sling:resourceType` en particular, se utiliza para determinar la secuencia de comandos que se utiliza para procesar el contenido. Consulte [Localización de la secuencia de comandos](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-scrip) para obtener más información. Sling también proporciona técnicas para acceder y combinar recursos a través de Superposiciones y Anulaciones. Estas técnicas se describen como parte de la [Fusión de recursos de Sling](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) y en [Superposiciones](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Para que sea más seguro y fácil para los clientes comprender qué áreas de `/libs` son seguros de usar y superponer, el contenido en `/libs` se clasifica con propiedades &quot;mixin&quot;:

* Público
* Descripción breve
* Final
* Interno

Cada clasificación implica reglas acerca de cómo se puede usar, heredar o superponer el contenido. Consulte [Actualizaciones sostenibles](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) para obtener una descripción detallada.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Una actualización de AEM puede provocar problemas de procesamiento de páginas y otros comportamientos no deseados.
* Las actualizaciones de seguridad no son efectivas.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Directrices de implementación"
>abstract="Deben revisarse los patrones identificados con CAS en los que existen diferentes infracciones de área de contenido. Deben evitarse las áreas de clasificación de contenido Final e Interno. Póngase en contacto con el equipo de soporte de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Actualizaciones sostenibles"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Minimice el uso de la superposición de contenido en los casos en que sea necesario.
* En particular, evite superponer el contenido restringido (clasificación Final e Interno).
* Considere la posibilidad de adaptar los cambios provenientes de `/libs` después de las actualizaciones de AEM, las instalaciones de Service Pack o Fix Pack acumulativo.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
