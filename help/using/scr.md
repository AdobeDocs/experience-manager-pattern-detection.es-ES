---
title: SCR
description: Página de ayuda de código del detector de patrones.
exl-id: 13b14cc2-f70b-45ff-a62d-dee647311d84
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%
---
# SCR {#scr}

## Información general {#background}

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
