---
title: OAUI
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# OAUI {#oaui}

Instancia de usuarios de OAuth

## Fondo {#background}

`OAUI` identifica el patrón en el que hay al menos un usuario configurado relacionado con OAuth que requiere una migración correcta.

OAuth se configura para usuarios cuando hay un subnodo llamado `oauth` directamente bajo un nodo `rep:AuthorizableId` en forma de `/home/user-path/user-node/oauth`.

Un ejemplo es: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Posibles implicaciones y riesgos {#implications-and-risks}

* Los usuarios externos configurados con OAuth no podrán iniciar sesión en instancias de autor/publicación hasta que se reconfiguren con el siguiente procedimiento.

## Posibles soluciones {#solutions}

* Póngase en contacto con su representante de Adobe para discutir las opciones de migración de usuarios.
* Póngase en contacto con nuestro [AEM equipo de soporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
