---
title: LUI
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 4%

---


# LUI {#lui}

Interfaz de usuario heredada

## Fondo {#background}

`LUI` identifica el uso de elementos de interfaz de usuario obsoletos que no se recomiendan o no se admiten en versiones posteriores de AEM y en AEM como Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de elementos de la interfaz de usuario que deben actualizarse o deben actualizarse:

* `legacy.dialog.classic`: Los cuadros de diálogo de la IU clásica basados en ExtJS deben cambiarse a Coral.
   * Se detecta cuando el nombre del cuadro de diálogo es &quot;dialog&quot; o &quot;design_dialog&quot; y cuando
el valor de la propiedad `jcr:primaryType` o el valor de la propiedad `xtype` es &quot;cq:Dialog&quot;.
* `legacy.dialog.coral2`: Los cuadros de diálogo de Coral 2 deben actualizarse para utilizar Coral 3.
   * Esto se detecta cuando el cuadro de diálogo y sus nombres de nodo de contenido secundario son &quot;cq:dialog/content&quot;,
&quot;cq:design_dialog/content&quot;, &quot;cq:dialog.coral2/content&quot; o &quot;cq:design_dialog.coral2/content&quot;
y el valor de la propiedad `sling:resourceType` no contiene
&quot;granite/ui/components/coral/foundation&quot;.
* `legacy.custom.component`: Los componentes que heredan de  `foundation/components`, deben actualizarse para utilizar los componentes principales.
   * Esto se detecta cuando el valor de la propiedad `jcr:primaryType` es &quot;cq:Component&quot; y la variable
      `sling:resourceSuperType` el valor de propiedad contiene &quot;foundation/components&quot; o cualquiera de los
      `sling:resourceSuperType` los valores de propiedad de la cadena de componentes de supertipo contienen &quot;foundation/components&quot;.
* `legacy.static.template`: Las plantillas estáticas deben actualizarse a plantillas editables.
   * Esto se detecta cuando el valor de la propiedad `jcr:primaryType` es &quot;cq:Template&quot;.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La IU clásica ya no está disponible en AEM como Cloud Service. La interfaz estándar para la creación es la IU táctil.
* El uso de componentes personalizados heredados puede aumentar los costes de mantenimiento a lo largo del tiempo.

## Posibles soluciones {#solutions}

* Utilice [AEM Conjunto de herramientas de modernización](https://opensource.adobe.com/aem-modernize-tools/) para reducir el esfuerzo necesario para modernizar las implementaciones de AEM Sites. Estas herramientas incluyen la conversión de:
   * Diálogo clásico (ExtJS) con cuadros de diálogo de Coral
   * Componentes básicos a principales.
   * Plantillas estáticas y control de columna a plantillas editables y cuadrícula adaptable
   * Diseños y cuadros de diálogo de diseño para políticas de plantilla editables
* Revise la biblioteca de componentes personalizados del proyecto y la transición, si es posible, al conjunto estandarizado de [componentes principales](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=es) para acelerar el tiempo de desarrollo y reducir el coste de mantenimiento de las aplicaciones.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
