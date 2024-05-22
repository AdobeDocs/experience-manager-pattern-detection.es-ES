---
title: CCOM
description: Página de ayuda de código del detector de patrones.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: ht
source-wordcount: '226'
ht-degree: 100%

---

# CCOM {#ccom}

Componente personalizado

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Componente personalizado"
>abstract="CCOM identifica los componentes personalizados que están instalados en AEM. Esta información se proporciona a los efectos de la evaluación de las prácticas recomendadas"

`CCOM` Identifica los componentes personalizados que están instalados en AEM. Esta información se proporciona a los efectos de la evaluación de las prácticas recomendadas.

Se utiliza un subtipo con este código para identificar la categoría del componente:

* `custom.core`: un supertipo de la cadena de supertipos del componente contiene `core/wcm/components/`, lo que indica que se hereda de un componente principal.
* `custom.foundation`: un supertipo de la cadena de supertipos del componente contiene `core/wcm/components/`, lo que indica que se hereda de un componente principal.
* `custom.overlay.foundation`: la ruta del componente contiene `wcm/foundation/components/` o `foundation/components/`, lo que indica que se superpone a un componente de base.
* `custom`: el componente personalizado no hereda ni superpone un componente principal o base.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La práctica recomendada consiste en minimizar el número de componentes personalizados, utilizar los componentes principales y utilizarlos con el sistema de estilos para reducir la deuda técnica.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Directrices de implementación"
>abstract="La práctica recomendada consiste en minimizar el número de componentes personalizados, utilizar los componentes principales y utilizarlos con el sistema de estilos para reducir la deuda técnica."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-core-components/using/introduction" text="Componentes principales"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring" text="Sistema de estilos"

* Para obtener más información acerca de los componentes principales, consulte [Introducción a los componentes principales](https://experienceleague.adobe.com/es/docs/experience-manager-core-components/using/introduction).
* Para obtener más información sobre el sistema de estilos, visite [Uso del sistema de estilos](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring).
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
