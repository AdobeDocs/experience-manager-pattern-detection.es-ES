---
title: WRF
description: Página de ayuda de código del detector de patrones.
exl-id: 36578498-d5b2-46d1-a274-a1646ceaa764
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 8%
---
# WRF {#wrf}

## Información general {#background}

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
