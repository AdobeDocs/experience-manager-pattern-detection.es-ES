---
title: REP
description: Página de ayuda de código del detector de patrones.
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 96%

---

# [!DNL REP] {#rep}

Agente de replicación

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Agente de replicación"
>abstract="REP identifica los agentes de replicación habilitados. Se informa de ellos debido a la posibilidad de que se produzcan problemas que deben abordarse al actualizar a AEM as a Cloud Service. AEM as a Cloud Service utiliza Sling Content Distribution para distribuir contenido desde los entornos de creación a publicación. Esto se lleva a cabo fuera del tiempo de ejecución de AEM utilizando el servicio de canalización de Adobe I/O Runtime en Adobe Developer. Se configura automáticamente en el entorno de AEM as a Cloud Service suministrado."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents" text="Cambios importantes en AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents" text="Directrices de desarrollo"

`REP`  Identifica los agentes de replicación habilitados. Se informa de ellos debido a la posibilidad de que se produzcan problemas que deben abordarse al actualizar a AEM as a Cloud Service.

Los subtipos se utilizan para identificar diferentes tipos de información:

* `forward.replication`: identifique los agentes de replicación avanzada habilitados.
* `reverse.replication`: identifique los agentes de replicación inversa habilitados.
* `standard.replication.agent.modification`: identifique los agentes de replicación estándar habilitados que se han modificado.
* `custom.replication.agent.detection`: identifique los agentes de replicación personalizados habilitados.

AEM as a Cloud Service usa [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) para distribuir contenido de los entornos de creación a publicación. Esto se lleva a cabo fuera del tiempo de ejecución de AEM utilizando el servicio de canalización de Adobe I/O Runtime en Adobe Developer. Se configura automáticamente en el entorno de AEM as a Cloud Service suministrado.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La configuración de la replicación ha cambiado con AEM as a Cloud Service. Todos los agentes de replicación actuales deben revisarse para ver cuáles se sustituyen por la capacidad estándar, qué configuraciones deben moverse al código y cuáles no son compatibles.
* Cualquier uso de agentes de replicación en el código personalizado o en los flujos de trabajo debe revisarse mientras se actualiza a AEM as a Cloud Service.
* La replicación inversa no se admite inicialmente en AEM as a Cloud Service.
* No es necesario configurar un agente de vaciado de Dispatcher independiente. Esto se configura automáticamente en el entorno de AEM as a Cloud Service.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar, refactorizar y optimizar la funcionalidad personalizada directamente dependiente de los agentes de replicación y hacerla compatible con AEM as a Cloud Service. Póngase en contacto con el equipo de soporte de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication" text="Replicación: AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Consulte las [Directrices de desarrollo](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents) de AEM as a Cloud Service y las notas de la versión para [agentes de replicación](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents).
* Revise, refactorice y optimice la funcionalidad directamente dependiendo de los agentes de replicación para realizar tareas del negocio.
* Consulte cómo la [replicación](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication) se ve afectada por la implementación en AEM as a Cloud Service.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
