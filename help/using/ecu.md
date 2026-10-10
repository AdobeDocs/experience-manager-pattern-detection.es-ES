---
title: ECU
description: Página de ayuda de código del detector de patrones.
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 97%
---
# ECU {#ecu}

OBSOLETO: uso de contenido externo (reemplazado por CAV, infracción de área de contenido)

## Fondo {#background}

`ECU` Identifica el patrón en el que se utilizan distintas áreas de contenido de forma que se infringen las reglas de la clasificación de contenido.

El procesamiento de solicitudes de Sling define el modo en que el contenido de un recurso, su propiedad `sling:resourceType` en particular, se utiliza para determinar la secuencia de comandos que se utiliza para procesar el contenido. (Consulte [Localización del script](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-scrip) para obtener más información). Sling también proporciona técnicas para acceder y combinar recursos a través de Superposiciones y Anulaciones. Estas técnicas se describen como parte de [Combinación de recursos de Sling](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) y en [Superposiciones](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Para que sea más seguro y fácil para los clientes comprender qué áreas de `/libs` son seguras de utilizar y superponer, el contenido de `/libs` se ha clasificado con propiedades de “mezcla”:

* Público
* Descripción breve
* Final
* Interno

Cada clasificación implica reglas acerca de cómo se puede usar, heredar o superponer el contenido. Consulte [Actualizaciones sostenibles](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) para obtener una descripción detallada.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Una actualización de AEM puede provocar problemas de procesamiento de páginas y otros comportamientos no deseados.
* Las actualizaciones de seguridad no son efectivas.

## Posibles soluciones {#solutions}

* Minimice el uso de la superposición de contenido en los casos en que sea necesario.
* En particular, evite superponer el contenido restringido (clasificación Final e Interno).
* Considere la posibilidad de adaptar los cambios provenientes de `/libs` después de las actualizaciones de AEM, las instalaciones de Service Pack o Fix Pack acumulativo.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
