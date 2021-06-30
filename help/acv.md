---
title: ACV
description: Página de ayuda de código de Pattern Detector
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
source-git-commit: 57e33b97aba253bad62cf95dcca9ef6885d263e6
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# ACV {#acv}

Validador de contenido de recursos

## Fondo {#background}

>[!INFO]
>id=&quot;aemcloud_bpa_acv_overview&quot;
>title=&quot;Validador de contenido de recursos&quot;
>abstract=&quot;ACV identifica los nodos obligatorios que faltan en el contenido de los recursos&quot;.
>additional-url=&quot;https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html&quot; text=&quot;Cambios importantes: Experience Manager como Cloud Service&quot;
>additional-url=&quot;https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html&quot; text=&quot;Experience Manager como Cloud Service - Notas de la versión&quot;

`ACV`  El validador de contenido de Assets identifica los nodos obligatorios que faltan en el contenido del recurso. Esto podría provocar un error en ciertas funciones de Assets en el Experience Manager como Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de información, como:

* `assets.sanity.missing.jcrcontent`: Identifique las carpetas con nodos obligatorios que faltan en el repositorio. La identificación de cualquier contenido que falte en el repositorio ayuda a evitar que se rompan las funciones o los casos de uso.

## Posibles implicaciones y riesgos {#implications-and-risks}

Esto podría provocar un error en ciertas funciones de Assets que dependen de propiedades heredadas en Experience Manager como Cloud Service.

## Posibles soluciones {#solutions}

>[!INFO]
>id=&quot;aemcloud_bpa_acv_guide&quot;
>title=&quot;Guía de implementación&quot;
>abstract=&quot;Adobe recomienda revisar la estructura de contenido para evitar flujos de trabajo rotos que dependen de propiedades heredadas. Póngase en contacto con el Servicio de atención al cliente para obtener ayuda&quot;.
>additional-url=&quot;https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html&quot; text=&quot;Experience Cloud Support&quot;

* Analice una carpeta si falta un nodo secundario. Cree los nodos manualmente si el número de carpetas es manejable; de lo contrario, utilice una secuencia de comandos.
* Póngase en contacto con nuestro [equipo de atención al cliente de Experience Manager](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar sus problemas.
