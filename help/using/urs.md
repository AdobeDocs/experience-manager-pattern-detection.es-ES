---
title: URS
description: Página de ayuda de código de Pattern Detector.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 53%

---

# URS {#urs}

Estructura de repositorio no admitida

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Estructura de repositorio no admitida"
>abstract="URS identifica casos de características de nodo y estructura de repositorio no admitidas. Esta información aparece para evitar conflictos entre el código de producto AEM y el código de cliente, contenido que se está reestructurando fuera de /etc a otras carpetas del repositorio y más."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Reestructuración de repositorios"

## Fondo {#background}

`URS`  Identifica casos de características de nodo y estructura de repositorio no admitidas. A partir del AEM 6.4, se han previsto directrices para la reestructuración del contenido del repositorio. Al delinear claramente las jerarquías para el código de producto AEM y el código de cliente y evitar conflictos entre ellos, el contenido se está reestructurando fuera de `/etc` a otras carpetas del repositorio, siguiendo las siguientes reglas de alto nivel:

* AEM El código de producto siempre se coloca en `/libs`, que no se deben sobrescribir con el código personalizado.
* El código personalizado debe colocarse en `/apps`, `/content`, y `/conf`.
* Es muy recomendable que estas directrices se sigan para AEM as a Cloud Service.

Los subtipos se utilizan para identificar tipos específicos de problemas de repositorios que deben solucionarse:

* `clientlibs.location`: Una biblioteca de cliente que hace referencia a `/etc` por ruta.
* `file.location`: Un archivo en `/etc` que se ha modificado desde la instalación.
* `node.location`: Un nodo en `/etc` que se ha modificado desde la instalación.
* `workflow.location`: Un modelo de flujo de trabajo o un lanzador en `/etc/workflow`.
* `package.structure`: Un paquete que contiene contenido mutable e inmutable.
* `node.size`: Un nodo con un tamaño no admitido.

## Posibles implicaciones y riesgos {#implications-and-risks}

* El código personalizado que depende de rutas antiguas puede causar un comportamiento no deseado y afectar a la funcionalidad del producto.
* Los paquetes que contienen contenido mutable e inmutable probablemente puedan causar problemas durante la implementación.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar el proyecto de código. AEM AEM Asegúrese de que se adhiera a las directrices de estructura del proyecto de la y evite que el código dependa de rutas de repositorio antiguas/no admitidas que puedan provocar un comportamiento no deseado en los as a Cloud Service. Póngase en contacto con el Soporte técnico de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Directrices de la estructura del proyecto AEM"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Consulte [Reestructuración de repositorios](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring) AEM para obtener instrucciones sobre cómo prepararse para el as a Cloud Service de la.
* Consulte también [AEM Estructura del proyecto de](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) si desea obtener más información sobre las áreas mutables e inmutables del repositorio.
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclaraciones o para que se aborden las preocupaciones.
* Utilice el [Modernizador de repositorio](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools) para reestructurar los paquetes de proyectos existentes separando contenido y código en paquetes discretos para que sean compatibles con la estructura de proyectos definida para Adobe Experience Manager as a Cloud Service.
