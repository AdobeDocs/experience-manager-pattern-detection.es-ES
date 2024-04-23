---
title: CTEM
description: Página de ayuda de código de Pattern Detector.
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 68%

---

# CTEM {#ctem}

Plantilla personalizada

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Plantilla personalizada"
>abstract="CTEM identifica los componentes personalizados que se han instalado en AEM. Esta información se proporciona a los efectos de la evaluación de las prácticas recomendadas"

AEM CTEM identifica las plantillas personalizadas que se han instalado en las plantillas de la aplicación de la plataforma de datos de. Esta información se proporciona a los efectos de la evaluación de las prácticas recomendadas.

Las plantillas se identifican con un valor de tipo principal de `cq:Template`. Con este código se utiliza un subtipo para identificar la categoría de la plantilla:

* `custom.editable.template`: la ruta de la plantilla no comienza con &quot;/apps&quot;.
* `custom.static.template`: La ruta de la plantilla comienza con &quot;/apps&quot;.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es mover todas las plantillas estáticas a plantillas editables. AEM Los clientes pueden utilizar las herramientas de modernización de la existentes para migrar plantillas estáticas a plantillas editables."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates" text="Plantillas editables"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Herramientas de modernización de AEM"

* Una práctica recomendada es mover todas las plantillas estáticas a plantillas editables.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Herramientas y recursos"
>abstract="Con la ayuda de AEM Modernización Suite, los clientes pueden manipular la estructura de una página desde una definición estática hasta una plantilla editable. La intención es ayudar a los clientes a pasar de las capacidades limitadas de las funciones heredadas a las opciones de AEM modernas y robustas. Estas herramientas son configurables, tienen en cuenta la configuración y son ampliables. Póngase en contacto con el Soporte técnico de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/structure/about.html" text="Conversor de estructura de página"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Utilice el [AEM Herramientas de modernización de](https://opensource.adobe.com/aem-modernize-tools/) para migrar plantillas estáticas a plantillas editables.
* Para obtener más información sobre las plantillas editables, consulte [Plantillas](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates).
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclaraciones o para que se aborden las preocupaciones.
