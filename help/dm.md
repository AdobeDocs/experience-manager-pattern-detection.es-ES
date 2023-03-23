---
title: DM
description: Página de ayuda de código del detector de patrones
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 100%

---

# DM {#dm}

Dynamic Media

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="El código DM identifica el uso de AEM Assets Dynamic Media en la implementación actual. El modo Dynamic Media se detecta mediante el modo de ejecución."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=es" text="Desarrollo de AEM: directrices y prácticas recomendadas"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=es" text="Directrices de desarrollo de AEM as a Cloud Service"

`DM` identifica el uso de AEM Assets Dynamic Media. El modo Dynamic Media se detecta mediante el modo de ejecución.

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
>abstract="AEM as a Cloud Service solo admite dynamicmedia_scene7 runmode. Revise la configuración actual y póngase en contacto con el equipo de Soporte de Adobe para obtener ayuda y aclaraciones."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html?lang=es" text="Configuración de Dynamic Media"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"


* `dynamic.media.runmode`
   * Encuentre más información en la [Configuración de Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html?lang=es).

* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
