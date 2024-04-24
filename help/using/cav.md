---
title: CAV
description: Página de ayuda de código de Pattern Detector.
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 45%

---

# CAV {#cav}

Infracción de área de contenido

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Infracción de área de contenido"
>abstract="El código CAV identifica el patrón en el que se utilizan diferentes áreas de contenido de una manera que infringe las reglas de la clasificación de contenido. AEM Esta infracción le daría una visión general de las superposiciones, el contenido restringido que podría tener que cambiar después de que se mueva a la posición as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Fusión de recursos de Sling"

`CAV` Identifica el patrón en el que se utilizan diferentes áreas de contenido de manera que se infringen las reglas de la clasificación de contenido.

El procesamiento de solicitudes de Sling define el modo en que el contenido de un recurso, su `sling:resourceType` en particular, se utiliza para determinar la secuencia de comandos que se utiliza para procesar el contenido. Consulte [Localización de la secuencia de comandos](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) para obtener más información. Sling también proporciona técnicas para acceder y combinar recursos a través de Superposiciones y Anulaciones. Estas se describen como parte de [Fusión de recursos de Sling](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) y en [Superposiciones](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Para que sea más seguro y fácil para los clientes comprender qué áreas de `/libs` son seguros de usar y superponer el contenido en `/libs` se ha clasificado con propiedades de &quot;mezcla&quot;: Pública, Abstracta, Final e Interna. Cada clasificación implica reglas acerca de cómo se puede usar, heredar o superponer el contenido. Consulte [Actualizaciones sostenibles](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) para obtener una descripción detallada.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Una actualización de AEM puede provocar problemas de procesamiento de páginas y otros comportamientos no deseados.
* Las actualizaciones de seguridad no son efectivas.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Directrices de implementación"
>abstract="Deben revisarse los patrones identificados con CAS en los que existen diferentes infracciones de área de contenido. Deben evitarse las áreas de clasificación de contenido Final e Interno. Póngase en contacto con el Soporte técnico de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Actualizaciones sostenibles"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Minimice el uso de la superposición de contenido en los casos en que sea necesario.
* En particular, evite superponer el contenido restringido (clasificación Final e Interno).
* Considere adaptar los cambios procedentes de `/libs` AEM después de las actualizaciones, las instalaciones del paquete de servicio o las del paquete de correcciones acumulativas de la.
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclaraciones o para que se aborden las preocupaciones.
