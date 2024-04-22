---
title: OAUI
description: Página de ayuda de código de Pattern Detector.
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 47%

---

# OAUI {#oaui}

Instancia de usuarios de OAuth

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="Instancia de usuarios de OAuth"
>abstract="El código OAUI identifica el patrón en el que hay al menos un usuario configurado relacionado con OAuth que requiere una migración correcta. OAuth está configurado para usuarios cuando hay un subnodo llamado oauth directamente bajo un nodo rep:AuthorizableId en forma de /home/user-path/user-node/oauth"
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service: notas de la versión"

OAUI identifica el patrón en el que hay al menos un usuario configurado relacionado con OAuth que requiere una migración correcta.

OAuth está configurado para usuarios cuando hay un subnodo llamado `oauth` directamente bajo `rep:AuthorizableId` en forma de `/home/user-path/user-node/oauth`.

Un ejemplo es: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Los usuarios externos configurados con OAuth no pueden iniciar sesión en instancias de autor/publicación hasta que se reconfiguren con el siguiente procedimiento.

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Directrices de implementación"
>abstract="AEM Los usuarios externos configurados con OAuth no pueden iniciar sesión en instancias de autor/publicación hasta que se hayan reconfigurado para ser compatibles con las instancias as a Cloud Service de la aplicación de creación de informes (o de publicación). AEM as a Cloud Service ofrece compatibilidad con la autenticación IMS solo para usuarios autores, administradores y desarrolladores, así como integración basada en SAML para los entornos de publicación. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support" text="Compatibilidad con IMS: AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="Integración de SAML: publicación"

* Póngase en contacto con el representante del Adobe si necesita discutir las opciones de migración de usuarios.
* Póngase en contacto con [AEM Equipo de soporte](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para aclaraciones o para que se aborden las preocupaciones.
