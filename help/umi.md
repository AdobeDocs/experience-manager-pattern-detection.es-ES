---
title: UMI
description: Página de ayuda de código del detector de patrones
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: ht
source-wordcount: '234'
ht-degree: 100%

---

# UMI {#umi}

Problema de falta de configuración de la actualización

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problema de falta de configuración de la actualización"
>abstract="UMI identifica las modificaciones a ciertas configuraciones de OSGi que causarán problemas al actualizar, incluida una actualización fallida o una funcionalidad reducida."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=es" text="Cambios importantes en AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=es" text="AEM as a Cloud Service: notas de la versión"

`UMI` identifica las modificaciones a ciertas configuraciones de OSGi que causarán problemas al actualizar, incluida una actualización fallida o una funcionalidad reducida.

Se comprueban las siguientes configuraciones para su modificación:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## Posibles implicaciones y riesgos {#implications-and-risks}

* Cambiar o quitar configuraciones puede causar los siguientes problemas:
   * La actualización puede quedarse atascada (por ejemplo, `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` faltaba, pero estaba presente en `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Los problemas de autorización pueden producirse después de la actualización (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Es posible que ciertas funciones no operen correctamente. Por ejemplo, cambiar `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` puede provocar que algunos archivos JSP no se compilen, lo que en última instancia resultará en la pérdida de funcionalidad.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Directrices de implementación"
>abstract="Una práctica recomendada es revisar las configuraciones actuales y revertir los cambios realizados en las configuraciones mencionadas para evitar cualquier problema de actualización futuro. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* No cambie ni elimine las cuatro configuraciones mencionadas anteriormente.
* Si las configuraciones se han modificado, se deben restaurar a los valores esperados. Estos valores se indican en los mensajes de `UMI`.
* Póngase en contacto con nuestro [Equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o solucionar problemas.
