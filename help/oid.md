---
title: OID
description: Página de ayuda de código de Pattern Detector
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# OID {#oid}

Definición de índice Oak

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Definición de índice Oak"
>abstract="OID identifica los problemas relacionados con las definiciones de índices de Oak. Identifica las modificaciones que se han realizado en las definiciones de índice estándar de Oak. También identifica definiciones de índice Oak personalizadas que son incompatibles con AEM como Cloud Service. El mensaje para cada búsqueda de OID identificará el índice y proporcionará información adicional."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#how-to-use" text="Directrices de indexación de contenido"

`OID` identifica los problemas relacionados con las definiciones de índices de Oak. Identifica las modificaciones que se han realizado en las definiciones de índice estándar de Oak. También identifica definiciones de índice Oak personalizadas que son incompatibles con AEM como Cloud Service. El mensaje para cada búsqueda `OID` identificará el índice y proporcionará información adicional.

Los subtipos se utilizan para identificar los diferentes tipos de información:

* `custom.index.violation`: Una incompatibilidad de índice Oak personalizada con AEM como Cloud Service.
* `standard.index.modification`: Una modificación a un índice Oak estándar.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar todos los índices personalizados y restringir según las directrices de indexación de contenido. Aproveche el Conversor de índices para migrar las definiciones de índices personalizadas de Oak existentes a AEM como una definición de índice Oak personalizada compatible con el Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#oak-indexes" text="Directrices de paquetes"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools" text="Conversor de índices"

* Las modificaciones en las definiciones de índices estándar de Oak pueden perderse durante una actualización de AEM.
* Las definiciones de Oak son inmutables, deben empaquetarse con el código de proyecto del cliente y solo deben implementarse mediante Cloud Manager.
* Todas las definiciones de índices Oak deben seguir la convención de nombres y otras reglas para índices Oak en AEM como Cloud Service. Aquellos que no lo hagan pueden causar un comportamiento no deseado.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Herramientas y recursos"
>abstract="Revise el proyecto heredado de WKND para comprender cómo se pueden resolver las violaciones de OID en su proyecto. Revise también el ejemplo de infracción de OID en Github para comprender cómo se pueden convertir los índices heredados con la herramienta Conversor de índices y cómo se pueden hacer compatibles con AEM como Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="Proyecto WKND-Legacy"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Ejemplo de infracción de OID: Github"

* Resuelva las violaciones de reglas de índice identificadas en el mensaje.
* Siga AEM como un Cloud Service [de pautas de empaquetado](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) para implementar definiciones de índice Oak nuevas o personalizadas.
* Los índices estándar AEM personalizados y las nuevas definiciones de índice Oak personalizadas deben seguir las [directrices de indexación de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition) para AEM como Cloud Service.
* Revise el proyecto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) y comprenda cómo se pueden corregir las [infracciones de OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) y hacerlas compatibles con AEM como Cloud Service.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
* Aproveche el [Conversor de índices](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools) para migrar las definiciones de índice Oak personalizadas existentes a AEM como una definición de índice Oak personalizada compatible con Cloud Service.
