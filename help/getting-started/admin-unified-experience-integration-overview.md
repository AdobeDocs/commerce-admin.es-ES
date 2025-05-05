---
title: Integración de Adobe Experience Cloud para el administrador de Commerce
description: Obtenga información acerca de la extensión de experiencia unificada de administración que integra Commerce con Experience Cloud para que los clientes puedan acceder a los proyectos de Commerce desde la página de inicio del Experience Cloud.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: 61874f3dac4f574ad393e8ae258f3d6c56c8f37e
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Integración de Adobe Experience Cloud para Commerce

<table style="border:1px solid red">
<tr><td><img alt="Función Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Característica exclusiva solamente en Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=es#product-editions">Más información</a>)</td></tr>
</table>

Integre proyectos de Adobe Commerce con Experience Cloud habilitando la extensión Admin Unified Experience. Cuando la integración está activa, los administradores pueden acceder a los proyectos de Commerce desde Adobe Experience Cloud.

![Acceder a Commerce desde la página de inicio del Experience Cloud](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Ver proyectos de Commerce disponibles

Los administradores pueden ver los proyectos de Commerce para los que tienen permiso de acceso seleccionando **[!UICONTROL Commerce]** en la página de inicio del Experience Cloud.

![Espacio de trabajo de proyectos de Commerce en Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Los administradores pueden abrir el Administrador y la Tienda para cada proyecto desde el área de trabajo [!DNL Commerce Projects] y ver información adicional.

- **Instantánea de la página principal de la tienda Commerce**: instantánea de la página principal de la tienda. Si un proyecto tiene varios sitios web, la instantánea muestra la página de inicio del sitio predeterminado.

- **[Nombre del proyecto](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=es)**: identifica el entorno del proyecto de nube para la instancia. El nombre del proyecto toma como valor predeterminado [nombre de la rama Git](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html?lang=es) en el proyecto de nube. Cambie o actualice el nombre del proyecto en [Ajustes de configuración de almacén de experiencia unificada](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[URL de tienda](../stores-purchase/store-urls.md)**: muestra la dirección URL base del sitio web predeterminado.

- **[Tipo de entorno](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=es)**: las instancias de Commerce implementadas en un entorno de ensayo o desarrollo se identifican con una etiqueta [!UICONTROL Development] o [!UICONTROL Staging]. Las instancias que no tienen una etiqueta se implementan en un entorno de producción.

- **Acceso de administrador de Commerce**: abra el administrador haciendo clic en **[!UICONTROL Open]**.

- **Acceso a tienda**: abre la tienda seleccionando **[!UICONTROL Open storefront]** en el menú de opciones.

- **Acceso rápido para seleccionar proyectos**—Seleccione **[!UICONTROL Add to Favorites]** del menú de opciones para agregar un proyecto a la ficha [!UICONTROL Favorites].

## Flujo de autenticación

Cuando la integración de Experience Cloud está habilitada, los administradores utilizan el siguiente flujo de trabajo para autenticarse y acceder a los proyectos de Commerce.

1. Inicie sesión a través de la página de inicio de sesión del Experience Cloud.

   ![Página de inicio de sesión de Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Los administradores deben iniciar sesión en Experience Cloud con el perfil empresarial de Adobe para la organización asociada a la instancia de Commerce. Consulte [Administrar perfiles de Adobe](https://helpx.adobe.com/es/enterprise/using/manage-adobe-profiles.html).

1. En la página de inicio del Experience Cloud, abra [!UICONTROL Commerce Projects workspace] seleccionando **[!UICONTROL Open]**.

1. Para acceder al administrador de un proyecto, seleccione **[!UICONTROL Open]**.

1. En la página Inicio de sesión de Adobe Commerce, seleccione **[!UICONTROL Sign in with Adobe ID]** para completar la autenticación y abrir el Administrador.

   ![Página de inicio de sesión de Adobe Commerce](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Consulte [Administrar la integración de Experience Cloud](admin-unified-experience-integration-manage.md) para obtener detalles sobre cómo se ve afectado el flujo de trabajo de autenticación cuando la integración de Experience Cloud está habilitada o deshabilitada.

## Requisitos

- Adobe Commerce 2.4.5 o posterior
- Adobe Commerce en la infraestructura en la nube
- Extensiones de Adobe Commerce

   - Extensión de experiencia unificada de administración de Commerce (`magento/module-unified-experience`)

     Si el módulo no está disponible en la instancia de Commerce, se puede instalar mediante Composer.

   - [Servicio de eventos de Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/): necesario para enviar datos de evento a fin de administrar el acceso de administrador a proyectos de Commerce desde Experience Cloud.

     La integración de eventos de Adobe I/O con Commerce está habilitada por la extensión de eventos de Commerce (`magento/commerce-eventing`), que está disponible con Adobe Commerce 2.4.4 y versiones posteriores.

## Habilitar la integración

Habilite la integración siguiendo las instrucciones para [configurar la integración de Experience Cloud con el administrador de Commerce](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Si la integración de Experience Cloud ya está habilitada en la instancia de Commerce, consulte [Administrar la integración de Experience Cloud](admin-unified-experience-integration-manage.md) para obtener detalles acerca de cómo cambiar o actualizar la configuración, administrar el acceso de administrador y solucionar problemas.
