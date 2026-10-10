---
title: IOI
description: Página de ayuda de código del detector de patrones.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 100%
---
# IOI {#ioi}

Importación interna de Oak

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Importación interna de Oak"
>abstract="El código IOI identifica el uso del cliente de los paquetes Oak internos y los importa a través de OSGi. Se exportan sin ninguna versión en particular. Los paquetes Oak o los servicios de bajo nivel de AEM solo los consumen."

`IOI` Identifica el uso de los paquetes Oak internos por parte del cliente, importándolos a través de OSGi. Se exportan sin ninguna versión en particular. Los paquetes Oak o los servicios de bajo nivel de AEM solo los consumen.
Algunas de estas áreas son utilizadas por `com.adobe.granite.repository`, que configura un repositorio para AEM durante el inicio. Otro ejemplo es el paquete de Adobe `com.adobe.granite.maintenance.oak`, que ajusta y proporciona tareas de mantenimiento de Oak.

## Posibles implicaciones y riesgos {#implications-and-risks}

* En una versión futura de AEM, las exportaciones internas podrían eliminarse, lo que ocasionaría dependencias rotas y paquetes inactivos dependiendo directamente de Oak.
* La API en las exportaciones internas puede cambiar.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Directrices para la implementación"
>abstract="Los clientes deben revisar su código personalizado para identificar el uso de dichas API y refactorizarlas para que sean compatibles con AEM as a Cloud Service. Póngase en contacto con la Asistencia de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Utilice la API de recursos de Sling (o la API de JCR) en lugar del acceso de bajo nivel.
* Evite depender de paquetes internos que no formen parte de ninguna API pública o SPI.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
