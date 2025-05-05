---
title: CTEM
description: Página de ayuda de código del detector de patrones.
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 100%

---

# CTEM {#ctem}

Plantilla personalizada

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Plantilla personalizada"
>abstract="CTEM identifica los componentes personalizados que están instalados en AEM. Esta información se proporciona a los efectos de la evaluación de las prácticas recomendadas"

`CTEM`  Identifica las plantillas personalizadas que están instaladas en AEM. Esta información se proporciona a los efectos de la evaluación de las prácticas recomendadas.

Las plantillas tienen un valor de tipo principal de `cq:Template`, que ayuda a identificarlas. Con este código se utiliza un subtipo para identificar la categoría de la plantilla:

* `custom.editable.template`: La ruta de la plantilla no comienza con `/apps`.
* `custom.static.template`: La ruta de la plantilla comienza con `/apps`.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es mover todas las plantillas estáticas a plantillas editables. Los clientes pueden utilizar las herramientas de modernización de AEM existentes para migrar las plantillas estáticas a plantillas editables."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/templates/templates" text="Plantillas editables"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Herramientas de modernización de AEM"

* Una práctica recomendada es mover todas las plantillas estáticas a plantillas editables.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Herramientas y recursos"
>abstract="Con la ayuda de AEM Modernización Suite, los clientes pueden manipular la estructura de una página desde una definición estática hasta una plantilla editable. La intención es ayudar a los clientes a pasar de las capacidades limitadas de las funciones heredadas a las opciones de AEM modernas y robustas. Estas herramientas son configurables, tienen en cuenta la configuración y son ampliables. Póngase en contacto con el equipo de soporte de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/structure/about.html" text="Conversor de estructura de página"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Utilice las [Herramientas de modernización de AEM](https://opensource.adobe.com/aem-modernize-tools/) para migrar plantillas estáticas a plantillas editables.
* Para obtener más información sobre las plantillas editables, consulte [Plantillas](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/developing/platform/templates/templates).
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclarar sus dudas o resolver sus problemas.
