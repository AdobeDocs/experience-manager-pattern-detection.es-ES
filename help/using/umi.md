---
title: UMI
description: Página de ayuda de código de Pattern Detector.
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 43%

---

# UMI {#umi}

Problema de falta de configuración de la actualización

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problema de falta de configuración de la actualización"
>abstract="UMI identifica las modificaciones a ciertas configuraciones de OSGi que causan problemas al actualizar, incluida una actualización fallida o una funcionalidad reducida."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Cambios importantes en AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service: notas de la versión"

UMI identifica las modificaciones a ciertas configuraciones de OSGi que causan problemas al actualizar, incluida una actualización fallida o una funcionalidad reducida.

Se comprueban las siguientes configuraciones para su modificación:

* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config` : Identifique si la propiedad `org.apache.sling.commons.log.file` de los registradores personalizados señala a algo distinto del archivo `logs/error.log`.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Cambiar o quitar configuraciones puede causar los siguientes problemas:
   * La actualización puede quedarse atascada (por ejemplo, `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` faltaba, pero estaba presente en `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Los problemas de autorización pueden producirse después de la actualización (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Es posible que ciertas funciones no operen correctamente. Por ejemplo, cambiar `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` puede provocar que algunos archivos JSP no se compilen, lo que en última instancia resulta en la pérdida de funcionalidad.
   * Los valores de la configuración del externalizador `com.day.cq.commons.impl.ExternalizerImpl` AEM son establecidas por variables de entorno de cloud manager en as a Cloud Service.
   * AEM as a Cloud Services no admite archivos de registro personalizados. AEM No se puede acceder a los registros escritos en registros con nombres personalizados desde el as a Cloud Service de la.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar las configuraciones actuales y revertir los cambios realizados en las configuraciones mencionadas para evitar cualquier problema de actualización futuro. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* No cambie ni elimine las cuatro configuraciones mencionadas anteriormente.
   * Si se produce la siguiente infracción:\
     &quot;Propiedades requeridas para la configuración OSGi `xyz-configuration` faltan: &#39;[property-1,property-2...]&#39;.&quot;\
     Confirme si estas eliminaciones son legítimas o no porque estas configuraciones de OSGI son OOTB y es posible que nunca se hayan modificado o guardado desde el Administrador de configuración OSGi.
* Si las configuraciones se han modificado, se deben restaurar a los valores esperados. Estos valores se indican en los mensajes de `UMI`.
* Para `com.day.cq.commons.impl.ExternalizerImpl`, consulte [documentación](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) AEM para establecer la configuración de externalizador mediante variables de entorno de cloud manager en as a Cloud Service de la.
* Para `org.apache.sling.commons.log.LogManager.factory.config`, cambie la configuración OSGI para enviar el registrador personalizado al archivo `logs/error.log`. Consulte [documentación](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) para volver a señalar a `logs/error.log` archivo.
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclaraciones o para que se aborden las preocupaciones.
