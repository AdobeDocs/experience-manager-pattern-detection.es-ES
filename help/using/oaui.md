---
title: OAUI
description: Página de ayuda de código del detector de patrones.
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 100%

---

# OAUI {#oaui}

Instancia de usuarios de OAuth

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="Instancia de usuarios de OAuth"
>abstract="El código OAUI identifica el patrón en el que hay al menos un usuario configurado relacionado con OAuth que requiere una migración correcta. OAuth está configurado para usuarios cuando hay un subnodo llamado Oauth directamente bajo un nodo rep:AuthorizableId en forma de /home/user-path/user-node/oauth"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service: Notas de la versión"

`OAUI` Identifica el patrón en el que hay al menos un usuario configurado relacionado con OAuth que requiere una migración correcta.

OAuth está configurado para usuarios cuando hay un subnodo llamado `oauth` directamente bajo `rep:AuthorizableId` en forma de `/home/user-path/user-node/oauth`.

Un ejemplo es: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Los usuarios externos configurados con OAuth no pueden iniciar sesión en instancias de creación/publicación hasta que se reconfiguren con el siguiente procedimiento.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Directrices de implementación"
>abstract="Los usuarios externos configurados con OAuth no pueden iniciar sesión en instancias de creación/publicación hasta que se hayan reconfigurado para ser compatibles con AEM as a Cloud Service. AEM as a Cloud Service ofrece compatibilidad con la autenticación IMS solo para usuarios autores, administradores y desarrolladores y proporciona integración basada en SAML para los entornos de publicación. Póngase en contacto con la Asistencia de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/security/ims-support" text="Compatibilidad con IMS: AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="Integración de SAML: publicación"

* Póngase en contacto con su representante de Adobe para hablar de las opciones de migración de usuarios.
* Póngase en contacto con el [equipo de soporte de AEM](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
