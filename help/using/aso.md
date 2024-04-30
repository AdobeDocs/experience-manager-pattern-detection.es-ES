---
title: ASO
description: Página de ayuda de código del detector de patrones.
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 67%

---

# ASO {#aso}

Información general del sistema AEM

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="Información general del sistema AEM"
>abstract="El código ASO identifica la información general acerca de la instancia de AEM. Cada búsqueda proporciona un valor de un tipo particular de información del sistema que puede ayudarle en la planificación de la migración y en el esfuerzo de refactorización."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service: Notas de la versión"

`ASO` AEM Identifica información general acerca de la instancia de. Cada búsqueda proporciona un valor de un tipo particular de información del sistema.

Los subtipos se utilizan para identificar diferentes tipos de información:

* `aem.version`: la versión de AEM.
* `aem.product`AEM : detección del uso de un producto de la (Commerce, Forms, etc.).
* `node.count`: el recuento aproximado de nodos de un tipo determinado (página, recurso, etc.) y el total general de nodos.
* `node.store`: el tipo de implementación del almacén de nodos (SegmentNodeStore, DocumentNodeStore) y su tamaño.
* `data.store`: el tipo de implementación del almacén de datos (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: una tarea de mantenimiento.
* `slow.query`: una consulta lenta.
* `group.membership`: el número de usuarios y subgrupos (miembros directos/declarados únicamente) de un grupo.
* `cqtag.count`: el número de activos etiquetados por CQ.
* `smarttag.count`: el número de activos etiquetados inteligentes.
* `ccom.version`: la versión del paquete de componentes principales.
* `instance.type`: el tipo de instancia de AEM (creación o publicación).
* `unprocessed.asset.count`: el número de activos sin procesar.
* `vanity.url.count`: el número de direcciones URL personalizadas.
* `index.size`: tamaño total del índice de Lucene migrable.
* `workflow.count`: número de flujos de trabajo de autor en estado en ejecución y obsoleto.
* `jvm.arguments`Los debates de JVM añadidos a la línea de comandos al iniciar la ejecución de AEM.

## Posibles implicaciones y riesgos {#implications-and-risks}

* AEM AEM La versión de la, los recuentos de nodos, los miembros del grupo, el almacén de nodos, los tipos de implementación del almacén de datos, el recuento de etiquetas CQ, el recuento de etiquetas inteligentes, la versión del componente principal, el tipo de instancia de la y el recuento de recursos sin procesar se proporcionan con fines informativos.
* El mayor número de URL mnemónicas (>1000) puede cargar Dispatcher y los servidores de publicación con consultas costosas.
* La aplicación personalizada puede depender de productos o características no disponibles en AEM as a Cloud Service.
* La actualización con funciones no compatibles puede provocar un error en la actualización y una aplicación no funcional.
* Un número elevado de flujos de trabajo de autor en estado en ejecución u obsoleto podría degradar el rendimiento.
* Las consultas lentas pueden degradar el rendimiento del sistema.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Directrices de implementación"
>abstract="La información expuesta mediante el código ASO proporciona información general para su entorno de AEM, incluida la versión, los complementos del producto y la información a nivel de sistema. Revísela para ver si hay productos o funciones no compatibles en AEM as a Cloud Service. Póngase en contacto con el equipo de soporte de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* AEM No se recomiendan las actualizaciones con productos o funciones no compatibles y es posible que no sean compatibles.
* Los activos no procesados deben ser procesados y el `dam:assetState` propiedad en el `jcr:content` del recurso debe establecerse en &quot;Procesado&quot;. O bien, debe eliminar estos recursos del conjunto de migración antes de migrarlos a AEMaaCS.
* Las URL mnemónicas podrían reemplazarse con las reescrituras de Apache.
* Consulte la [documentación](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/bestpractices/troubleshooting-slow-queries) para solucionar problemas de consultas lentas.
* Consulte la [notas de la versión](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current) AEM si desea obtener más información sobre los cambios más recientes en el as a Cloud Service de la.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
