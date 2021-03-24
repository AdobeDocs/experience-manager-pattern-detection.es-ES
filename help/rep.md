---
title: REP
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: 7d05067fc624571e6fe520e2a1addd5dff8acbd8
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 2%

---


# [!DNL REP] {#rep}

Agente de replicación

## Fondo {#background}

`REP` identifica los agentes de replicación habilitados. Se informa de ellas debido a la posibilidad de que se aborden problemas que deberían abordarse al actualizar a AEM como Cloud Service.

AEM como Cloud Service utiliza [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) para distribuir contenido de los entornos de autor a publicación. Esto se realiza fuera del tiempo de ejecución de AEM mediante el servicio de canalización de Adobe I/O. Esto se configura automáticamente en el AEM aprovisionado como entorno de Cloud Service.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La configuración de la replicación ha cambiado con AEM como Cloud Service. Todos los agentes de replicación actuales deben revisarse para ver cuáles se sustituyen por la capacidad estándar, qué configuraciones deben moverse al código y cuáles no son compatibles.
* Cualquier uso de agentes de replicación en código personalizado o flujos de trabajo debe revisarse mientras se actualiza a AEM como Cloud Service.
* La replicación inversa no se admite inicialmente en AEM como Cloud Service.
* No es necesario configurar un agente de vaciado de Dispatcher independiente. Esto se configura automáticamente en el AEM como entorno de Cloud Service.

## Posibles soluciones {#solutions}

* Consulte el AEM como Cloud Service [Development Guidelines](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents) y las notas de la versión para [agentes de replicación](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents).
* Revise, refactorice y optimice la funcionalidad directamente dependiendo de los agentes de replicación para realizar tareas del negocio.
* Vea cómo [replication](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication) se ve afectada por la implementación en AEM como Cloud Service.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
