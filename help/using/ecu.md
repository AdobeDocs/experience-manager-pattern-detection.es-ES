---
title: ECU
description: Página de ayuda de código del detector de patrones
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 100%

---

# ECU {#ecu}

OBSOLETO: uso de contenido externo (reemplazado por CAV, infracción de área de contenido)

## Fondo {#background}

`ECU` identifica el patrón en el que se utilizan distintas áreas de contenido de forma que se infringen las reglas de la clasificación de contenido.

El procesamiento de solicitudes de Sling define el modo en que el contenido de un recurso, su propiedad `sling:resourceType` en particular, se utiliza para determinar la secuencia de comandos que se utilizará para procesar el contenido. (Consulte [Localización de la secuencia de comandos](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html?lang=es#locating-the-script) para obtener más información). Sling también proporciona técnicas para acceder y combinar recursos a través de Superposiciones y Anulaciones. Estas se describen como parte de [Fusión de recursos de Sling](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=es) y en [Superposiciones](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=es).

Para que sea más seguro y fácil para los clientes comprender qué áreas de `/libs` son seguras de usar y superponer, el contenido en `/libs` se ha clasificado con propiedades de “mezcla”: Público, Abstracto, Final e Interno. Cada clasificación implica reglas acerca de cómo se puede usar, heredar o superponer el contenido. Consulte [Actualizaciones sostenibles](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=es) para obtener una descripción detallada.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Una actualización de AEM puede provocar problemas de procesamiento de páginas y otros comportamientos no deseados.
* Las actualizaciones de seguridad no son efectivas.

## Posibles soluciones {#solutions}

* Minimice el uso de la superposición de contenido en los casos en que sea necesario.
* En particular, evite superponer el contenido restringido (clasificación Final e Interno).
* Considere la posibilidad de adaptar los cambios procedentes de `/libs` después de las actualizaciones de AEM o las instalaciones de ServicePack o CumulativeFixPack.
* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
