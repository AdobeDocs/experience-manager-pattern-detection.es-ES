---
title: LUI
description: Página de ayuda de código de Pattern Detector.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 58%

---

# LUI {#lui}

Interfaz de usuario heredada

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Interfaz de usuario heredada"
>abstract="LUI identifica el uso de elementos de interfaz de usuario obsoletos que no se recomiendan o no se admiten en versiones posteriores de AEM y en AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Cambios importantes en AEM as a Cloud Service"

LUI identifica el uso de elementos de interfaz de usuario obsoletos que no se recomiendan o no se admiten en versiones posteriores de AEM y en AEM as a Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de elementos de la interfaz de usuario que deberían o deben actualizarse:

* `legacy.dialog.classic`: los cuadros de diálogo de la IU clásica basados en ExtJS deben cambiarse a Coral.
   * Esto se detecta cuando el nombre del cuadro de diálogo es &quot;dialog&quot; o &quot;design_dialog&quot; y cuando la variable `jcr:primaryType` valor de propiedad para `xtype` el valor de propiedad es `cq:Dialog`.
* `legacy.dialog.coral2`: `Coral 2` los cuadros de diálogo deben actualizarse para utilizar `Coral 3`.
   * Esto se detectará cuando el cuadro de diálogo y sus nombres de nodo de contenido secundario estén `cq:dialog/content`,
     `cq:design_dialog/content`, `cq:dialog.coral2/content`&quot;, o `cq:design_dialog.coral2/content`
y el `sling:resourceType` el valor de la propiedad no contiene granite/ui/components/coral/foundation.
* `legacy.custom.component`: los componentes que heredan de `foundation/components`, deben actualizarse para usar los componentes principales.
   * Esto se detecta cuando el `jcr:primaryType` el valor de propiedad es &quot;`cq:Component`&quot; y el
     `sling:resourceSuperType` valor de propiedad contiene &quot;foundation/components&quot;. O bien, cualquiera de los
     valores de propiedad `sling:resourceSuperType` de la cadena de componentes de supertipo contienen “foundation/components”.
* `legacy.static.template`: las plantillas estáticas deben actualizarse a plantillas editables.
   * Esto se detecta cuando el `jcr:primaryType` el valor de propiedad es &quot;`cq:Template`&quot;.
* `content.fragment.template`: las plantillas de fragmento de contenido deben crear modelos de fragmento para reemplazar las plantillas de fragmento.
   * Las plantillas de fragmento de contenido se encuentran en las siguientes ubicaciones:
      * Las plantillas de fragmento de contenido listas para usar se almacenan en `/libs/settings/dam/cfm/templates`
      * Pueden superponerse en  `/apps/settings/dam/cfm/templates`  o  `/conf/.../settings/dam/cfm/templates`(... = global o “tenant”)
* `translation.dictionary`: `I18n` diccionario que está presente en /apps.
   * /apps es inmutable en tiempo de ejecución y translator.html ya no estaría disponible en AEM as a cloud service.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Directrices de implementación"
>abstract="La IU clásica ya no está disponible en AEM as a Cloud Service y la interfaz estándar para la creación es la IU táctil. AEM Una práctica recomendada es mover todas las interfaces no admitidas, y las personalizaciones vinculadas deben refactorizarse a funciones/capacidades más nuevas compatibles con las as a Cloud Service de la. AEM Los clientes pueden utilizar el grupo de modernización de la aplicación existente para ayudar a reducir el esfuerzo necesario para modernizar las implementaciones de AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Herramientas de modernización de AEM"

* La IU clásica ya no está disponible en AEM as a Cloud Service. La interfaz estándar para la creación es la IU táctil.
* El uso de componentes personalizados heredados puede aumentar los costes de mantenimiento a lo largo del tiempo.
* AEM Las plantillas de fragmento de contenido fueron reemplazadas por los modelos de fragmento de contenido en la versión 6.3 de la. AEM La migración de fragmentos de contenido basados en plantillas heredadas para que se mantengan as a Cloud Service conserva estos fragmentos como funcionales, pero no es posible crear fragmentos basados en plantillas heredadas. AEM Tampoco es posible distribuir estos fragmentos mediante GraphQL, que requiere modelos de fragmento de contenido como esquemas.
* /apps es inmutable en tiempo de ejecución y translator.html ya no estaría disponible en AEM as a cloud service. Por lo tanto, `I18n` Los diccionarios deben proceder de Git a través de la canalización CI/CD.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Herramientas y recursos"
>abstract="Con la ayuda del conjunto de modernización de AEM, los clientes pueden convertir los cuadros de diálogo clásicos (ExtJS) a cuadros de diálogo de Coral. La intención es ayudar a los clientes a pasar de las funciones no admitidas o heredadas a las opciones de AEM modernas y robustas. Estas herramientas son configurables, tienen en cuenta la configuración y son ampliables. Además, explore la sustitución de componentes personalizados por un conjunto de componentes principales estandarizados para acelerar el tiempo de desarrollo y reducir el coste de mantenimiento de sus aplicaciones."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Conversor de componentes"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-core-components/using/introduction" text="Componentes principales"

* Para reducir los esfuerzos necesarios para modernizar las implementaciones de AEM Sites, utilice [AEM Conjunto de herramientas de modernización de](https://opensource.adobe.com/aem-modernize-tools/). Estas herramientas incluyen la conversión de:
   * Cuadros de diálogo clásicos (ExtJS) a Coral
   * Componentes básicos a principales
   * Plantillas estáticas y control de columna a plantillas editables y cuadrícula adaptable
   * Diseños y cuadros de diálogo de diseño a políticas de plantilla editables
* Revise la biblioteca de componentes personalizados del proyecto y la transición, si es posible, al conjunto de [Componentes principales](https://experienceleague.adobe.com/es/docs/experience-manager-core-components/using/introduction) para acelerar el tiempo de desarrollo y reducir el coste de mantenimiento de sus aplicaciones.
* Cree modelos de fragmento de contenido con capacidades equivalentes a las plantillas heredadas y utilice esos modelos para la creación de fragmentos de contenido en el futuro. Consulte [Modelos de fragmento de contenido](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models) para obtener más información.
* `I18n` Los diccionarios deben proceder de Git a través de la canalización CI/CD. [Documentación](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclaraciones o para que se aborden las preocupaciones.
