---
title: ACV
description: Página de ayuda de código del detector de patrones
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 301aef7e53e94eb5941691450b3f1192408f2c6b
workflow-type: ht
source-wordcount: '274'
ht-degree: 100%

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

`ACV` El validador de contenido de Assets identifica los nodos obligatorios que faltan en el contenido del recurso. Esto podría provocar un error en ciertas funciones de Assets en Experience Manager as a Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de información, como:

* `missing.jcrcontent`: identifique las carpetas con nodos obligatorios que faltan en el repositorio. La identificación de cualquier contenido que falte en el repositorio ayuda a evitar que se rompan las funciones o los casos de uso.
* `missing.original.rendition`: identifique los recursos con la representación original obligatoria que falta en el repositorio.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Esto podría provocar un error en ciertas funciones de Assets que dependen de propiedades heredadas en Experience Manager as a Cloud Service.
* AEM Assets depende de la existencia de la representación original. El procesamiento de recursos en Cloud Service irá en bucle si falta la representación original.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Directrices de implementación"
>abstract="Adobe recomienda revisar la estructura del contenido para evitar flujos de trabajo rotos que dependen de propiedades heredadas. Póngase en contacto con el Servicio de atención al cliente para obtener ayuda."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Analice una carpeta si falta un nodo secundario. Cree los nodos manualmente si el número de carpetas es manejable; de lo contrario, utilice una secuencia de comandos.
* Para los activos que no tengan la representación original, vuelva a cargarlos o elimínelos antes de migrar.
* Póngase en contacto con nuestro [Equipo de servicio de atención al cliente de Experience Manager](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
