---
title: Forms
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: a6ba6e93c89644160650882ecbf17028bec35068
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---


# [!DNL FORMS] {#forms}

[!DNL Adobe Experience Manager Forms]

## Fondo {#background}

`FORMS` identifica posibles problemas relacionados con la migración de Adobe Experience Manager Forms a Adobe Experience Manager Forms como Cloud Service. Solucione estos problemas antes de migrar a Cloud Service.

Los siguientes subtipos le ayudan a identificar los diferentes tipos de problemas:

* `modified.feature`: Estas funciones, recursos o API se actualizaron o modificaron para el Cloud Service. Antes de migrar al Cloud Service, ejecute la utilidad de migración para que estas funciones y recursos sean compatibles con el Cloud Service.
* `unavailable.feature`: Su entorno tiene características y recursos que no están disponibles ni se han eliminado del Cloud Service. No migre estas características o recursos a un entorno de Cloud Service.
* `unsupported.feature`: Su entorno utiliza algunas funciones que aún no son compatibles con el Cloud Service. No migre estas características o recursos a un entorno de Cloud Service. Tenga en cuenta las notas de la versión mensuales para ver la disponibilidad de las funciones.
* `unsupported.api`: Su entorno tiene algunas API que aún no son compatibles con el Cloud Service. Antes de migrar al Cloud Service, deshabilite, sustituya o elimine estas API de su código. Tenga en cuenta las notas de la versión mensuales para ver la disponibilidad de las funciones.

Consulte las secciones [Posibles implicaciones y riesgos](#implications-and-risks) y [Posibles soluciones](#solutions) para obtener información sobre los reemplazos y otras acciones necesarias para hacer que algunas funciones y API sean compatibles con el Cloud Service

## Posibles implicaciones y riesgos {#implications-and-risks}

Solucione los siguientes problemas antes de migrar a Adobe Experience Manager Forms como Cloud Service. Cuando no se abordan las implicaciones y riesgos que se enumeran a continuación, algunas funciones no funcionan como se espera en el entorno del Cloud Service.

* La funcionalidad del editor de código de la función del editor de reglas no está disponible. (CODE_EDITOR)

* La compatibilidad con el correo electrónico (puerto SMTP) está deshabilitada de forma predeterminada. (EMAIL_SERVICE_CONFIGURATION)

* La acción de envío **[!UICONTROL Email PDF]** no está disponible.(EMAIL_PDF_SUBMIT_ACTION)

* Los formularios adaptables basados en XDP aún no son compatibles. (XDP_BASED_FORM)

* Se invoca una acción de envío inmediatamente al presentar el formulario, en lugar de esperar a que todos los firmantes completen la firma. Por lo tanto, el documento de firma de formulario adaptable (PDF de acuerdo con Adobe Sign enviado a los firmantes) no está disponible para enviar acciones para utilizarlo o procesarlo. (FORM_SIGN_INTEGRATION)

* El paso Firma no está disponible. (SIGNATURE_STEP)

* El paso Verificar no está disponible. (VERIFY_STEP)

* La función del portal de Forms y la **[!UICONTROL acción de envío del portal de Forms]** no están disponibles. No se puede utilizar Forms Portal para enumerar formularios, guardar borradores o mostrar formularios enviados. No se pueden enviar (utilizar **[!UICONTROL Forms Portal submit action]** ) datos enviados a un formulario adaptable a un portal de Forms. [!UICONTROL Guardar como ] borrador y las funciones de formulario adaptable  [!UICONTROL de ] guardado automático no son compatibles actualmente. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* La acción de envío **[!UICONTROL Submit to Forms workflow]** no está disponible. En AEM 6.5 Forms y versiones anteriores, la acción de envío se utilizó para enviar datos de formulario adaptables a AEM Forms heredado en flujos de trabajo y LiveCycles Workflow JEE. (LC_WORKFLOW_SUBMISSION)

* La capacidad de comunicaciones interactivas no está disponible.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL Guardar como]** borrador y las funciones de formulario adaptable  **[!UICONTROL de]** guardado automático no son compatibles actualmente. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* El acordeón de metadatos no está disponible. (METADATA_ACCORDION_FORM_CONTAINER)

* El componente CAPTCHA ahora utiliza el servicio Google reCAPTCHA para validar CAPTCHA de forma predeterminada. La opción de usar Adobe Experience Manager para validar CAPTCHA no está disponible. (FORMS_CAPTCHA)

## Posibles soluciones {#solutions}

* Utilice la utilidad de migración para convertir todas las secuencias de comandos de reglas del entorno en funciones reutilizables. Puede utilizar las funciones reutilizables con el editor de reglas visuales para seguir obteniendo resultados obtenidos con secuencias de comandos de reglas. (CODE_EDITOR)

* Póngase en contacto con el equipo de asistencia para habilitar la funcionalidad de correo electrónico (abrir puerto SMTP) para su entorno. De forma predeterminada, solo están habilitadas las conexiones HTTP y HTTPS salientes. (EMAIL_SERVICE_CONFIGURATION)

* Utilice la acción de envío **[!UICONTROL Email]** en lugar de **[!UICONTROL Email PDF]**. La acción de envío **[!UICONTROL Email]** proporciona opciones para enviar archivos adjuntos y adjuntar el documento de registro (DoR) mediante correo electrónico. (EMAIL_PDF_SUBMIT_ACTION)

* No migre formularios adaptables basados en XDP a un entorno de Cloud Service. Tenga en cuenta las notas de la versión mensuales para ver la disponibilidad de las funciones. (XDP_BASED_FORM)

* Los datos enviados contienen un ID de acuerdo de firma. Puede utilizar el ID del contrato de firma para recuperar un PDF del contrato de firma, si es necesario.  (FORM_SIGN_INTEGRATION)

* Reemplace el paso Firma de los formularios adaptables con la opción Firmar un formulario adaptable después del envío, en la misma ventana. Le ayuda a seguir proporcionando una [experiencia de firma en el navegador](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). (SIGNATURE_STEP)

* Elimine el paso de verificación de los formularios adaptables existentes antes de mover dichos formularios a un entorno de Cloud Service. (VERIFY_STEP)

* No hay alternativa a la **[!UICONTROL acción de envío del portal de Forms]**. Puede utilizar esta acción de envío una vez lanzada la función Forms Portal para el Cloud Service. Tenga en cuenta las notas de la versión mensuales para ver la disponibilidad de las funciones. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL)

* No hay otra acción de envío alternativa a **[!UICONTROL Enviar a las acciones de envío del flujo de trabajo de Forms]**. Puede desarrollar una acción de envío personalizada para enviar datos, archivos adjuntos o documentos de registro (DoR) a un proceso de LiveCycle. (LC_WORKFLOW_SUBMISSION)

* No migre las comunicaciones interactivas, las cartas y los diccionarios relacionados a un entorno de Cloud Service. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Desactive la opción **[!UICONTROL Guardar como borrador]** y **[!UICONTROL Habilitar guardado automático]** en los formularios adaptables antes de migrarlos a Cloud Service. Puede activar estas opciones una vez que la función Forms Portal se haya lanzado para el Cloud Service. Consulte las notas de la versión mensuales para ver la disponibilidad de las funciones. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* No hay reemplazo para el acordeón de metadatos. Quítelo de los formularios antes de migrarlo a Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Utilice Google reCaptcha en lugar del servicio CAPTCHA proporcionado por Adobe Experience Manager. (FORMS_CAPTCHA)

Póngase en contacto con el [Soporte de Adobe](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
