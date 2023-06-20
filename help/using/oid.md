---
title: OID
description: Página de ayuda de código del detector de patrones
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: d3e518cf8ad53a2cd28d4eea7f9b75c672881507
workflow-type: ht
source-wordcount: '485'
ht-degree: 100%

---

# OID {#oid}

Definición de índice de Oak

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Definición de índice de Oak"
>abstract="OID identifica los problemas relacionados con las definiciones de índices de Oak. Identifica las modificaciones que se han realizado en las definiciones de índice estándar de Oak. También identifica definiciones de índice de Oak personalizadas que son incompatibles con AEM as a Cloud Service. El mensaje para cada búsqueda de OID identificará el índice y proporcionará información adicional."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=es#how-to-use" text="Directrices de indexación de contenido"

`OID` identifica los problemas relacionados con las definiciones de índices de Oak. Identifica las modificaciones que se han realizado en las definiciones de índice estándar de Oak. También identifica definiciones de índice de Oak personalizadas que son incompatibles con AEM as a Cloud Service. El mensaje para cada hallazgo de `OID` identificará el índice y proporcionará información adicional.

Los subtipos se utilizan para identificar los diferentes tipos de información:

* `index.rule.violation`: una incompatibilidad de índice de Oak personalizada con AEM as a Cloud Service
* `standard.index.modification`: una modificación a un índice de Oak estándar.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar todos los índices personalizados y restringir según las directrices de indexación de contenido. Aproveche el conversor de índices para migrar las definiciones de índices personalizadas de Oak existentes a la definición de índices Oak personalizada y compatible de AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=es#oak-indexes" text="Directrices de paquetes"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html?lang=es#refactoring-tools" text="Conversor de índices"

* Las modificaciones en las definiciones de índices estándar de Oak pueden perderse durante una actualización de AEM.
* Las definiciones de Oak son inmutables, deben empaquetarse con el código de proyecto del cliente y solo deben implementarse mediante Cloud Manager.
* Todas las definiciones de índices de Oak deben seguir la convención de nomenclatura y otras reglas para índices de Oak en AEM as a Cloud Service. Aquellas que no lo hagan pueden causar un comportamiento no deseado.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Herramientas y recursos"
>abstract="Revise el proyecto de WKND heredado para comprender cómo se pueden resolver las infracciones de OID en su proyecto. Además, revise el ejemplo de infracción de OID en Github para comprender cómo se pueden convertir los índices heredados con la herramienta Conversor de índices y cómo se pueden hacer compatibles con AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="Proyecto de WKND heredado"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Ejemplo de infracción de OID: Github"

* Resuelva las infracciones de reglas de índice identificadas en el mensaje.
* Siga las [directrices de embalaje](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=es) de AEM as a Cloud Service para implementar definiciones de índice de Oak nuevas o personalizadas.
* Los índices estándar de AEM personalizados y las nuevas definiciones de índices de Oak personalizadas deben seguir las [directrices de indexación de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=es#preparing-the-new-index-definition) para AEM as a Cloud Service.
* Consulte el proyecto de [WKND heredado](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) y comprenda cómo las [infracciones de OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) pueden corregirse y hacerse compatibles con AEM as a Cloud Service.
* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
* Aproveche el [Conversor de índices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html?lang=es#refactoring-tools) para migrar las definiciones de índice de Oak personalizadas existentes a definiciones de índice de Oak personalizadas compatibles con AEM as a Cloud Service.
