---
title: MI
description: Página de ayuda de código del detector de patrones
source-git-commit: aa05ebcb54c6945a903c76add4f31e3279cd05b5
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 26%

---

# MI {#mi}

Problema de configuración incorrecta

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Problema de configuración incorrecta"
>abstract="AEM MI identifica los problemas de configuración en la instancia de"

`MI`  AEM Problema de configuración incorrecta identifica problemas de configuración en la instancia de.

Los subtipos se utilizan para identificar los diferentes tipos de información, como:

* `sling.job.max.parallel`: identifique los trabajos de sling en los que la configuración paralela máxima está establecida en -1.
* `missing.maintenance.configuration`: identifique las configuraciones de tareas de mantenimiento que faltan.

## Posibles implicaciones y riesgos {#implications-and-risks}

* `sling.job.max.parallel`
   * El valor -1 se sustituye por el número de procesadores disponibles. AEM Esto puede causar problemas de rendimiento en la instancia de la.
* `missing.maintenance.configuration`
   * La falta de configuraciones de tareas de mantenimiento puede causar pérdida de rendimiento o daños en la instancia.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Directrices de implementación"
>abstract="Póngase en contacto con el Servicio de atención al cliente para obtener ayuda."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* `sling.job.max.parallel`
   * Es aconsejable establecer el valor en 0,5 para disponer de la mitad de los procesadores disponibles.
* `missing.maintenance.configuration`
   * Limpieza de revisión: consulte [Limpieza de revisión](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html). La parte importante con respecto a la configuración es esta: [Limpieza de revisión: configurar cola y compactación completa](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html#how-to-configure-full-and-tail-compaction).
   * Limpieza de binarios de Lucene: consulte [Panel de operaciones - Limpieza de binarios de Lucene](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-dashboard.html#lucene-binaries-cleanup).
   * Recopilación de basura del almacén de datos: consulte [Recopilación de residuos del almacén de datos](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/data-store-garbage-collection.html).
   * Purga del flujo de trabajo: consulte [Depuración regular de instancias de flujo de trabajo](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/workflows-administering.html?lang=es#regular-purging-of-workflow-instances).
   * Tarea de mantenimiento de AuditLog: consulte [Mantenimiento del registro de auditoría](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-audit-log.html).
* Póngase en contacto con nuestro [Equipo de servicio de atención al cliente de Experience Manager](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.