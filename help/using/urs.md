---
title: URS
description: Página de ayuda de código del detector de patrones
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '436'
ht-degree: 100%

---

# URS {#urs}

Estructura de repositorio no admitida

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Estructura de repositorio no admitida"
>abstract="URS identifica casos de características de nodo y estructura de repositorio no admitidas. Esta información aparece para evitar conflictos entre el código de producto AEM y el código de cliente, contenido que se está reestructurando fuera de /etc a otras carpetas del repositorio y más."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=es" text="Reestructuración de repositorios"

## Fondo {#background}

`URS` identifica casos de estructura de repositorio no compatible y características de nodo. A partir del AEM 6.4, se han previsto directrices para la reestructuración del contenido del repositorio. Al delinear claramente las jerarquías para el código de producto AEM y el código de cliente y evitar conflictos entre ellos, el contenido se está reestructurando fuera de `/etc` a otras carpetas del repositorio, siguiendo las siguientes reglas de alto nivel:

* El código de producto AEM siempre se colocará en `/libs`, que no se debe sobrescribir con el código personalizado.
* El código personalizado debe colocarse en `/apps`, `/content` y `/conf`.
* AEM as a Cloud Service no admite nombres de nodo largos (>150 bytes).
* Es muy recomendable que estas directrices se sigan para AEM as a Cloud Service.

Los subtipos se utilizan para identificar tipos específicos de problemas de repositorios que deben solucionarse:
* `clientlibs.location`: Una biblioteca de cliente que hace referencia a `/etc` por ruta.
* `file.location`: Un archivo en `/etc` que se ha modificado desde la instalación.
* `node.location`: Un nodo en `/etc` que se ha modificado desde la instalación.
* `workflow.location`: Un modelo de flujo de trabajo o un lanzador en `/etc/workflow`.
* `package.structure`: Un paquete que contiene contenido mutable e inmutable.
* `node.name.length`: Un nombre de nodo con longitud no admitida.
* `node.size`: Un nodo con un tamaño no admitido.

## Posibles implicaciones y riesgos {#implications-and-risks}

* El código personalizado que depende de rutas antiguas puede causar un comportamiento no deseado y afectar a la funcionalidad del producto.
* Los paquetes que contienen contenido mutable e inmutable probablemente causarán problemas durante la implementación.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar el proyecto de código y asegurarse de que se adhiera a las directrices de estructura del proyecto AEM y evitar que el código dependa de rutas de repositorio antiguas/no admitidas que puedan provocar un comportamiento no deseado en AEM as a Cloud Service. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=es" text="Directrices de la estructura del proyecto AEM"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Consulte la [Reestructuración de repositorios](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=es) para obtener instrucciones para prepararse para AEM as a Cloud Service.
* Consulte también la [Estructura del proyecto AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=es) para obtener más información sobre las áreas mutables e inmutables del repositorio.
* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
* Aproveche el [Modernizador de repositorio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html?lang=es#refactoring-tools) para reestructurar los paquetes de proyectos existentes separando contenido y código en paquetes discretos para que sean compatibles con la estructura de proyectos definida para Adobe Experience Manager as a Cloud Service.
