---
title: SIF
description: Página de ayuda de código del detector de patrones.
exl-id: c0a5c565-16e7-407b-befc-5a2966089da1
source-git-commit: 29d702c9662fd185ef806123fc4f4a03a70d64aa
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 7%
---
# SIF {#sif}

## Contexto {#background}

SIF identifica el uso social que es incompatible con AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Posibles soluciones {#solutions}

Encuentre las posibles soluciones para los diferentes subtipos a continuación:

* `social.bundles.detected`: estos paquetes se desinstalarán durante la actualización
* `social.packages.detected`: estos paquetes se eliminarán durante la actualización
* `social.packages.dependency` - Elimine la dependencia del paquete de las redes sociales de los paquetes personalizados
* `social.nodes.detected`: actualice el código personalizado para no crear nodos sociales
* `social.configs.detected` - No usar propiedades de configuración social en código personalizado
* `social.users.detected` - No usar usuarios sociales en código personalizado
* `social.overlays.detected` - Quitar uso de superposiciones sociales
* `social.paths.detected`: elimine las rutas sociales después de asegurarse de que estas no se utilizan en AEM
* `social.resource.type.detected` - Quitar el uso del tipo de recurso social
* `social.usage` - Quitar las API sociales del código personalizado.
