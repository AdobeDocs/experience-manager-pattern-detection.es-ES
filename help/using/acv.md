---
title: ACV
description: Página de ayuda de código del detector de patrones.
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 100%

---

# ACV {#acv}

Validador de contenido de Assets

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Validador de contenido de Assets"
>abstract="ACV identifica los nodos obligatorios que faltan en el contenido de los recursos."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/overview" text="Cambios importantes: Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Experience Manager as a Cloud Service: notas de la versión"

`ACV` (Validador de contenido de Assets) identifica los nodos obligatorios que faltan en el contenido del recurso, así como los posibles incumplimientos. Este tipo de cosas podría provocar un error en ciertas funciones de Assets en Experience Manager as a Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de información, como:

* `missing.jcrcontent`: identifique las carpetas con nodos obligatorios que faltan en el repositorio. La identificación de cualquier contenido que falte en el repositorio ayuda a evitar que se rompan las funciones o los casos de uso.
* `missing.original.rendition`: identifique los archivos con la representación original obligatoria que falta en el repositorio. La previsualización de las páginas del PDF no requiere la generación de subarchivos en AEMaaCS. Por lo tanto, para los recursos de PDF, se suprimen los recursos secundarios de creación de informes que no tengan representación original.
* `metadata.descendants.violation`: identifique los recursos con más de 100 descendientes bajo el nodo de metadatos del recurso en el repositorio.
* `conflict.node`: identifique la presencia de nodos de conflicto en el repositorio bajo la ruta /content/dam/.
* `psb.file.large`: identifique los archivos PSB grandes (`dc:format : application/vnd.3gpp.pic-bw-small`) con un tamaño superior a 2 GB.
* `invalid.asset.name`: identifique los recursos con caracteres no válidos[`* / : [ \ ] | # % { } ? &`] en el nombre.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Posiblemente provoque un error en ciertas funciones de Assets que dependen de propiedades heredadas en Experience Manager as a Cloud Service.
* AEM Assets depende de la existencia de la representación original. El procesamiento de recursos en Cloud Service va en bucle si falta la representación original. La generación de subarchivos no es compatible con AEMaaCS.
* Un número elevado de descendientes bajo un nodo de metadatos puede ralentizar la descarga de carpetas que contienen recursos incumplidores.
* La presencia de nodos de conflicto podría provocar un error de ingesta en AEM as a Cloud Service.
* Es posible que Experience Manager no procese archivos PSB de alta resolución. Los clientes que utilizan ImageMagick para procesar archivos grandes pueden verse afectados por el rendimiento si no se realiza una evaluación comparativa adecuada del servidor de Experience Manager.
* Los caracteres no válidos en el nombre del recurso podrían provocar errores al migrar a AEM as a Cloud Service.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Directrices de implementación"
>abstract="Adobe recomienda revisar la estructura del contenido para evitar que se rompan los flujos de trabajo que dependen de propiedades heredadas. Póngase en contacto con el Servicio de atención al cliente para obtener ayuda."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Analice una carpeta si falta un nodo secundario. Cree los nodos manualmente si el número de carpetas es manejable; de lo contrario, utilice una secuencia de comandos.
* Para los activos que no tengan la representación original, vuelva a cargarlos o elimínelos antes de migrar.
* No se requiere ninguna acción para la representación original de los recursos secundarios que faltan.
* En caso de nodos de conflicto, deben resolverse o deben eliminarse antes de migrar a AEM as a Cloud Service.
* Póngase en contacto con la Asistencia al cliente de Adobe si tiene previsto procesar muchos archivos PSD o PSB grandes. Es posible que Experience Manager no procese archivos PSB de alta resolución que tengan más de 30000 x 23000 píxeles. Consulte la [documentación](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/assets/extending/best-practices-for-imagemagick)
* Póngase en contacto con el [servicio de atención al cliente de Experience Manager](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclarar sus dudas o resolver sus problemas.
