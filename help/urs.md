---
title: URL
description: Página de ayuda de código de Pattern Detector
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# URS {#urs}

Estructura de repositorio no admitida

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Estructura de repositorio no admitida"
>abstract="URS identifica casos de estructura de repositorio no admitida. Esta información aparece para evitar conflictos entre AEM código de producto y el código de cliente, contenido que se está reestructurando fuera de /etc a otras carpetas del repositorio y más."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html" text="Reestructuración de repositorios"

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

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar el proyecto de código y asegurarse de que se adhiere a las directrices de estructura del proyecto AEM y evitar que el código dependa de rutas de repositorio antiguas/no admitidas que puedan provocar un comportamiento no deseado en AEM como Cloud Service. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html" text="Directrices AEM estructura del proyecto"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"

* Consulte [Reestructuración del repositorio](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) para obtener instrucciones sobre cómo prepararse para AEM como Cloud Service.
* Consulte también [AEM Estructura del proyecto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) para obtener más información sobre las áreas mutables e inmutables del repositorio.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
* Aproveche el [Modernizador de repositorio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools) para reestructurar los paquetes de proyectos existentes separando contenido y código en paquetes discretos para que sean compatibles con la estructura de proyectos definida para Adobe Experience Manager como Cloud Service.