---
title: MI
description: Página de ayuda de código del detector de patrones.
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 85%

---

# MI {#mi}

Problema de configuración incorrecta

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Problema de configuración incorrecta"
>abstract="MI identifica los problemas de configuración en la instancia de AEM"

`MI` (Problema de configuración incorrecta) Identifica problemas de configuración en la instancia de AEM.

Los subtipos se utilizan para identificar los diferentes tipos de información, como:

* `sling.job.max.parallel`: identifique los trabajos de Sling en los que la configuración paralela máxima está establecida en -1.
* `missing.maintenance.configuration`: identifique las configuraciones de tareas de mantenimiento que faltan.

## Posibles implicaciones y riesgos {#implications-and-risks}

* `sling.job.max.parallel`
   * Un valor -1 se sustituye por el número de procesadores disponibles. AEM Como tal, puede causar problemas de rendimiento en una instancia de.
* `missing.maintenance.configuration`
   * La falta de configuraciones de tarea de mantenimiento puede causar pérdida de rendimiento o daños en la instancia.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Directrices de implementación"
>abstract="Póngase en contacto con el Servicio de atención al cliente para obtener ayuda."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* `sling.job.max.parallel`
   * Adobe recomienda establecer el valor en 0,5 para aprovechar la mitad de los procesadores disponibles.
* `missing.maintenance.configuration`
   * Limpieza de revisión: Consulte [Limpieza de revisión](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup). La parte importante con respecto a la configuración es esta: [Limpieza de revisión: configuración de cola y compactación completa](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup).
   * Limpieza de binarios de Lucene: consulte [Panel de operaciones: limpieza de binarios de Lucene](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/sites/administering/operations/operations-dashboard#lucene-binaries-cleanup).
   * Recopilación de datos desechables del almacén de datos: consulte [Recopilación de datos desechables del almacén de datos](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/sites/administering/operations/data-store-garbage-collection).
   * Depuración del flujo de trabajo: consulte [Depuración regular de instancias de flujo de trabajo](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/sites/administering/operations/workflows-administering#regular-purging-of-workflow-instances).
   * Tarea de mantenimiento del registro de auditoría: consulte [Mantenimiento del registro de auditoría](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/sites/administering/operations/operations-audit-log).
* Póngase en contacto con el [equipo de servicio de atención al cliente de Experience Manager](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclarar sus dudas o resolver sus problemas.
