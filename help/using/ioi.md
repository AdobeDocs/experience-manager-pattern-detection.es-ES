---
title: IOI
description: Página de ayuda de código del detector de patrones
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
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
>abstract="El código IOI identifica el uso del cliente de los paquetes Oak internos y los importa a través de OSGi. Normalmente se exportan sin ninguna versión en particular y están destinados al consumo únicamente por otros paquetes Oak o servicios de AEM de bajo nivel."

`IOI` identifica el uso de los paquetes Oak internos por parte del cliente, importándolos a través de OSGi. Normalmente se exportan sin ninguna versión en particular y están destinados al consumo únicamente por otros paquetes Oak o servicios de AEM de bajo nivel.

Algunos de ellos son utilizados por `com.adobe.granite.repository`, que configura un repositorio para AEM durante el inicio. Otro ejemplo es el paquete de Adobe `com.adobe.granite.maintenance.oak`, que ajusta y proporciona tareas de mantenimiento de Oak.

## Posibles implicaciones y riesgos {#implications-and-risks}

* En una versión futura de AEM, las exportaciones internas podrían eliminarse, lo que ocasionaría dependencias rotas y paquetes inactivos dependiendo directamente de Oak.
* La API en las exportaciones internas puede cambiar.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Directrices de implementación"
>abstract="Los clientes deben revisar su código personalizado para identificar el uso de dichas API y refactorizarlas para que sean compatibles con AEM as a Cloud Service. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Utilice la API de recursos de Sling (o la API de JCR) en lugar del acceso de bajo nivel.
* Evite depender de paquetes internos que no formen parte de ninguna API pública o SPI.
* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
