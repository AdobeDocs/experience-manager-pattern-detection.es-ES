---
title: CTEM
description: Página de ayuda de código del detector de patrones
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 9a993a5cf078e5bc61cb5d314d2a15abcbd33f2a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# CTEM {#ctem}

Plantilla personalizada

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Plantilla personalizada"
>abstract="CTEM identifica los componentes personalizados que se han instalado en AEM. Esta información se proporciona a los efectos de la evaluación de las prácticas recomendadas"

`CTEM` identifica las plantillas personalizadas que se han instalado en AEM. Esta información se proporciona a los efectos de la evaluación de las prácticas recomendadas.

Las plantillas se identifican con un valor de tipo principal &quot;cq:Template&quot;. Con este código se utiliza un subtipo para identificar la categoría de la plantilla:

* `custom.editable.template`: la ruta de la plantilla no comienza con &quot;/apps&quot;.
* `custom.static.template`: La ruta de la plantilla comienza con &quot;/apps&quot;.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es mover todas las plantillas estáticas a plantillas editables. Los clientes pueden aprovechar las herramientas de modernización AEM existentes para migrar plantillas estáticas a plantillas editables."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=es" text="Plantillas editables"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Herramientas de modernización de AEM"

* Una práctica recomendada es mover todas las plantillas estáticas a plantillas editables.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Herramientas y recursos"
>abstract="Con la ayuda de AEM Modernización Suite, los clientes pueden manipular la estructura de una página desde una definición estática hasta una plantilla editable. La intención es ayudar a los clientes a pasar de las capacidades limitadas de las funciones heredadas a las opciones de AEM modernas y robustas. Estas herramientas son configurables, tienen en cuenta la configuración y son ampliables. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/structure/about.html" text="Conversor de estructura de página"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Aproveche las [Herramientas de modernización AEM](https://opensource.adobe.com/aem-modernize-tools/) para migrar plantillas estáticas a plantillas editables.
* Para obtener más información sobre las plantillas editables, consulte [Plantillas](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=es).
* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
