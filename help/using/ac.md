---
title: AC
description: Página de ayuda de código del detector de patrones.
exl-id: 4c6ac075-5ba6-4511-97c6-a9b496d4677a
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
# AC {#ac}

## Información general {#background}

AC identifica el uso del paquete de Assets que es incompatible con AEM 6.5 LTS

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Posibles soluciones {#solutions}

Encuentre las posibles soluciones para los diferentes subtipos a continuación:

* `asset.bundles.detected`: este paquete se desinstalará durante la actualización.
* `asset.usage`: elimine cualquier dependencia de los componentes Clasificación de recursos y Catálogo de recursos del código personalizado. Si corresponde, cambie el código para utilizar la nueva API `List<Scene7ConfigSetting>` `com.day.cq.dam.scene7.api.model.Scene7ViewerConfig#getSettingsList()`.
* `asset.overlays.detected`: es necesario eliminar las superposiciones creadas en los componentes de catálogo y clasificación de Assets.
* `asset.resource.type.detected`: elimine cualquier uso del tipo de recurso del componente de clasificación de Assets en su código personalizado.
* `asset.paths.detected`: mueva el contenido de clientes presente en estas rutas y quite estas rutas después de asegurarse de que no se utilizan en AEM.

