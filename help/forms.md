---
title: FORMULARIO
description: Página de ayuda de código de Pattern Detector
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: 5ba6a9a4b6da17bd78acdd82c955e296d8bbc994
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="Forms"
>abstract="El código de Forms identifica posibles problemas relacionados con la migración de Adobe Experience Manager Forms a Adobe Experience Manager Forms as a Cloud Service. Revise las posibles implicaciones y riesgos asociados y aborde estos problemas antes de migrar a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-pattern-detection/table-of-contents/forms.html#implications-and-risks" text="Posibles implicaciones y riesgos"

`FORMS` Identifica posibles problemas relacionados con la migración de [!DNL Adobe Experience Manager Forms] a [!DNL Adobe Experience Manager Form]s como [!DNL Cloud Service]. Solucionar estos problemas antes de migrar a [!DNL Cloud Service].

Los siguientes subtipos le ayudan a identificar los diferentes tipos de problemas:

* `modified.feature`: Estas funciones, recursos o API se actualizaron o modificaron para el Cloud Service. Antes de migrar al Cloud Service, ejecute la utilidad de migración para que estas funciones y recursos sean compatibles con el Cloud Service.
* `unavailable.feature`: Su entorno tiene características y recursos que no están disponibles ni se han eliminado del Cloud Service. No migre estas características o recursos a un entorno de Cloud Service.
* `unsupported.feature`: Su entorno utiliza algunas funciones que aún no son compatibles con el Cloud Service. No migre estas características o recursos a un entorno de Cloud Service. Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de las funciones.
* `unsupported.api`: Su entorno tiene algunas API que aún no son compatibles con el Cloud Service. Antes de migrar al Cloud Service, deshabilite, sustituya o elimine estas API de su código. Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de las funciones.

Consulte la [Posibles implicaciones y riesgos](#implications-and-risks) y [Posibles soluciones](#solutions) secciones para obtener información sobre los reemplazos y otras acciones necesarias para hacer que algunas funciones y API sean compatibles con el Cloud Service

## Posibles implicaciones y riesgos {#implications-and-risks}

Antes de migrar a [!DNL Adobe Experience Manager Forms as a Cloud Service]. Cuando no se abordan las implicaciones y riesgos que se enumeran a continuación, algunas funciones no funcionan como se espera en el entorno del Cloud Service.

* La funcionalidad del editor de código de la función del editor de reglas no está disponible. (CODE_EDITOR)

* La compatibilidad con el correo electrónico (puerto SMTP) está deshabilitada de forma predeterminada. (EMAIL_SERVICE_CONFIGURATION)

* La variable **[!UICONTROL PDF de correo electrónico]** Acción de envío no está disponible.(EMAIL_PDF_SUBMIT_ACTION)

* Forms adaptable basado en XFA aún no es compatible. (XFA_BASED_FORM, XDP_BASED_FORM)

* Se invoca una acción de envío inmediatamente al enviar el formulario, en lugar de esperar a que todos los firmantes completen la firma. Por lo tanto, el PDF del acuerdo de Adobe Sign enviado a los firmantes no está disponible para que las acciones de envío se utilicen o procesen. (FORM_SIGN_INTEGRATION)

* El paso Firma no está disponible. (SIGNATURE_STEP)

* El paso Verificar no está disponible. (VERIFY_STEP)

* La variable **[!UICONTROL Enviar al Forms Workflow]** Acción de envío no está disponible. En AEM 6.5 Forms y versiones anteriores, la acción de envío se utilizaba para enviar datos de formulario adaptables a AEM Forms heredado en flujos de trabajo y LiveCycles Workflow JEE. (LC_WORKFLOW_SUBMISSION)

* La capacidad de comunicaciones interactivas no está disponible.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* El acordeón de metadatos no está disponible. (METADATA_ACCORDION_FORM_CONTAINER)

* El componente CAPTCHA ahora utiliza el servicio reCAPTCHA de Google para validar CAPTCHA de forma predeterminada. La opción de usar Adobe Experience Manager para validar CAPTCHA está en desuso. (FORMS_CAPTCHA)

* [!DNL AEM Forms] la aplicación no está disponible para [!DNL Cloud Services]. (AEM_FORMS_APP)

* [Servicios de documentos](https://experienceleague.adobe.com/docs/experience-manager-65/forms/install-aem-forms/osgi-installation/install-configure-document-services.html?lang=en#deployment-topology) Los pasos no están disponibles en AEM Flujos de trabajo. (WORKFLOW_DOCSERVICES)

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Directrices de implementación"
>abstract="La información expuesta a través del código FORMS puede proporcionar instrucciones sobre los reemplazos y otras acciones necesarias para hacer algunas funciones y API compatibles con el Cloud Service. Póngase en contacto con la asistencia de Adobe para obtener ayuda y aclaraciones"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Asistencia al Experience Cloud"

* Utilice la utilidad de migración para convertir todas las secuencias de comandos de reglas del entorno en funciones reutilizables. Puede utilizar las funciones reutilizables con el editor de reglas visuales para seguir obteniendo resultados obtenidos con secuencias de comandos de reglas. (CODE_EDITOR)

* Póngase en contacto con el equipo de asistencia para habilitar la funcionalidad de correo electrónico (abrir puerto SMTP) para su entorno. De forma predeterminada, solo están habilitadas las conexiones HTTP y HTTPS salientes. (EMAIL_SERVICE_CONFIGURATION, paso de correo electrónico)

* Uso **[!UICONTROL Correo electrónico]** Enviar acción en lugar de **[!UICONTROL PDF de correo electrónico]**. La variable **[!UICONTROL Correo electrónico]** Acción de envío proporciona opciones para enviar archivos adjuntos y adjuntar el documento de registro (DoR) mediante correo electrónico. (EMAIL_PDF_SUBMIT_ACTION)

* Los datos enviados contienen un ID de acuerdo de Adobe Sign. Puede utilizar el ID del contrato de firma para recuperar un PDF del contrato de firma, si es necesario.  (FORM_SIGN_INTEGRATION)

* Elimine el paso Firma de un formulario adaptable existente. Configure el formulario adaptable para usar [experiencia de firma en el navegador](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Muestra el acuerdo de Adobe Sign para firmar el acuerdo dentro del explorador al enviar un formulario adaptable. La experiencia de firma en el navegador ayuda a proporcionar una experiencia de firma más rápida y ahorra tiempo para el firmante. (SIGNATURE_STEP)

* Elimine el paso de verificación de la Forms adaptable existente antes de mover estos formularios a una [!DNL Cloud Service] entorno. (VERIFY_STEP)

* Modifique los formularios adaptables existentes para utilizar [Enviar al extremo REST](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-to-rest-endpoint), [Enviar correo electrónico](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#send-email), [Enviar mediante el modelo de datos de formulario](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-using-form-data-model)y [Invocar un flujo de trabajo AEM](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Enviar acciones.

* Puede desarrollar un flujo de trabajo AEM y modificar los formularios adaptables existentes para su uso [Flujo de trabajo AEM](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Enviar acción para enviar datos a un flujo de trabajo AEM en lugar de usar la variable **[!UICONTROL Enviar al Forms Workflow]** Enviar acción. Puede desarrollar una acción de envío personalizada para enviar datos, archivos adjuntos o un documento de registro (DoR) a un proceso de LiveCycle en lugar de usar la variable [!UICONTROL Enviar al Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de la función de comunicaciones interactivas. No migre las comunicaciones interactivas, las cartas y los diccionarios relacionados a un entorno de Cloud Service hasta que la función no esté disponible. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* No hay reemplazo para el acordeón de metadatos. Quítelo de los formularios antes de migrarlo a Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Utilice Google reCaptcha en lugar del servicio CAPTCHA proporcionado por Adobe Experience Manager. (FORMS_CAPTCHA)

* No migre un modelo de flujo de trabajo AEM que utilice un paso de flujo de trabajo de servicios de documentos . Tampoco migre ni actualice Forms adaptable que envíe datos de usuario a un modelo de flujo de trabajo que utilice los pasos del flujo de trabajo de servicios de documentos ni cambie la acción de envío a un [compatible con uno](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html) antes de migrar el formulario. (WORKFLOW_DOCSERVICES)

* Forms adaptable ofrece un diseño interactivo. Estos formularios cambian el aspecto, el diseño y la interactividad en función del dispositivo subyacente. Puede seguir utilizando Forms adaptable en dispositivos móviles. Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de la variable [!DNL AEM Forms] aplicación. (AEM_FORMS_APP)

* La compatibilidad con Forms adaptable basado en XFA no está disponible de forma predeterminada. Si tiene intención de utilizar Forms adaptable basado en XFA, póngase en contacto con el servicio de asistencia al Adobe con detalles de su caso de uso y requisitos específicos.(XFA_BASED_FORM, XDP_BASED_FORM)

Póngase en contacto con [Compatibilidad con Adobe](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o para solucionar problemas.
