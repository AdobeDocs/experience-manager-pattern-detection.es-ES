---
title: FORM
description: Página de ayuda de código del detector de patrones.
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 85%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Fondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="FORMS"
>abstract="El código Forms identifica posibles problemas relacionados con la migración de Forms (Adobe Experience Manager) de la aplicación de la plataforma de migración de la plataforma de datos de AEM a la plataforma de AEM Forms as a Cloud Service. Revise las posibles implicaciones y riesgos asociados y aborde estos problemas antes de migrar a Cloud Service."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-manager-pattern-detection/table-of-contents/forms#implications-and-risks" text="Posibles implicaciones y riesgos"

`FORMS` Identifica posibles problemas relacionados con la migración de [!DNL Adobe Experience Manager Forms] a [!DNL Adobe Experience Manager Forms] como [!DNL Cloud Service]. Solucionar estos problemas antes de migrar a [!DNL Cloud Service].

Los siguientes subtipos le ayudan a identificar los diferentes tipos de problemas:

* `modified.feature`: estas funciones, activos o API se actualizaron o modificaron para Cloud Service. Antes de migrar a Cloud Service, ejecute la utilidad de migración para que estas funciones y activos sean compatibles con Cloud Service.
* `unavailable.feature`: su entorno tiene características y activos que no están disponibles ni se han eliminado de Cloud Service. No migre estas características o activos a un entorno de Cloud Service.
* `unsupported.feature`: su entorno utiliza algunas funciones que aún no son compatibles con Cloud Service. No migre estas características o activos a un entorno de Cloud Service. Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de las funciones.
* `unsupported.api`: su entorno tiene algunas API que aún no son compatibles con Cloud Service. Antes de migrar a Cloud Service, deshabilite, sustituya o elimine estas API de su código. Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de las funciones.

Consulte las secciones de [Posibles implicaciones y riesgos](#implications-and-risks) y [Posibles soluciones](#solutions) para obtener información sobre los reemplazos y otras acciones necesarias para hacer que algunas funciones y API sean compatibles con Cloud Service

## Posibles implicaciones y riesgos {#implications-and-risks}

Aborde los siguientes problemas, antes de migrar a [!DNL Adobe Experience Manager Forms as a Cloud Service]. Cuando no se abordan las implicaciones y riesgos que se enumeran a continuación, algunas funciones no trabajan como se espera en el entorno de Cloud Service.

* La funcionalidad del editor de código de la función del editor de reglas no está disponible. (CODE_EDITOR)

* La compatibilidad con el correo electrónico (puerto SMTP) está deshabilitada de forma predeterminada. (EMAIL_SERVICE_CONFIGURATION)

* La acción de envío de **[!UICONTROL PDF de correo electrónico]** no está disponible. (EMAIL_PDF_SUBMIT_ACTION)

* Los formularios adaptables basados en XFA aún no son compatibles. (XFA_BASED_FORM, XDP_BASED_FORM)

* Se invoca una acción de envío inmediatamente al enviar el formulario, en lugar de esperar a que todos los firmantes completen la firma. Por lo tanto, el PDF del acuerdo de Adobe Acrobat Sign enviado a los firmantes no está disponible para que las acciones de envío se utilicen o procesen. (FORM_SIGN_INTEGRATION)

* El paso Firma no está disponible. (SIGNATURE_STEP)

* El paso Verificar no está disponible. (VERIFY_STEP)

* La acción de envío **[!UICONTROL Enviar a Forms Workflow]** no está disponible. AEM En Forms 6.5 y versiones anteriores, la acción de envío se utilizaba para enviar datos de formulario adaptable a AEM Forms heredado en flujos de trabajo y LiveCycles Workflow JEE. (LC_WORKFLOW_SUBMISSION)

* La capacidad de comunicaciones interactivas no está disponible.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* El acordeón de metadatos no está disponible. (METADATA_ACCORDION_FORM_CONTAINER)

* El componente CAPTCHA ahora utiliza el servicio reCAPTCHA de Google para validar CAPTCHA de forma predeterminada. La opción de usar Adobe Experience Manager para validar el Captcha está en desuso. (FORMS_CAPTCHA)

* La aplicación [!DNL AEM Forms] no está disponible para [!DNL Cloud Services]. (AEM_FORMS_APP)

* Los pasos de [Servicios de documentos](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/forms/install-aem-forms/osgi-installation/install-configure-document-services#deployment-topology) no están disponibles en flujos de trabajo de AEM. (WORKFLOW_DOCSERVICES)

## Posibles soluciones {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Directrices de implementación"
>abstract="La información expuesta a través del código Forms puede proporcionar instrucciones acerca de los reemplazos y otras acciones necesarias para hacer algunas funciones y API compatibles con Cloud Service. Póngase en contacto con el equipo de soporte de Adobe para obtener ayuda o aclaraciones."
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Soporte de Experience Cloud"

* Utilice una utilidad de migración para convertir todas las secuencias de comandos de reglas del entorno en funciones reutilizables. Puede utilizar las funciones reutilizables con el Editor de reglas visuales para seguir obteniendo resultados con secuencias de comandos de reglas. (CODE_EDITOR)

* Póngase en contacto con el Equipo de Soporte para que habiliten la funcionalidad de correo electrónico (abrir puerto SMTP) para su entorno. De forma predeterminada, solo están habilitadas las conexiones HTTP y HTTPS salientes. (EMAIL_SERVICE_CONFIGURATION, paso de correo electrónico)

* Use la acción de envío **[!UICONTROL Correo electrónico]** en lugar de **[!UICONTROL PDF de correo electrónico]**. La acción de envío **[!UICONTROL Correo electrónico]** proporciona opciones para enviar archivos adjuntos y adjuntar el documento de registro (DoR) mediante correo electrónico. (EMAIL_PDF_SUBMIT_ACTION)

* Los datos enviados contienen un ID de acuerdo de Adobe Acrobat Sign. Puede utilizar el ID del acuerdo de Sign para recuperar un PDF del contrato de Sign, si es necesario.  (FORM_SIGN_INTEGRATION)

* Elimine el paso Firma de un formulario adaptable existente. Configure el formulario adaptable para utilizar un [experiencia de firma en el explorador](https://blog.developer.adobe.com/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Muestra el acuerdo de Adobe Sign para firmarlo en el explorador al enviar un formulario adaptable. La experiencia de firma en el explorador ayuda a proporcionar una experiencia de firma más rápida y ahorra tiempo para el firmante. (SIGNATURE_STEP)

* Quite el paso de verificación de sus formularios adaptables existentes antes de trasladar dichos formularios a un entorno de [!DNL Cloud Service]. (VERIFY_STEP)

* Edite los formularios adaptables existentes para utilizar las acciones de envío [Enviar al punto final REST](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-to-rest-endpoint), [Enviar correo electrónico](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#send-email), [Enviar mediante el modelo de datos de formulario](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-using-form-data-model) e [Invocar un flujo de trabajo de AEM](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow).

* Puede desarrollar un flujo de trabajo de AEM y modificar los formularios adaptables existentes para utilizar la acción de envío [Flujo de trabajo de AEM](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) y enviar datos a un flujo de trabajo de AEM en lugar de usar **[!UICONTROL Enviar a Forms Workflow]**. Puede desarrollar una acción de envío personalizada para enviar datos, archivos adjuntos o un documento de registro (DoR) a un proceso de LiveCycle en lugar de usar [!UICONTROL Enviar a Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de la función de comunicaciones interactivas. No migre las comunicaciones interactivas, las cartas y los diccionarios relacionados a un entorno de Cloud Service hasta que la función no esté disponible. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* No hay reemplazo para el acordeón de metadatos. Quítelo de los formularios antes de migrarlos a Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Utilice Google reCAPTCHA en lugar del servicio CAPTCHA proporcionado por Adobe Experience Manager. (FORMS_CAPTCHA)

* AEM No migre a un modelo de flujo de trabajo de que utilice un paso de flujo de trabajo de servicios de documentos. Tampoco migre ni actualice formularios adaptables que envíen datos de usuario a un modelo de flujo de trabajo que utilice los pasos del flujo de trabajo de servicios de documentos ni cambie `Submit Action` a [una compatible](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions) antes de migrar el formulario. (WORKFLOW_DOCSERVICES)

* Los formularios adaptables ofrecen un diseño interactivo. Estos formularios cambian el aspecto, el diseño y la interactividad en función del dispositivo subyacente. Puede seguir utilizando Forms adaptable en un dispositivo móvil. Busque las notas de la versión mensuales para obtener información sobre la disponibilidad de la [!DNL AEM Forms] aplicación. (AEM_FORMS_APP)

* La compatibilidad con formularios adaptables basados en XFA no está disponible de forma predeterminada. Si tiene intención de utilizar formularios adaptables basados en XFA, póngase en contacto con el servicio de soporte de Adobe e incluya información sobre su caso de uso y los requisitos específicos en el mensaje.(XFA_BASED_FORM, XDP_BASED_FORM)

Póngase en contacto con el [Equipo de soporte de Adobe](https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html) para obtener aclaraciones o resolver dudas.
