---
title: URS
description: Página de ayuda de código del detector de patrones.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 66%

---

# URS {#urs}

Estructura de repositorio no admitida

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Estructura de repositorio no admitida"
>abstract="URS identifica casos de URS (estructura de repositorio no admitida) y características de nodo. AEM Esta información aparece para evitar conflictos entre el código de producto y el código de cliente, contenido que se está reestructurando fuera de la estructura de productos de `/etc` a otras carpetas del repositorio y más."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Reestructuración de repositorios"

## Fondo {#background}

`URS`  Identifica casos de URS (estructura de repositorio no admitida) y características de nodo. A partir del AEM 6.4, se han previsto directrices para la reestructuración del contenido del repositorio. AEM Al delinear claramente las jerarquías para el código de producto, el código de producto y el código de cliente, y evitar conflictos entre todos ellos, el contenido se está reestructurando fuera de `/etc` a otras carpetas del repositorio. Al hacerlo, se adhieren a las siguientes reglas de alto nivel:

* AEM El código de producto siempre se coloca en `/libs` ese código personalizado no debe sobrescribirse.
* El código personalizado debe colocarse en `/apps`, `/content`, y `/conf`.
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
* Los paquetes que contienen contenido mutable e inmutable probablemente causarán problemas durante la implementación.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Directrices de implementación"
>abstract="La práctica recomendada consiste en revisar su proyecto de código. AEM AEM Asegúrese de que se adhiera a las directrices de estructura del proyecto de la y evite que el código dependa de rutas de repositorio antiguas o no admitidas que puedan provocar un comportamiento no deseado en los as a Cloud Service. Póngase en contacto con el equipo de soporte de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Directrices de la estructura del proyecto AEM"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Consulte la [Reestructuración de repositorios](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring) para obtener ayuda para prepararse para AEM as a Cloud Service.
* Consulte también la [Estructura del proyecto AEM](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) para obtener más información sobre las áreas mutables e inmutables del repositorio.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
* Utilice el [Modernizador de repositorio](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools) para reestructurar los paquetes de proyectos existentes separando contenido y código en paquetes discretos para que sean compatibles con la estructura de proyectos definida para Adobe Experience Manager as a Cloud Service.
