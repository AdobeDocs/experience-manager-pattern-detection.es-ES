---
title: DG
description: Página de ayuda de código de Pattern Detector
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 1%

---

# DG {#dg}

Directrices para desarrolladores

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Directrices para desarrolladores"
>abstract="El código DG identifica las desviaciones de determinadas directrices de desarrollo para AEM 6.5 y AEM como Cloud Service. Las prácticas recomendadas pueden mejorar la capacidad de mantenimiento y el rendimiento del sistema. Aunque algunas de estas desviaciones pueden no ser un problema en otros contextos de la aplicación, incluidas las versiones anteriores de AEM, pueden causar problemas cuando se utilizan con AEM como Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html" text="Desarrollo de AEM: directrices y prácticas recomendadas"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="Directrices de desarrollo de AEM as a Cloud Service"


`DG` identifica las desviaciones de las directrices de desarrollo seleccionadas para  [AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html) y  [AEM como Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html). Las prácticas recomendadas pueden mejorar la capacidad de mantenimiento y el rendimiento del sistema. Aunque algunas de estas desviaciones pueden no ser un problema en otros contextos de la aplicación, incluidas las versiones anteriores de AEM, pueden causar problemas cuando se utilizan con AEM como Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de infracciones detectadas:

* `java.io.inputstream`: El uso de  `java.io.InputStream` en el código de la aplicación.
* `maintenance.task.configuration`: La configuración de una determinada actividad de mantenimiento periódico.
* `sling.commons.scheduler`: El uso de la API del planificador de Sling Commons para una tarea programada.

## Posibles implicaciones y riesgos {#implications-and-risks}

* `java.io.inputstream`
   * La transmisión de datos binarios con `java.io.InputStream` puede consumir recursos de memoria hasta el punto de afectar al rendimiento. Esto es particularmente un problema debido a la limitada memoria disponible en contenedores utilizados en AEM como Cloud Service.

* `maintenance.task.configuration`
   * Algunas tareas de mantenimiento que anteriormente requerían una configuración explícita ahora se configuran y administran automáticamente en AEM como Cloud Service.
   * La configuración de la tarea de mantenimiento en AEM como Cloud Service debe moverse al control de código fuente.

* `sling.commons.scheduler`
   * Es posible que las aplicaciones que dependen de tareas en segundo plano que utilizan [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) no funcionen del modo esperado porque la ejecución no se puede garantizar en AEM como Cloud Service.
   * AEM como Cloud Service de directrices de desarrollo para [tareas en segundo plano y trabajos de larga duración](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#background-tasks-and-long-running-jobs) sugieren que el código ejecutado como tarea programada debe suponer que la instancia en la que se está ejecutando se puede reducir en cualquier momento. Por lo tanto, el código debe ser flexible y reanudable.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="Directrices de implementación"
>abstract="Siguiendo AEM directrices de desarrollo y prácticas recomendadas, los clientes deben revisar sus implementaciones sobre el uso del planificador de Sling Commons y reestructurarlas en trabajos de Sling, reestructurar sus tareas de mantenimiento del sistema, revisar la transmisión de cualquier dato binario y refactorizar su código para que sea compatible con AEM como Cloud Service."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Trabajos sling"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html" text="Tareas de mantenimiento en AEM como Cloud Service"

* `java.io.inputstream`
   * Utilice un método de carga binario directo en el que el binario se añada directamente al almacén de datos.
   * Para casos de uso de recursos, utilice [aem-upload](https://github.com/adobe/aem-upload). Para otros tipos de binarios, la lógica de carga personalizada se puede modelar según este mismo patrón.

* `maintenance.task.configuration`
   * Revise la documentación de AEM como Cloud Service [Maintenance Task](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html) .
   * Asegúrese de que [Maintenance Task Configuration](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#maintenance-tasks-configuration-in-source-control) esté en el control de código fuente.

* `sling.commons.scheduler`
   * Reemplace el uso de [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) por [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), que tienen una garantía de ejecución de al menos una vez.
   * Si es posible, deben evitarse los trabajos de larga duración.

* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
