---
title: DG
description: Página de ayuda de código del detector de patrones.
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 80%

---

# DG {#dg}

Directrices para desarrolladores

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Directrices para desarrolladores"
>abstract="El código DG identifica las desviaciones de determinadas directrices de desarrollo para AEM 6.5 y AEM as a Cloud Service. Las siguientes prácticas recomendadas pueden mejorar la capacidad de mantenimiento y el rendimiento del sistema. Aunque algunas de estas desviaciones pueden no ser un problema en otros contextos de aplicación, incluidas las versiones anteriores de AEM, pueden causar problemas cuando se utilizan con AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="Desarrollo de AEM: directrices y prácticas recomendadas"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Directrices de desarrollo de AEM as a Cloud Service"


`DG` Identifica las desviaciones de las directrices de desarrollo seleccionadas para [AEM 6.5](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices) y [AEM as a Cloud Service](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines).  Las siguientes prácticas recomendadas pueden mejorar la capacidad de mantenimiento y el rendimiento del sistema. Aunque algunas de estas desviaciones pueden no ser un problema en otros contextos de aplicación, incluidas las versiones anteriores de AEM, pueden causar problemas cuando se utilizan con AEM as a Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de infracciones detectadas:

* `java.io.inputstream`: el uso de `java.io.InputStream` en el código de la aplicación.
* `maintenance.task.configuration`: la configuración de una determinada actividad de mantenimiento periódico.
* `sling.commons.scheduler`: el uso de la API del Planificador de Sling Commons para una tarea programada.
* `unsupported.asset.api`: el uso de la API del Administrador de recursos no admitidas en el código de la aplicación.
* `javax.jcr.observation.EventListener`: el uso del receptor de eventos en el código de la aplicación.
* `custom.guava.cache`: el uso de la caché de Guava en el código de la aplicación.
* `java.api`: Algunas API de Java se eliminaron de Java 11 a Java 17.
* `configuration.admin`: se marcará el código personalizado que está accediendo a las configuraciones.
* `guava.api`: la guayaba no se admite de forma predeterminada en AEM 6.5 LTS.
* `com.day.cq.dam.scene7.api.model`: Hay un cambio de versión importante para `package com.day.cq.dam.scene7.api.model`.

## Posibles implicaciones y riesgos {#implications-and-risks}

* `java.io.inputstream`
   * El streaming de datos binarios con `java.io.InputStream` puede consumir recursos de memoria hasta el punto de afectar al rendimiento. Este problema se debe a la limitada memoria disponible en los contenedores utilizados en AEM as a Cloud Service.

* `maintenance.task.configuration`
   * Algunas tareas de mantenimiento que anteriormente requerían una configuración explícita ahora se configuran y administran automáticamente dentro de AEM as a Cloud Service.
   * La configuración de la tarea de mantenimiento en AEM as a Cloud Service debe moverse al control de origen.

* `sling.commons.scheduler`
   * Las aplicaciones dependientes de tareas en segundo plano que utilizan el [Planificador de Sling Commons](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) pueden no funcionar como se espera porque la ejecución no se puede garantizar en AEM as a Cloud Service.
   * Las directrices para [tareas en segundo plano y trabajos de larga duración](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#background-tasks-and-long-running-jobs) sugieren que el código ejecutado como tarea programada debe suponer que la instancia en la que se está ejecutando puede caerse en cualquier momento. Por lo tanto, el código debe ser flexible y reanudable.

* `unsupported.asset.api`
   * Las siguientes API de AssetManager están marcadas como no admitidas en AEM as a Cloud Service.
      * createAssetForBinary
      * getAssetForBinary
      * removeAssetForBinary
      * createAsset

* `javax.jcr.observation.EventListener`
   * Es posible que las aplicaciones que dependen del receptor de eventos no funcionen del modo esperado porque no se puede garantizar la ejecución.

* `custom.guava.cache`
   * El uso de la caché de Guava puede causar problemas de rendimiento en AEM.

* `java.api`
   * Con AEM 6.5 LTS en JRE17, estas API de Java eliminadas no estarán disponibles y su uso fallará.

* `configuration.admin`
   * Debe observar su uso para asegurarse de que no está usando ninguna configuración no admitida, como social.

* `guava.api`
   * Como Guayaba no es compatible con AEM 6.5 LTS, el código personalizado que utiliza guayaba no estará activo.

* `com.day.cq.dam.scene7.api.model`
   * El paquete importado `com.day.cq.dam.scene7.api.model` en paquetes personalizados no se resolverá debido a un cambio de versión importante.


## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="Directrices de implementación"
>abstract="Revise sus implementaciones sobre el uso del planificador de Sling Commons. Reestructúrelas a Sling Jobs, reestructure las tareas de mantenimiento del sistema, revise el streaming de cualquier dato binario y refactorice su código para que sea compatible con AEM as a Cloud Service."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Trabajos de Sling"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/operations/maintenance" text="Tareas de mantenimiento en AEM as a Cloud Service"

* `java.io.inputstream`
   * Utilice un método de carga binario directo en el que el binario se añada directamente al almacén de datos.
   * Para casos de uso de recursos, consulte [aem-upload](https://github.com/adobe/aem-upload). Para otros tipos de binarios, la lógica de carga personalizada se puede modelar según este mismo patrón.

* `maintenance.task.configuration`
   * Revise la documentación [Tarea de mantenimiento](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/operations/maintenance) de AEM as a Cloud Service.
   * Asegúrese de que [Configuración de tarea de mantenimiento](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/deploying/overview#maintenance-tasks-configuration-in-source-control) está en el control de origen.

* `sling.commons.scheduler`
   * Reemplace el uso del [Planificador de Sling Commons](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) con [Trabajos de Sling](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), que tienen una garantía de ejecución de al menos una vez.
   * Deben evitarse los trabajos de larga duración.

* `unsupported.asset.api`
   * En lugar de utilizar las API del Administrador de recursos no admitidas, consulte [aem-upload](https://github.com/adobe/aem-upload).

* `javax.jcr.observation.EventListener`
   * En lugar de utilizar el receptor de eventos, se recomienda refactorizar el mecanismo de gestión de eventos a [Trabajos de Sling](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), ya que proporciona la garantía de procesamiento.

* `custom.guava.cache`
   * Las cachés, si es necesario, deben crearse fuera de AEM. Se puede considerar una solución de almacenamiento en caché externa.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.

* `configuration.admin`
   * Elimine cualquier uso de configuración de funciones no compatibles como Social.

* `guava.api`
   * Instale Guava o elimine el uso si Guava se utiliza en su código personalizado.

* `com.day.cq.dam.scene7.api.model`
   * Actualice el intervalo de versiones del paquete importado `com.day.cq.dam.scene7.api.model` a **3.0.4**.