---
title: IOI
description: Página de ayuda de código del detector de patrones.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 60%

---

# IOI {#ioi}

Importación interna de Oak

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Importación interna de Oak"
>abstract="El código IOI identifica el uso del cliente de los paquetes Oak internos y los importa mediante OSGi. Se exportan sin ninguna versión en particular. AEM Los paquetes Oak o los servicios de bajo nivel de la solo los consumen."

`IOI` Identifica el uso de los paquetes Oak internos por parte del cliente, importándolos a través de OSGi. Se exportan sin ninguna versión en particular. AEM Los paquetes Oak o los servicios de bajo nivel de la solo los consumen.
Algunas de estas áreas son utilizadas por `com.adobe.granite.repository`AEM , que configura un repositorio para el inicio de los procesos de la. Otro ejemplo es el paquete de Adobe `com.adobe.granite.maintenance.oak`, que ajusta y proporciona tareas de mantenimiento de Oak.

## Posibles implicaciones y riesgos {#implications-and-risks}

* AEM En una versión futura, las exportaciones internas de la versión de la podrían eliminarse, lo que ocasionaría dependencias rotas y paquetes inactivos dependiendo directamente de Oak.
* La API en las exportaciones internas puede cambiar.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Directrices de implementación"
>abstract="Los clientes deben revisar su código personalizado para identificar el uso de dichas API y refactorizarlas para que sean compatibles con AEM as a Cloud Service. Póngase en contacto con el equipo de soporte de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Utilice la API de recursos de Sling (o la API de JCR) en lugar del acceso de bajo nivel.
* Evite depender de paquetes internos que no formen parte de ninguna API pública o SPI.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclarar sus dudas o resolver sus problemas.
