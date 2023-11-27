---
title: Integración de Adobe Experience Cloud para el administrador de Commerce
description: Obtenga información acerca de la extensión de experiencia unificada de administración que integra Commerce con Experience Cloud para que los clientes puedan acceder a los proyectos de Commerce desde la página de inicio del Experience Cloud.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Integración de Adobe Experience Cloud para Commerce

{{ee-feature}}

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Integre proyectos de Adobe Commerce con Experience Cloud habilitando la extensión Admin Unified Experience. Cuando la integración está activa, los administradores pueden acceder a los proyectos de Commerce desde Adobe Experience Cloud.

![Acceso a Commerce desde la página de inicio del Experience Cloud](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Ver proyectos de Commerce disponibles

Los administradores pueden ver los proyectos de Commerce a los que tienen permiso de acceso seleccionando **[!UICONTROL Commerce]** en la página de inicio del Experience Cloud.

![Workspace de proyectos de Commerce en Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Los administradores pueden abrir Admin y Storefront para cada proyecto desde el [!DNL Commerce Projects] espacio de trabajo y vea información adicional.

- **Instantánea de la página principal de la tienda de Commerce**: instantánea de la página de inicio de la tienda. Si un proyecto tiene varios sitios web, la instantánea muestra la página de inicio del sitio predeterminado.

- **[Nombre del proyecto](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**: identifica el entorno del proyecto de nube para la instancia. El nombre predeterminado del proyecto es [Nombre de rama Git](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) en el proyecto de la nube. Cambie o actualice el nombre del proyecto en la [Ajustes de configuración del almacén de experiencia unificada](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[URL de tienda](../stores-purchase/store-urls.md)**: permite mostrar la URL base del sitio Web por defecto.

- **[Tipo de entorno](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**: las instancias de comercio implementadas en un entorno de ensayo o desarrollo se identifican con un [!UICONTROL Development] o [!UICONTROL Staging] etiqueta. Las instancias que no tienen una etiqueta se implementan en un entorno de producción.

- **Acceso de administrador de Commerce**: abra el Administrador haciendo clic en. **[!UICONTROL Open]**.

- **Acceso a tienda**: permite abrir la tienda seleccionando **[!UICONTROL Open storefront]** en el menú opciones.

- **Acceso rápido a proyectos seleccionados**—Seleccionar **[!UICONTROL Add to Favorites]** en el menú opciones para agregar un proyecto al [!UICONTROL Favorites] pestaña.

## Flujo de autenticación

Cuando la integración de Experience Cloud está habilitada, los administradores utilizan el siguiente flujo de trabajo para autenticarse y acceder a los proyectos de Commerce.

1. Inicie sesión a través de la página de inicio de sesión del Experience Cloud.

   ![Página de inicio de sesión del Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Los administradores deben iniciar sesión en Experience Cloud con el perfil empresarial de Adobe para la organización asociada a la instancia de Commerce. Consulte [Administración de perfiles de Adobe](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. En la página de inicio del Experience Cloud, abra [!UICONTROL Commerce Projects workspace] seleccionando **[!UICONTROL Open]**.

1. Acceda al administrador de un proyecto seleccionando **[!UICONTROL Open]**.

1. En la página Inicio de sesión de Adobe Commerce, seleccione **[!UICONTROL Sign in with Adobe ID]** para completar la autenticación y abrir el Administrador.

   ![Página de inicio de sesión de Adobe Commerce](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Consulte [Administración de la integración de Experience Cloud](admin-unified-experience-integration-manage.md) para obtener más información sobre cómo se ve afectado el flujo de trabajo de autenticación cuando la integración de Experience Cloud está habilitada o deshabilitada.

## Requisitos

- Adobe Commerce 2.4.5 o posterior
- Adobe Commerce en la infraestructura en la nube
- Extensiones de Adobe Commerce

   - Extensión de experiencia unificada de administración de Commerce (`magento/module-unified-experience`)

     Si el módulo no está disponible en la instancia de Commerce, se puede instalar mediante Composer.

   - [Servicio Eventos de Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/): necesario para enviar datos de evento para administrar el acceso de administrador a proyectos de Commerce desde Experience Cloud.

     La integración de Adobe I/O Events con Commerce se habilita mediante la extensión de Commerce Event (`magento/commerce-eventing`), que está disponible con Adobe Commerce 2.4.4 y versiones posteriores.

## Habilitar la integración

Habilite la integración siguiendo las instrucciones para [Configuración de la integración de Experience Cloud con el administrador de Commerce](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Si la integración de Experience Cloud ya está habilitada en la instancia de Commerce, consulte [Administración de la integración de Experience Cloud](admin-unified-experience-integration-manage.md) para obtener más información sobre cómo cambiar o actualizar la configuración, administrar el acceso de administrador y solucionar problemas.
