---
title: DM
description: Obtenga información sobre cómo el código del detector de patrones identifica el uso de AEM Assets - Dynamic Media.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '173'
ht-degree: 100%

---

# DM {#dm}

Dynamic Media

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="El código DM identifica el uso de AEM Assets Dynamic Media en la implementación actual. El modo Dynamic Media se detecta mediante el modo de ejecución."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="Desarrollo de AEM: directrices y prácticas recomendadas"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Directrices de desarrollo de AEM as a Cloud Service"

`DM` (Dynamic Media) Identifica el uso de AEM Assets Dynamic Media. El modo de Dynamic Media se detecta mediante el modo de ejecución.

Se utiliza un subtipo con este código:

* `dynamic.media.runmode`: El valor asociado de este subtipo, si se proporciona, es:
   * `dynamicmedia`: Dynamic Media, modo híbrido
   * `dynamicmedia_scene7`: Dynamic Media, modo Scene7

## Posibles implicaciones y riesgos {#implications-and-risks}

* `dynamic.media.runmode`
   * Puede haber problemas de actualización relacionados con Dynamic Media.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Directrices de implementación"
>abstract="AEM as a Cloud Service solo admite el modo de ejecución dynamicmedia_scene7. Revise la configuración actual y póngase en contacto con el equipo de soporte de Adobe para obtener ayuda y aclaraciones."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Configuración de Dynamic Media"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"


* `dynamic.media.runmode`
   * Encuentre más información en la [Configuración de Dynamic Media](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media).

* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
