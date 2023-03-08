---
title: ACV
description: Página de ayuda de código del detector de patrones
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: bbeb7193e198a32a9bc966e1821b1058dbbc8c02
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 81%

---

# ACV {#acv}

Validador de contenido de Assets

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Validador de contenido de Assets"
>abstract="ACV identifica los nodos obligatorios que faltan en el contenido de los recursos."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html?lang=es" text="Cambios importantes: Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=es" text="Experience Manager as a Cloud Service: notas de la versión"

El validador de contenido de Assets `ACV` identifica los nodos obligatorios que faltan en el contenido del recurso, así como los posibles incumplimientos. Esto podría provocar un error en ciertas funciones de Assets en Experience Manager as a Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de información, como:

* `missing.jcrcontent`: identifique las carpetas con nodos obligatorios que faltan en el repositorio. La identificación de cualquier contenido que falte en el repositorio ayuda a evitar que se rompan las funciones o los casos de uso.
* `missing.original.rendition`: identifique los archivos con la representación original obligatoria que falta en el repositorio. Tenga en cuenta que la previsualización de las páginas del PDF no requiere la generación de subarchivos en AEMaaCS. Por lo tanto, para los archivos del PDF, se suprimen los subarchivos de creación de informes que no tengan representación original.
* `metadata.descendants.violation`: identifique los recursos con más de 100 descendientes bajo el nodo de metadatos del recurso en el repositorio.
* `conflict.node`: Identifique la presencia de nodos de conflicto en el repositorio bajo la ruta /content/dam/.
* `psb.file.large`: identifique archivos PSB grandes (dc:format : application/vnd.3gpp.pic-bw-small) con un tamaño bueno a 2 gigabytes.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Esto podría provocar un error en ciertas funciones de Assets que dependen de propiedades heredadas en Experience Manager as a Cloud Service.
* AEM Assets depende de la existencia de la representación original. El procesamiento de archivos en Cloud Service irá en bucle si falta la representación original. La generación de subarchivos no es compatible con AEMaaCS.
* Un número elevado de descendientes bajo el nodo de metadatos puede ralentizar la carga de carpetas consistentes en recursos que infringen esto.
* La presencia de nodos de conflicto podría provocar un error de ingesta en AEM as a Cloud Service.
* Es posible que el Experience Manager no procese archivos PSB de muy alta resolución. Los clientes que utilizan ImageMagick para procesar archivos grandes pueden verse afectados por el rendimiento si no se realiza una evaluación comparativa adecuada del servidor Experience Manager.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Directrices de implementación"
>abstract="Adobe recomienda revisar la estructura del contenido para evitar flujos de trabajo rotos que dependen de propiedades heredadas. Póngase en contacto con el Servicio de atención al cliente para obtener ayuda."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Analice una carpeta si falta un nodo secundario. Cree los nodos manualmente si el número de carpetas es manejable; de lo contrario, utilice una secuencia de comandos.
* Para los activos que no tengan la representación original, vuelva a cargarlos o elimínelos antes de migrar.
* No se requiere ninguna acción para la representación original de los subarchivos que faltan.
* En caso de nodos de conflicto, deben resolverse o deben eliminarse antes de migrar a AEM as a Cloud Service.
* Póngase en contacto con Asistencia al cliente de Adobe si planea procesar muchos archivos de PSD o PSB grandes. Es posible que el Experience Manager no procese archivos PSB de muy alta resolución que tengan más de 30000 x 23000 píxeles. Consulte [documentación](https://experienceleague.adobe.com/docs/experience-manager-64/assets/extending/best-practices-for-imagemagick.html).
* Póngase en contacto con nuestro [Equipo de servicio de atención al cliente de Experience Manager](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
