---
title: URL
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# URS {#urs}

Estructura de repositorio no admitida

## Fondo {#background}

`URS` identifica casos de estructura de repositorio no admitida. A partir del AEM 6.4, se han previsto directrices para la reestructuración del contenido del repositorio. Al delinear claramente las jerarquías para AEM código de producto y código de cliente y evitar conflictos entre ellos, el contenido se está reestructurando fuera de `/etc` a otras carpetas del repositorio, siguiendo las siguientes reglas de alto nivel:

* AEM código de producto siempre se colocará en `/libs`, que no se debe sobrescribir con el código personalizado. El código personalizado debe colocarse en `/apps`, `/content` y `/conf`.
* Es muy recomendable que estas directrices se sigan como Cloud Service para AEM.

Los subtipos se utilizan para identificar tipos específicos de problemas de repositorios que deben solucionarse:
* `clientlibs.location`: Una biblioteca de cliente que hace referencia  `/etc` por ruta.
* `file.location`: Archivo en  `/etc` que se ha modificado desde la instalación.
* `node.location`: Un nodo en el  `/etc` que se ha modificado desde la instalación.
* `workflow.location`: Un modelo de flujo de trabajo o lanzador en  `/etc/workflow`.
* `package.structure`: Paquete que contiene contenido mutable e inmutable.

## Posibles implicaciones y riesgos {#implications-and-risks}

* El código personalizado que depende de rutas antiguas puede causar un comportamiento no deseado y afectar a la funcionalidad del producto.
* Los paquetes que contienen contenido mutable e inmutable probablemente causarán problemas durante la implementación.

## Posibles soluciones {#solutions}

* Consulte [Reestructuración del repositorio](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) para obtener instrucciones sobre cómo prepararse para AEM como Cloud Service.
* Consulte también [AEM Estructura del proyecto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) para obtener más información sobre las áreas mutables e inmutables del repositorio.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
* Aproveche el [Modernizador de repositorio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools) para reestructurar los paquetes de proyectos existentes separando contenido y código en paquetes discretos para que sean compatibles con la estructura de proyectos definida para Adobe Experience Manager como Cloud Service.