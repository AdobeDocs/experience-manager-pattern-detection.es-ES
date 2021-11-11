---
title: ASO
description: Página de ayuda de código de Pattern Detector
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: 3e05ecb2c78b0ebf97d334cf592347b54255c75f
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 4%

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
* `node.count`: El recuento aproximado de nodos de un tipo determinado (página, recurso, etc.) y el total general de nodos.
* `node.store`: El tipo de implementación del almacén de nodos (SegmentNodeStore, DocumentNodeStore) y su tamaño.
* `data.store`: Tipo de implementación del almacén de datos (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Una tarea de mantenimiento.
* `slow.query`: Una consulta lenta.
* `group.membership`: Número de usuarios y subgrupos ( miembros directos/declarados únicamente ) de un grupo.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La versión de AEM, los recuentos de nodos, la pertenencia a grupos y los tipos de implementación del almacén de nodos y el almacén de datos se proporcionan con fines informativos.
* La aplicación personalizada puede depender de productos o características no disponibles en AEM as a Cloud Service.
* La actualización con funciones no compatibles puede provocar un error en la actualización y una aplicación no funcional.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Directrices de implementación"
>abstract="La información expuesta a través del código ASO proporciona información general para su entorno de AEM, incluida la versión, los complementos del producto, la información a nivel del sistema, y esto debe revisarse para cualquier producto o función no compatible de AEM as a Cloud Service. Póngase en contacto con el soporte de Adobe para obtener ayuda y aclaraciones."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"

* No se recomiendan AEM actualizaciones con productos o funciones no compatibles y es posible que no sean compatibles.
* Consulte la [notas de la versión](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=es) para obtener más información sobre los cambios más recientes en AEM as a Cloud Service.
* Póngase en contacto con nuestra [Equipo de asistencia AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
