---
title: LUI
description: Página de ayuda de código del detector de patrones.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '703'
ht-degree: 100%

---

# LUI {#lui}

Interfaz de usuario heredada

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Interfaz de usuario heredada"
>abstract="LUI identifica el uso de elementos de interfaz de usuario obsoletos que no se recomiendan o no se admiten en versiones posteriores de AEM y en AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Cambios importantes en AEM as a Cloud Service"

`LUI` Identifica el uso de elementos de interfaz de usuario obsoletos que no se recomiendan o no se admiten en versiones posteriores de AEM y en AEM as a Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de elementos de la interfaz de usuario que deberían o deben actualizarse:

* `legacy.dialog.classic`: los cuadros de diálogo de la IU clásica basados en ExtJS deben cambiarse a Coral.
   * Esto se detecta cuando el nombre del cuadro de diálogo es “dialog” o “design_dialog” y cuando 
el valor de la propiedad `jcr:primaryType` o el valor de la propiedad `xtype` es `cq:Dialog`.
* `legacy.dialog.coral2`: los cuadros de diálogo de `Coral 2` deben actualizarse para que usen `Coral 3`.
   * Esto se detecta cuando el cuadro de diálogo y los nombres de sus nodos de contenido secundarios son `cq:dialog/content`,
     `cq:design_dialog/content`, `cq:dialog.coral2/content` o `cq:design_dialog.coral2/content` 
y el valor de la propiedad `sling:resourceType` no contiene
&quot;granite/ui/components/coral/foundation&quot;.
* `legacy.custom.component`: los componentes que se heredan de `foundation/components`, deben actualizarse para poder usar los componentes principales.
   * Esto se detecta cuando el valor de propiedad `jcr:primaryType` es &quot;`cq:Component`&quot; y el
     valor de la propiedad `sling:resourceSuperType` contiene &quot;foundation/components&quot;. O cualquiera de los
     valores de propiedad `sling:resourceSuperType` de la cadena de componentes de supertipo contienen 
“foundation/components”.
* `legacy.static.template`: las plantillas estáticas deben actualizarse a plantillas editables.
   * Esto se detecta cuando el valor de propiedad `jcr:primaryType` es &quot;`cq:Template`&quot;.
* `content.fragment.template`: las plantillas de fragmento de contenido deben crear modelos de fragmento para reemplazar las plantillas de fragmento.
   * Las plantillas de fragmento de contenido se encuentran en las siguientes ubicaciones:
      * Las plantillas de fragmento de contenido listas para usar se almacenan en `/libs/settings/dam/cfm/templates`
      * Pueden superponerse en  `/apps/settings/dam/cfm/templates`  o  `/conf/.../settings/dam/cfm/templates`(... = global o “tenant”)
* `translation.dictionary`: el diccionario `I18n` que está en /apps.
   * /apps es inmutable en tiempo de ejecución y translator.html ya no estaría disponible en AEM as a cloud service.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Directrices de implementación"
>abstract="La IU clásica ya no está disponible en AEM as a Cloud Service y la interfaz estándar para la creación es la IU táctil. La práctica recomendada consiste en mover todas las interfaces no admitidas, y las personalizaciones vinculadas deben refactorizarse a funciones/capacidades más nuevas que son compatibles con AEM as a Cloud Service. Los clientes pueden utilizar AEM Modernization Suite para ayudar a reducir el esfuerzo necesario para modernizar las implementaciones de AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Herramientas de modernización de AEM"

* La IU clásica ya no está disponible en AEM as a Cloud Service. La interfaz estándar para la creación es la IU táctil.
* El uso de componentes personalizados heredados puede aumentar los costes de mantenimiento a lo largo del tiempo.
* Las plantillas de fragmento de contenido se reemplazaron por los modelos de fragmento de contenido de AEM 6.3. Al migrar los fragmentos de contenido basados en plantillas heredadas a AEM as a Cloud Service, estos fragmentos se conservan como funcionales, pero no se pueden crear nuevos basados en la plantilla heredada. Tampoco es posible distribuir estos fragmentos mediante AEM GraphQL, que necesita modelos de fragmento de contenido como esquemas.
* /apps es inmutable en tiempo de ejecución y translator.html ya no está disponible en AEM as a Cloud Service. Por consiguiente, los diccionarios `I18n` deben proceder de Git a través de la canalización CI/CD.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Herramientas y recursos"
>abstract="Con la ayuda del conjunto de modernización de AEM, los clientes pueden convertir los cuadros de diálogo clásicos (ExtJS) a cuadros de diálogo de Coral. La intención es ayudar a los clientes a pasar de las funciones no admitidas o heredadas a las opciones de AEM modernas y robustas. Estas herramientas son configurables, tienen en cuenta la configuración y son ampliables. Además, explore la sustitución de componentes personalizados por un conjunto de componentes principales estandarizados para acelerar el tiempo de desarrollo y reducir el coste de mantenimiento de sus aplicaciones."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Conversor de componentes"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-core-components/using/introduction" text="Componentes principales"

* Para reducir el esfuerzo necesario para modernizar sus implementaciones de AEM Sites, utilice las [herramientas de modernización de AEM](https://opensource.adobe.com/aem-modernize-tools/). Estas herramientas incluyen la conversión de:
   * Cuadros de diálogo clásicos (ExtJS) a Coral
   * Componentes básicos a principales
   * Plantillas estáticas y control de columna a plantillas editables y cuadrícula adaptable
   * Diseños y cuadros de diálogo de diseño a políticas de plantilla editables
* Revise la biblioteca de componentes personalizados del proyecto y la transición, si es posible, al conjunto de [Componentes principales](https://experienceleague.adobe.com/es/docs/experience-manager-core-components/using/introduction) para acelerar el tiempo de desarrollo y reducir el coste de mantenimiento de sus aplicaciones.
* Cree modelos de fragmentos de contenido con funciones equivalentes a las plantillas heredadas y utilice esos modelos para la creación de fragmentos de contenido en el futuro. Para obtener más información, consulte [Modelos de fragmentos de contenido](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models).
* Los diccionarios `I18n` deben proceder de Git a través de la canalización CI/CD. [Documentación](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
