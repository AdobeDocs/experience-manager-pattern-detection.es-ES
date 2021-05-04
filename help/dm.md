---
title: DM
description: Página de ayuda de código de Pattern Detector
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 7%

---

# DM {#dm}

Dynamic Media

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="El código DM identifica el uso de AEM Assets Dynamic Media en la implementación actual. El modo Dynamic Media se detecta mediante el modo de ejecución."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html" text="Desarrollo de AEM: directrices y prácticas recomendadas"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="Directrices de desarrollo de AEM as a Cloud Service"

`DM` identifica el uso de AEM Assets Dynamic Media. El modo Dynamic Media se detecta mediante el modo de ejecución.

Se utiliza un subtipo con este código:

* `dynamic.media.runmode`: El valor asociado de este subtipo, si se proporciona, es:
   * `dynamicmedia`: Dynamic Media: modo híbrido
   * `dynamicmedia_scene7`: Dynamic Media: modo Scene7

## Posibles implicaciones y riesgos {#implications-and-risks}

* `dynamic.media.runmode`
   * Puede haber problemas de actualización relacionados con Dynamic Media.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Directrices de implementación"
>abstract="AEM como Cloud Service solo admite dynamic_media_scene7 runmode. Revise la configuración actual y póngase en contacto con el equipo de asistencia de Adobe para obtener ayuda y aclaraciones."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html" text="Configuración de Dynamic Media"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"


* `dynamic.media.runmode`
   * Encontrará más información en [Configuración de Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html).

* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
