---
title: LUI
description: Página de ayuda de código del detector de patrones
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: ht
source-wordcount: '554'
ht-degree: 100%

---

# LUI {#lui}

Interfaz de usuario heredada

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Interfaz de usuario heredada"
>abstract="LUI identifica el uso de elementos de interfaz de usuario obsoletos que no se recomiendan o no se admiten en versiones posteriores de AEM y en AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=es" text="Cambios importantes en AEM as a Cloud Service"

`LUI` identifica el uso de elementos de interfaz de usuario obsoletos que no se recomiendan o no se admiten en versiones posteriores de AEM y en AEM as a Cloud Service.

Los subtipos se utilizan para identificar los diferentes tipos de elementos de la interfaz de usuario que deberían o deben actualizarse:

* `legacy.dialog.classic`: los cuadros de diálogo de la IU clásica basados en ExtJS deben cambiarse a Coral.
   * Esto se detecta cuando el nombre del cuadro de diálogo es “dialog” o “design_dialog” y cuando el valor de propiedad `jcr:primaryType` o `xtype` es “cq:Dialog”.
* `legacy.dialog.coral2`: los cuadros de diálogo de Coral 2 deben actualizarse para utilizar Coral 3.
   * Esto se detecta cuando el cuadro de diálogo y sus nombres de nodo de contenido secundario son “cq:dialog/content”,
“cq:design_dialog/content”, “cq:dialog.coral2/content” o “cq:design_dialog.coral2/content”
y el valor de la propiedad no contiene `sling:resourceType`
“granite/ui/components/coral/foundation”.
* `legacy.custom.component`: componentes que heredan de `foundation/components`, deben actualizarse para usar los componentes principales.
   * Esto se detectará cuando el valor de propiedad `jcr:primaryType` sea “cq:Component” y el
      valor de propiedad `sling:resourceSuperType` contiene “foundation/components” o cualquiera de los
      valores de propiedad `sling:resourceSuperType` de la cadena de componentes de supertipo contienen “foundation/components”.
* `legacy.static.template`: las plantillas estáticas deben actualizarse a plantillas editables.
   * Esto se detectará cuando el valor de propiedad `jcr:primaryType` sea “cq:Template”.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Directrices de implementación"
>abstract="La IU clásica ya no está disponible en AEM as a Cloud Service y la interfaz estándar para la creación es la IU táctil. La práctica recomendada es mover todas las interfaces no admitidas, y las personalizaciones vinculadas deben refactorizarse a funciones/capacidades más nuevas compatibles con AEM as a Cloud Service. Los clientes pueden aprovechar el conjunto de modernización de AEM existente para ayudar a reducir el esfuerzo necesario para modernizar las implementaciones de AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Herramientas de modernización de AEM"

* La IU clásica ya no está disponible en AEM as a Cloud Service. La interfaz estándar para la creación es la IU táctil.
* El uso de componentes personalizados heredados puede aumentar los costes de mantenimiento a lo largo del tiempo.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Herramientas y recursos"
>abstract="Con la ayuda del conjunto de modernización de AEM, los clientes pueden convertir los cuadros de diálogo clásicos (ExtJS) a cuadros de diálogo de Coral. La intención es ayudar a los clientes a pasar de las funciones no admitidas o heredadas a las opciones de AEM modernas y robustas. Estas herramientas son configurables, tienen en cuenta la configuración y son ampliables. Además, explore la sustitución de componentes personalizados por un conjunto de componentes principales estandarizados para acelerar el tiempo de desarrollo y reducir el coste de mantenimiento de sus aplicaciones."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/component.html" text="Conversor de componentes"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=es" text="Componentes principales"

* Utilice el [Conjunto de herramientas de modernización de AEM](https://opensource.adobe.com/aem-modernize-tools/) para reducir los esfuerzos necesarios para modernizar las implementaciones de AEM Sites. Estas herramientas incluyen la conversión de:
   * Cuadros de diálogo clásicos (ExtJS) a Coral
   * Componentes básicos a principales
   * Plantillas estáticas y control de columna a plantillas editables y cuadrícula adaptable
   * Diseños y cuadros de diálogo de diseño a políticas de plantilla editables
* Revise la biblioteca de componentes personalizados del proyecto y la transición, si es posible, al conjunto de [Componentes principales](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=es) para acelerar el tiempo de desarrollo y reducir el coste de mantenimiento de sus aplicaciones.
* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
