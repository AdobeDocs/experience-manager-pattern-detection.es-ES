---
title: SCR
description: Página de ayuda de código del detector de patrones.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---

# SCR {#scr}

## Fondo {#background}

SIF identifica el uso de AEM Screens que es incompatible con AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Posibles soluciones {#solutions}

Encuentre las posibles soluciones para los diferentes subtipos a continuación:

* `screens.bundles.detected`: estos paquetes se desinstalarán durante la actualización.
* `screens.packages.detected`: estos paquetes se eliminarán durante la actualización.
* `screens.packages.dependency`: elimine cualquier dependencia de Screens de sus paquetes personalizados.
* `screens.configs.detected` - Asegúrese de que no está usando ninguna propiedad de configuración de Screens en su código personalizado.
* `screens.users.detected`: asegúrese de que no utiliza usuarios del servicio Screens en el código personalizado.
* `screens.paths.detected`: quite las rutas de Screens después de asegurarse de que no se están usando en AEM.
* `screens.resource.type.detected` - Quitar el uso de tipo de recurso de Screens.
* `screens.usage`: elimine las API de Screens de su código personalizado.