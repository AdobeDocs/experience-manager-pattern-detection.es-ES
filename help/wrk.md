---
title: TRABAJO
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 1%

---


# WRK {#wrk}

Flujo de trabajo

## Fondo {#background}

`WRK` identifica una búsqueda relacionada con un modelo de flujo de trabajo o un lanzador. Estos se informan porque los modelos de flujo de trabajo de recursos personalizados deben migrarse al actualizar a AEM como Cloud Service.

Se utiliza un subtipo para identificar el tipo de problema de flujo de trabajo que se detecta actualmente.

* `custom.asset.workflow`: Detección de un modelo de flujo de trabajo de recursos personalizado o un iniciador.

## Posibles implicaciones y riesgos {#implications-and-risks}

* El procesamiento de recursos se ha realizado tradicionalmente con flujos de trabajo de recursos que se ejecutan en la instancia de AEM Author. Con AEM como Cloud Service, el procesamiento de recursos ahora se realiza mediante microservicios de recursos. (Consulte la [descripción general de los microservicios de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) para obtener más información.
* Los flujos de trabajo de recursos estándar son compatibles automáticamente con mis microservicios de recursos.
* Las personalizaciones de los flujos de trabajo de recursos requieren una migración para trabajar con AEM como Cloud Service.

## Posibles soluciones {#solutions}

* Si se identifica un modelo de flujo de trabajo de recursos personalizado o un iniciador, planifique ejecutar la [Herramienta de migración del flujo de trabajo de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html).
* Consulte la [Introducción a los microservicios de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html) para obtener más información.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
