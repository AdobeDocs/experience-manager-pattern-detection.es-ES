---
title: INST
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---


# INST {#inst}

Artefacto instalado

## Fondo {#background}

`INST` identifica paquetes y paquetes personalizados y de terceros que el cliente ha instalado en AEM. Se informa de que estas medidas ayudan a caracterizar el estado del sistema en el ámbito general de un esfuerzo de actualización.

Cuando se instalan varias versiones de un paquete, solo se informa de la última versión.

Los paquetes y paquetes detectados no se han optimizado necesariamente para AEM como Cloud Service. Cualquier paquete de terceros debe verificarse con su creador o Adobe para comprobar la compatibilidad con AEM como Cloud Service.

Los subtipos se utilizan para identificar diferentes tipos de información:

* `custom.bundle`: Paquete que se ha instalado en AEM.
* `custom.package`: Paquete que se ha instalado en AEM.

## Posibles implicaciones y riesgos {#implications-and-risks}

* La instalación de paquetes de terceros mediante el Administrador de paquetes CRX no es posible en AEM como Cloud Service.
* Es posible que las aplicaciones que dependen de paquetes de terceros no funcionen según lo esperado hasta que se implementen correctamente para trabajar con AEM como Cloud Service.
* Los paquetes de terceros proveedores, si no están optimizados para AEM as a Cloud Service, pueden dar como resultado un comportamiento no deseado.

## Posibles soluciones {#solutions}

* Los paquetes de terceros deben implementarse en AEM como parte del proyecto mediante el proceso de implementación [Cloud Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process).
* Revise cómo [integrar paquetes de terceros](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages) en su proyecto para AEM como Cloud Service.
* Los paquetes de terceros deben adherirse a las directrices AEM as a Cloud Service [development](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) y [packaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html).
* Revise el proyecto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) y comprenda cómo se pueden corregir las [infracciones INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) y hacerlas compatibles con AEM como Cloud Service.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
