---
title: WRF
description: Página de ayuda de código del detector de patrones.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 8%

---

# WRF {#wrf}

## Fondo {#background}

WRF identifica el uso de We-Retail incompatible con AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Posibles soluciones {#solutions}

Encuentre las posibles soluciones para los diferentes subtipos a continuación:

* `weretail.bundles.detected`: estos paquetes se desinstalarán durante la actualización
* `weretail.packages.detected`: estos paquetes se eliminarán durante la actualización
* `weretail.configs.detected`: no use las propiedades de configuración de We.Retail en su código personalizado
* `weretail.packages.dependency`: elimine la dependencia de cualquier paquete personalizado en We.Retail
* `weretail.paths.detected`: estas rutas de We.Retail se pueden eliminar después de asegurarse de que no utiliza las redes sociales
* `weretail.resource.type.detected`: eliminar el uso de tipo de recurso de We.Retail
* `weretail.usage`: elimine las API de We.Retail de su código personalizado.