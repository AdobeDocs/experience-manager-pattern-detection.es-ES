---
title: TRABAJO
description: Página de ayuda de código de Pattern Detector
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---

# WRK {#wrk}

Flujo de trabajo

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Flujo de trabajo"
>abstract="El código WRK identifica una búsqueda relacionada con un modelo de flujo de trabajo o un iniciador. Estos se informan porque los modelos de flujo de trabajo de recursos personalizados deben migrarse al actualizar a AEM como Cloud Service. Con AEM como Cloud Service, el procesamiento de recursos ahora se realiza mediante microservicios de recursos."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html" text="Microservicios de recursos"

`WRK` identifica una búsqueda relacionada con un modelo de flujo de trabajo o un lanzador. Estos se informan porque los modelos de flujo de trabajo de recursos personalizados deben migrarse al actualizar a AEM como Cloud Service.

Se utiliza un subtipo para identificar el tipo de problema de flujo de trabajo que se detecta actualmente.

* `custom.asset.workflow`: Detección de un modelo de flujo de trabajo de recursos personalizado o un iniciador.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Directrices de implementación"
>abstract="Como los flujos de trabajo de recursos estándar son compatibles automáticamente con mis microservicios de recursos, lo mejor es revisar todo el modelo de flujo de trabajo de recursos personalizado o el iniciador para ver si son necesarios una vez que realizamos la transición a AEM como Cloud Service. Las personalizaciones de los flujos de trabajo de recursos requieren la migración para trabajar con AEM como Cloud Service con la ayuda de la herramienta de migración del flujo de trabajo de recursos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html" text="Introducción: Microservicios de recursos"

* El procesamiento de recursos se ha realizado tradicionalmente con flujos de trabajo de recursos que se ejecutan en la instancia de AEM Author. Con AEM como Cloud Service, el procesamiento de recursos ahora se realiza mediante microservicios de recursos. (Consulte la [descripción general de los microservicios de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) para obtener más información.
* Los flujos de trabajo de recursos estándar son compatibles automáticamente con mis microservicios de recursos.
* Las personalizaciones de los flujos de trabajo de recursos requieren una migración para trabajar con AEM como Cloud Service.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Herramientas y recursos"
>abstract="Revise y planifique ejecutar la herramienta de migración del flujo de trabajo de recursos una vez que se identifique un modelo de flujo de trabajo de recursos personalizado o un iniciador. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html" text="Herramienta de Migración del flujo de trabajo de recursos"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"

* Si se identifica un modelo de flujo de trabajo de recursos personalizado o un iniciador, planifique ejecutar la [Herramienta de migración del flujo de trabajo de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html).
* Consulte la [Introducción a los microservicios de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html) para obtener más información.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
