---
title: CCOM
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# CCOM {#ccom}

Componente personalizado

## Fondo {#background}

`CCOM` identifica los componentes personalizados que se han instalado en AEM. Esta información se proporciona a los efectos de la evaluación de las prácticas recomendadas.

Se utiliza un subtipo con este código para identificar la categoría del componente:

* `custom.core`: Un supertipo de la cadena de supertipos del componente contiene &quot;core/wcm/components/&quot;, lo que indica que se hereda de un componente principal.
* `custom.foundation`: Un supertipo de la cadena de supertipos del componente contiene &quot;core/wcm/components/&quot;, lo que indica que se hereda de un componente principal.
* `custom.overlay.foundation`: La ruta del componente contiene &quot;wcm/foundation/components/&quot; o &quot;foundation/components/&quot;, lo que indica que se superpone a un componente de base.
* `custom`: El componente personalizado no hereda ni superpone un componente principal o base.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Una práctica recomendada es minimizar el número de componentes personalizados, aprovechar los componentes principales y utilizar componentes principales con el sistema de estilos para reducir la deuda técnica.

## Posibles soluciones {#solutions}

* Encontrará más información sobre los componentes principales en [Introducción a los componentes principales](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=es).
* Encontrará más información sobre el sistema de estilos en [Uso del sistema de estilos](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring).
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
