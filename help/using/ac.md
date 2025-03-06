---
title: AC
description: Página de ayuda de código del detector de patrones.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---

# AC {#ac}

## Fondo {#background}

AC identifica el uso del paquete de Assets que es incompatible con AEM 6.5 LTS

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Posibles soluciones {#solutions}

Encuentre las posibles soluciones para los diferentes subtipos a continuación:

* `asset.bundles.detected`: este paquete se desinstalará durante la actualización.
* `asset.usage`: elimine cualquier dependencia de los componentes Clasificación de recursos y Catálogo de recursos del código personalizado. Si corresponde, cambie el código para utilizar la nueva API `List<Scene7ConfigSetting>` `com.day.cq.dam.scene7.api.model.Scene7ViewerConfig#getSettingsList()`.
* `asset.overlays.detected`: es necesario eliminar las superposiciones creadas en los componentes de catálogo y clasificación de Assets.
* `asset.resource.type.detected`: elimine cualquier uso del tipo de recurso del componente de clasificación de Assets en su código personalizado.
* `asset.paths.detected`: mueva el contenido de clientes presente en estas rutas y quite estas rutas después de asegurarse de que no se utilizan en AEM.