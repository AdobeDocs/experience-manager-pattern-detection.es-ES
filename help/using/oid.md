---
title: OID
description: Página de ayuda de código de Pattern Detector.
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 50%

---

# OID {#oid}

Definición de índice de Oak

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Definición de índice de Oak"
>abstract="OID identifica los problemas relacionados con las definiciones de índices de Oak. Identifica las modificaciones que se han realizado en las definiciones de índice estándar de Oak. También identifica definiciones de índice de Oak personalizadas que son incompatibles con AEM as a Cloud Service. El mensaje para cada búsqueda de OID identifica el índice y proporciona información adicional."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing#how-to-use" text="Directrices de indexación de contenido"

OID identifica los problemas relacionados con las definiciones de índices de Oak. Identifica las modificaciones que se han realizado en las definiciones de índice estándar de Oak. También identifica definiciones de índice de Oak personalizadas que son incompatibles con AEM as a Cloud Service. El mensaje para cada `OID` La búsqueda de identifica el índice y proporciona información adicional.

Los subtipos se utilizan para identificar los diferentes tipos de información:

* `index.rule.violation`: una incompatibilidad de índice de Oak personalizada con AEM as a Cloud Service
* `standard.index.modification`: una modificación a un índice de Oak estándar.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar todos los índices personalizados y reestructurarlos según las directrices de indexación de contenido. AEM Utilice el Conversor de índices para migrar las definiciones de índice de Oak personalizadas existentes a definiciones de índice de Oak personalizadas compatibles con el as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#oak-indexes" text="Directrices de paquetes"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools" text="Conversor de índices"

* Las modificaciones en las definiciones de índices estándar de Oak pueden perderse durante una actualización de AEM.
* Las definiciones de Oak son inmutables, deben empaquetarse con el código de proyecto del cliente y solo deben implementarse mediante Cloud Manager.
* AEM Todas las definiciones de índices de Oak deben seguir la convención de nomenclatura y otras reglas para índices de Oak en el as a Cloud Service de la. De lo contrario, puede causar un comportamiento no deseado.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Herramientas y recursos"
>abstract="Revise el proyecto de WKND heredado para comprender cómo se pueden resolver las infracciones de OID en su proyecto. AEM Además, revise el ejemplo de infracción de OID en GitHub para comprender cómo se pueden convertir los índices heredados con la herramienta Conversor de índices y cómo se pueden hacer compatibles con los índices as a Cloud Service de."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="Proyecto de WKND heredado"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Ejemplo de infracción de OID: GitHub"

* Resuelva las infracciones de reglas de índice identificadas en el mensaje.
* AEM Para implementar definiciones de índice de Oak nuevas o personalizadas, siga los pasos que se indican a continuación as a Cloud Service [directrices de empaquetado](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure).
* AEM Los índices estándar de la personalizados y las nuevas definiciones de índices de Oak personalizadas deben seguir el [directrices de indexación de contenido](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing#preparing-the-new-index-definition) AEM para los as a Cloud Service.
* Consulte el proyecto de [WKND heredado](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) y comprenda cómo las [infracciones de OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) pueden corregirse y hacerse compatibles con AEM as a Cloud Service.
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclaraciones o para que se aborden las preocupaciones.
* Utilice el [Conversor de índices](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools) AEM para migrar las definiciones de índice de Oak personalizadas existentes a definiciones de índice de Oak personalizadas compatibles con el as a Cloud Service.
