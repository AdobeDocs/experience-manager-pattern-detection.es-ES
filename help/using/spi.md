---
title: SPI
description: Página de ayuda de código del detector de patrones.
source-git-commit: e050b9190f67fd6ccfac31490c4bf2a60d47731f
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 8%

---

# SPI {#spi}

## Fondo {#background}

SIF identifica el uso de Search and Promote que es incompatible con AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Posibles soluciones {#solutions}

Encuentre las posibles soluciones para los diferentes subtipos a continuación:

* `searchpromote.bundles.detected`: estos paquetes se desinstalarán durante la actualización
* `earchpromote.packages.detected`: estos paquetes se eliminarán durante la actualización
* `searchpromote.packages.dependency`: elimine cualquier dependencia de Search&amp;Promote que puedan tener sus paquetes personalizados
* `searchpromote.usage` - Quitar las API de Search&amp;Promote del código personalizado
* `searchpromote.users.detected` - No usar los usuarios del servicio Buscar y Promocionar en el código personalizado
* `searchpromote.configs.detected` - No use las propiedades de configuración de Search&amp;Promote en su código personalizado.