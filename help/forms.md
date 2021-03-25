---
title: FORMULARIO
description: Página de ayuda de código de Pattern Detector
translation-type: tm+mt
source-git-commit: 9a02482d023ce1a6cbbff24b8e6509c91ddd2a6b
workflow-type: tm+mt
source-wordcount: '1136'
ht-degree: 0%

---


# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Fondo {#background}

`FORMS` Identifica posibles problemas relacionados con la migración de  [!DNL Adobe Experience Manager Forms] a  [!DNL Adobe Experience Manager Form]s como un  [!DNL Cloud Service]. Solucione estos problemas antes de migrar a [!DNL Cloud Service].

Los siguientes subtipos le ayudan a identificar los diferentes tipos de problemas:

* `modified.feature`: Estas funciones, recursos o API se actualizaron o modificaron para el Cloud Service. Antes de migrar al Cloud Service, ejecute la utilidad de migración para que estas funciones y recursos sean compatibles con el Cloud Service.
* `unavailable.feature`: Su entorno tiene características y recursos que no están disponibles ni se han eliminado del Cloud Service. No migre estas características o recursos a un entorno de Cloud Service.
* `unsupported.feature`: Su entorno utiliza algunas funciones que aún no son compatibles con el Cloud Service. No migre estas características o recursos a un entorno de Cloud Service. Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de las funciones.
* `unsupported.api`: Su entorno tiene algunas API que aún no son compatibles con el Cloud Service. Antes de migrar al Cloud Service, deshabilite, sustituya o elimine estas API de su código. Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de las funciones.

Consulte las secciones [Posibles implicaciones y riesgos](#implications-and-risks) y [Posibles soluciones](#solutions) para obtener información sobre los reemplazos y otras acciones necesarias para hacer que algunas funciones y API sean compatibles con el Cloud Service

## Posibles implicaciones y riesgos {#implications-and-risks}

Solucione los siguientes problemas antes de migrar a [!DNL Adobe Experience Manager Forms as a Cloud Service]. Cuando no se abordan las implicaciones y riesgos que se enumeran a continuación, algunas funciones no funcionan como se espera en el entorno del Cloud Service.

* La funcionalidad del editor de código de la función del editor de reglas no está disponible. (CODE_EDITOR)

* La compatibilidad con el correo electrónico (puerto SMTP) está deshabilitada de forma predeterminada. (EMAIL_SERVICE_CONFIGURATION)

* La acción de envío **[!UICONTROL Email PDF]** no está disponible.(EMAIL_PDF_SUBMIT_ACTION)

* Forms adaptable basado en XFA aún no es compatible. (XFA_BASED_FORM, XDP_BASED_FORM)

* Se invoca una acción de envío inmediatamente al enviar el formulario, en lugar de esperar a que todos los firmantes completen la firma. Por lo tanto, el PDF del acuerdo de Adobe Sign enviado a los firmantes no está disponible para que las acciones de envío se utilicen o procesen. (FORM_SIGN_INTEGRATION)

* El paso Firma no está disponible. (SIGNATURE_STEP)

* El paso Verificar no está disponible. (VERIFY_STEP)

* La función Portal de Forms y **[!UICONTROL Acción de envío del portal de Forms]** aún no están disponibles. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* La acción de envío **[!UICONTROL Submit to Forms Workflow]** no está disponible. En [!DNL AEM 6.5 Forms] y versiones anteriores, la acción de envío se utilizaba para enviar datos de formulario adaptables a los flujos de trabajo y LiveCycles Workflow [!DNL AEM Forms on JEE] heredados. (LC_WORKFLOW_SUBMISSION)

* La capacidad de comunicaciones interactivas no está disponible.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL Guardar como]** borrador y las funciones de formulario adaptable  **[!UICONTROL de]** guardado automático no son compatibles actualmente. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* El acordeón de metadatos no está disponible. (METADATA_ACCORDION_FORM_CONTAINER)

* El componente CAPTCHA ahora utiliza el servicio Google reCAPTCHA para validar CAPTCHA de forma predeterminada. La opción de usar Adobe Experience Manager para validar CAPTCHA está en desuso. (FORMS_CAPTCHA)

* [!DNL AEM Forms] no está disponible para  [!DNL Cloud Services]. (AEM_FORMS_APP)

* [Los ](https://experienceleague.adobe.com/docs/experience-manager-65/forms/install-aem-forms/osgi-installation/install-configure-document-services.html?lang=en#deployment-topology) pasos de Document Services no están disponibles en AEM Flujos de trabajo. (WORKFLOW_DOCSERVICES)

## Posibles soluciones {#solutions}

* Utilice la utilidad de migración para convertir todas las secuencias de comandos de reglas del entorno en funciones reutilizables. Puede utilizar las funciones reutilizables con el editor de reglas visuales para seguir obteniendo resultados obtenidos con secuencias de comandos de reglas. (CODE_EDITOR)

* Póngase en contacto con el equipo de asistencia para habilitar la funcionalidad de correo electrónico (abrir puerto SMTP) para su entorno. De forma predeterminada, solo están habilitadas las conexiones HTTP y HTTPS salientes. (EMAIL_SERVICE_CONFIGURATION, paso de correo electrónico)

* Utilice **[!UICONTROL Correo electrónico]** Enviar acción en lugar de **[!UICONTROL Correo electrónico PDF]**. La acción de envío de **[!UICONTROL correo electrónico]** proporciona opciones para enviar archivos adjuntos y adjuntar el documento de registro (DoR) mediante correo electrónico. (EMAIL_PDF_SUBMIT_ACTION)

* Los datos enviados contienen un ID de acuerdo de Adobe Sign. Puede utilizar el ID del contrato de firma para recuperar un PDF del contrato de firma, si es necesario.  (FORM_SIGN_INTEGRATION)

* Elimine el paso Firma de un formulario adaptable existente. Configure el formulario adaptable para utilizar [la experiencia de firma en el navegador](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Muestra el acuerdo de Adobe Sign para firmar el acuerdo dentro del explorador al enviar un formulario adaptable. La experiencia de firma en el navegador ayuda a proporcionar una experiencia de firma más rápida y ahorra tiempo para el firmante. (SIGNATURE_STEP)

* Elimine el paso de verificación de la Forms adaptable existente antes de mover estos formularios a un entorno [!DNL Cloud Service]. (VERIFY_STEP)

* Modifique los formularios adaptables existentes para utilizar [Submit to REST endpoint](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-to-rest-endpoint), [Send email](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#send-email), [Submit using Form Data Model](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-using-form-data-model) e [Invoke an AEM Workflow](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Submit Actions. La acción de envío del portal de Forms y del portal de Forms aún no están disponibles. Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de las funciones. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL)

* Puede desarrollar un flujo de trabajo AEM y modificar los formularios adaptables existentes para utilizar [AEM Workflow](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Enviar acción para enviar datos a un flujo de trabajo AEM en lugar de utilizar la acción de envío **[!UICONTROL Enviar al Forms Workflow]**. Puede desarrollar una acción de envío personalizada para enviar datos, archivos adjuntos o documentos de registro (DoR) a un proceso de LiveCycle en lugar de utilizar [!UICONTROL Enviar al Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de la función de comunicaciones interactivas. No migre las comunicaciones interactivas, las cartas y los diccionarios relacionados a un entorno de Cloud Service hasta que la función no esté disponible. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Desactive la opción **[!UICONTROL Guardar como borrador]** y **[!UICONTROL Habilitar guardado automático]** en su Forms adaptable antes de migrarlas a Cloud Service. Puede activar estas opciones una vez que la función Forms Portal se haya lanzado para el Cloud Service. Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de las funciones. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* No hay reemplazo para el acordeón de metadatos. Quítelo de los formularios antes de migrarlo a Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Utilice Google reCaptcha en lugar del servicio CAPTCHA proporcionado por Adobe Experience Manager. (FORMS_CAPTCHA)

* Forms adaptable ofrece un diseño interactivo. Estos formularios cambian el aspecto, el diseño y la interactividad en función del dispositivo subyacente. Puede seguir utilizando Forms adaptable en dispositivos móviles. Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de la aplicación [!DNL AEM Forms]. (AEM_FORMS_APP)

* No migre un modelo de flujo de trabajo AEM que utilice un paso de flujo de trabajo de servicios de documentos . Además, no migre ni actualice Forms adaptable que envíe datos de usuario a un modelo de flujo de trabajo que utilice los pasos del flujo de trabajo de servicios de documentos o cambie la acción de envío a una [compatible](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html) antes de migrar el formulario. (WORKFLOW_DOCSERVICES)

* La compatibilidad con Forms adaptable basado en XFA no está disponible de forma predeterminada. Si tiene intención de utilizar Forms adaptable basado en XFA, póngase en contacto con el servicio de asistencia al Adobe con detalles de su caso de uso y requisitos específicos.((XFA_BASED_FORM, XDP_BASED_FORM)

Póngase en contacto con el [Soporte de Adobe](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
