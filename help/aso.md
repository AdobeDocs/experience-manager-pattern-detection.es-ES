---
title: ASO
description: Página de ayuda de código de Pattern Detector
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
translation-type: tm+mt
source-git-commit: 449288e567adda9998a89e0ad5198fd5a4e93f35
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 5%

---

# ASO {#aso}

Información general del sistema AEM

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="Información general del sistema AEM"
>abstract="El código ASO identifica la información general sobre la instancia de AEM. Cada búsqueda proporciona un valor de un tipo particular de información del sistema que puede ayudarle en la planificación de la migración y en el esfuerzo de refactorización."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service: Notas de la versión"

`ASO` identifica información general sobre la instancia de AEM. Cada búsqueda proporciona un valor de un tipo particular de información del sistema.

Los subtipos se utilizan para identificar diferentes tipos de información:

* `aem.version`: La versión AEM.
* `aem.product`: Detección del uso de un producto AEM (Comercio, Forms, etc.).
* `node.count`: Recuento aproximado de nodos de un tipo determinado (página, recurso, etc.).
* `node.store`: El tipo de implementación del almacén de nodos (SegmentNodeStore, DocumentNodeStore).
* `data.store`: Tipo de implementación del almacén de datos (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Una tarea de mantenimiento.
* `slow.query`: Una consulta lenta.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La versión de AEM, los recuentos de nodos y los tipos de implementación del almacén de nodos y del almacén de datos se proporcionan con fines informativos.
* La aplicación personalizada puede depender de productos o características que no están disponibles en AEM como Cloud Service.
* La actualización con funciones no compatibles puede provocar un error en la actualización y una aplicación no funcional.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Directrices de implementación"
>abstract="La información expuesta a través del código ASO proporciona información general para su entorno AEM, incluida la versión, los complementos de producto, la información a nivel del sistema, y esto debe revisarse para cualquier producto o función no compatible en AEM como Cloud Service. Póngase en contacto con el soporte de Adobe para obtener ayuda y aclaraciones."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"

* No se recomiendan AEM actualizaciones con productos o funciones no compatibles y es posible que no sean compatibles.
* Revise las [notas de la versión](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=es) para conocer los cambios más recientes en AEM como Cloud Service.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
