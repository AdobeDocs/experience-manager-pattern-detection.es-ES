---
title: INST
description: Página de ayuda de código de Pattern Detector.
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 72%

---

# INST {#inst}

Artefacto instalado

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Artefacto instalado"
>abstract="INST identifica paquetes personalizados y de terceros que el cliente ha instalado en AEM. Se informa de que estas medidas ayudan a caracterizar el estado del sistema en el ámbito general de un esfuerzo de actualización. Cualquier paquete de terceros debe adherirse a las directrices de desarrollo as a Cloud Service y empaquetado AEM."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Directrices de desarrollo: AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package" text="Directrices de paquetes: AEM as a Cloud Service"

`INST`  AEM Identifica paquetes personalizados y de terceros que el cliente ha instalado en el servicio de paquetes de. Se informa de que estas medidas ayudan a caracterizar el estado del sistema en el ámbito general de un esfuerzo de actualización.

Cuando se instalan varias versiones de un paquete, solo se informa de la última versión.

Los paquetes detectados no se han optimizado necesariamente para AEM as a Cloud Service. Cualquier paquete de terceros debe verificarse con su creador o Adobe para comprobar la compatibilidad con AEM as a Cloud Service.

Los subtipos se utilizan para identificar diferentes tipos de información:

* `custom.bundle`: Un paquete que se ha instalado en AEM.
* `custom.package`: Un paquete que se ha instalado en AEM.

## Posibles implicaciones y riesgos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Directrices de implementación"
>abstract="Los clientes ya no pueden instalar paquetes de terceros mediante el Administrador de paquetes CRX. AEM Los clientes deben revisar estos artefactos instalados que deben estar estructurados y optimizarlos para que funcionen con el as a Cloud Service de la. Compruebe la compatibilidad de cualquier paquete de terceros con el as a Cloud Service mediante su creador o su Adobe AEM."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embeddeds" text="Incrustación de subpaquetes en el paquete de contenedor"


* La instalación de paquetes de terceros mediante el Administrador de paquetes CRX no es posible en AEM as a Cloud Service.
* Es posible que las aplicaciones que dependen de paquetes de terceros no funcionen según lo esperado hasta que se implementen correctamente para trabajar con AEM as a Cloud Service.
* Los paquetes de terceros proveedores, si no están optimizados para AEM as a Cloud Service, pueden dar como resultado un comportamiento no deseado.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Herramientas y recursos"
>abstract="Revise el proyecto heredado de WKND para comprender cómo se pueden hacer compatibles las infracciones de INST con AEM Cloud Service. AEM Además, revise el ejemplo de infracción INST en GitHub para comprender cómo se puede corregir e implementar en as a Cloud Service de la."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="Proyecto de WKND heredado"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Ejemplo de infracción INST: GitHub"

* Los paquetes de terceros deben implementarse en AEM como parte del proyecto mediante el [proceso de implementación](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deployment-process) de Cloud Manager.
* Consulte cómo [incrustar paquetes de terceros](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embedding-3rd-party-packages) en el proyecto para AEM as a Cloud Service.
* Los paquetes de terceros deben adherirse a las directrices de [desarrollo](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines) y [embalaje](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package) de AEM as a Cloud Service.
* Consulte el proyecto de [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) y comprenda cómo las [Infracciones INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) pueden corregirse y hacerse compatibles con AEM as a Cloud Service.
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclaraciones o para que se aborden las preocupaciones.
