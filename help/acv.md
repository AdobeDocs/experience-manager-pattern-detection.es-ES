---
title: ACV
description: Página de ayuda de código de Pattern Detector
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
source-git-commit: d61fbb28fdf91fd9b356654d5cd2d50b156398c4
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---

# ACV {#acv}

Validador de contenido de recursos

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Validador de contenido de recursos"
>abstract="ACV identifica los nodos obligatorios que faltan en el contenido de los recursos."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html" text="Cambios importantes: Experience Manager como Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=es" text="Experience Manager como Cloud Service: Notas de la versión"

`ACV`  El validador de contenido de Assets identifica los nodos obligatorios que faltan en el contenido del recurso. Esto podría provocar un error en ciertas funciones de Assets en el Experience Manager como Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de información, como:

* `assets.sanity.missing.jcrcontent`: Identifique las carpetas con nodos obligatorios que faltan en el repositorio. La identificación de cualquier contenido que falte en el repositorio ayuda a evitar que se rompan las funciones o los casos de uso.

## Posibles implicaciones y riesgos {#implications-and-risks}

Esto podría provocar un error en ciertas funciones de Assets que dependen de propiedades heredadas en Experience Manager como Cloud Service.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Directrices de implementación"
>abstract="Adobe recomienda revisar la estructura del contenido para evitar flujos de trabajo rotos que dependen de propiedades heredadas. Póngase en contacto con el Servicio de atención al cliente para obtener ayuda&quot;.
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"

* Analice una carpeta si falta un nodo secundario. Cree los nodos manualmente si el número de carpetas es manejable; de lo contrario, utilice una secuencia de comandos.
* Póngase en contacto con nuestro [equipo de atención al cliente de Experience Manager](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar sus problemas.
