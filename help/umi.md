---
title: UMI
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# UMI {#umi}

Problema de falta de configuración de la actualización

## Fondo {#background}

`UMI` identifica las modificaciones a ciertas configuraciones de OSGi que causarán problemas al actualizar, incluida una actualización fallida o una funcionalidad reducida.

Se comprueban las siguientes configuraciones para su modificación:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## Posibles implicaciones y riesgos {#implications-and-risks}

* Cambiar o quitar configuraciones puede causar los siguientes problemas:
   * La actualización puede quedar atascada (por ejemplo, faltaba `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` pero está presente en `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Los problemas de autorización pueden producirse después de la actualización (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Es posible que ciertas funciones no funcionen correctamente. Por ejemplo, cambiar `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` puede causar que algunos archivos JSP no se compilen, lo que en última instancia resultará en la pérdida de funcionalidad.

## Posibles soluciones {#solutions}

* No cambie ni elimine las cuatro configuraciones mencionadas anteriormente.
* Si las configuraciones se han cambiado, se deben restaurar a los valores esperados. Estos valores se indican en los mensajes `UMI`.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
