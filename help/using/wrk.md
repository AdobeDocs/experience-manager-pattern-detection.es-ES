---
title: WRK
description: Página de ayuda de código de Pattern Detector.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 62%

---

# WRK {#wrk}

Flujo de trabajo

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Flujo de trabajo"
>abstract="El código WRK identifica un hallazgo relacionado con un modelo de flujo de trabajo o un lanzador. Estos se registran porque los modelos de flujo de trabajo de recursos personalizados deben migrarse al actualizar a AEM as a Cloud Service. Con AEM as a Cloud Service, el procesamiento de recursos ahora se realiza mediante microservicios de recursos."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview" text="Microservicios de recursos"

WRK identifica un hallazgo relacionado con un modelo de flujo de trabajo o un lanzador. Estos se registran porque los modelos de flujo de trabajo de recursos personalizados deben migrarse al actualizar a AEM as a Cloud Service.

Se utiliza un subtipo para identificar el tipo de problema de flujo de trabajo que se detecta actualmente.

* `custom.asset.workflow`: detección de un modelo de flujo de trabajo de recursos personalizado o un lanzador.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Directrices de implementación"
>abstract="Los flujos de trabajo de recursos estándar son compatibles automáticamente con mis microservicios de recursos. AEM Por lo tanto, una práctica recomendada es revisar todos los modelos de flujo de trabajo de recursos personalizados o el lanzador para ver si son necesarios después de realizar la transición a un flujo de trabajo as a Cloud Service de la. AEM Las personalizaciones de los flujos de trabajo de recursos requieren la migración para funcionar con los flujos de trabajo de recursos as a Cloud Service con la ayuda de la herramienta de migración del flujo de trabajo de recursos"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use" text="Introducción: microservicios de recursos"

* El procesamiento de recursos se ha realizado tradicionalmente con flujos de trabajo de recursos que se ejecutan en la instancia de creación de AEM. Con AEM as a Cloud Service, el procesamiento de recursos ahora se realiza mediante microservicios de recursos. Consulte la [información general sobre microservicios de recursos](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview) para obtener más información.
* Los flujos de trabajo de recursos estándar son compatibles automáticamente con mis microservicios de recursos.
* AEM Las personalizaciones de los flujos de trabajo de recursos requieren la migración para funcionar con los flujos de trabajo de recursos as a Cloud Service de forma.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Herramientas y recursos"
>abstract="Revise y planifique la ejecución de la herramienta de migración del flujo de trabajo de recursos una vez que se identifique un modelo de flujo de trabajo de recursos personalizado o un lanzador. Póngase en contacto con el Soporte técnico de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool" text="Herramienta de migración del flujo de trabajo de recursos"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Si se identifica un modelo de flujo de trabajo de recursos personalizado o un lanzador, planifique la ejecución de la [Herramienta de migración del flujo de trabajo de recursos](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool).
* Consulte la [Introducción a los microservicios de recursos](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use) para obtener más información.
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclaraciones o para que se aborden las preocupaciones.
