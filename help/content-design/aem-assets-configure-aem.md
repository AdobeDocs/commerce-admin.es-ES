---
title: Configuración de Experience Manager Assets
description: Añada los metadatos de recursos necesarios para permitir que la integración de AEM Assets para Commerce sincronice recursos entre proyectos de Adobe Commerce y Experience Manager Assets.
feature: CMS, Media, Integration
source-git-commit: f04648a41fc16154d5f10278f810114d707b670c
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Configuración de Experience Manager Assets

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Para administrar los recursos de medios de su tienda mediante la integración de AEM Assets para Commerce, su proyecto de AEM Assets requiere agregar ciertos metadatos para garantizar que pueda buscar y administrar fácilmente los recursos de Commerce. Estos metadatos también facilitan la sincronización de recursos entre Adobe Commerce y Experience Manager Assets. Después de definir los campos de metadatos, la asignación inicial de estos campos se produce automáticamente la primera vez que se comparte un recurso de Commerce con Experience Manager Assets.

Para la integración, se configuran dos tipos de metadatos:

- **[El perfil de metadatos](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles)** le permite aplicar metadatos predeterminados a los recursos de una carpeta. Todos los recursos de la carpeta heredan los metadatos predeterminados configurados en el perfil.

- AEM **[El esquema de metadatos](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas)** define el diseño de la página de propiedades y el conjunto de campos que se pueden usar como propiedades de metadatos en un recurso de.

## Configuración de metadatos

Para la incorporación inicial, añada los siguientes metadatos de Commerce a un perfil de metadatos de AEM Assets y a un esquema de metadatos.

| Tipo de campo | Etiqueta | Propiedad | Valor predeterminado |
|------ | ------- | ---------- | ------------- |
| Texto | **¿Existe en Adobe Commerce?** | `./jcr:content/metadata/commerce:isCommerce` | yes |
| Texto con varios valores | **SKU** | `./jcr:content/metadata/commerce:skus` | ninguno |
| Texto con varios valores | **Posiciones** | `./jcr:content/metadata/commerce:positions` | ninguno |
| Texto con varios valores | **Roles** | `./jcr:content/metadata/commerce:roles` | ninguno |


### Añadir campos de Commerce a un perfil de metadatos

1. En Adobe Experience Manager Workspace, vaya al espacio de trabajo de administración de contenido de autor para AEM Assets haciendo clic en el icono Adobe Experience Manager.

   ![Creación de AEM Assets](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Abra las Herramientas de administración seleccionando el icono de martillo.

   AEM ![Administrador de autor de administra perfiles de metadatos](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Abra la página de configuración del perfil haciendo clic en **[!UICONTROL Metadata Profiles]**.

1. **[!UICONTROL Create]** un perfil de metadatos para la integración de Commerce.

   AEM ![Administrador de autor de agrega perfiles de metadatos ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Agregue una pestaña para los metadatos de Commerce.

   1. A la izquierda, haga clic en **[!UICONTROL Settings]**.

   1. Haga clic en **[!UICONTROL +]** en la sección de la ficha y, a continuación, especifique **[!UICONTROL Tab Name]**, `Commerce`.

1. Agregue los [campos de metadatos](#configure-metadata) al formulario.

   AEM ![Administrador de autor de agrega campos de metadatos al perfil](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Guarde la actualización.

1. Aplicar el perfil de metadatos `Commerce integration` a la carpeta donde se almacenan los recursos de Commerce.

   1. En la página [!UICONTROL  Metadata Profiles], seleccione el perfil de integración de Commerce.

   1. En el menú de acción, seleccione **[!UICONTROL Apply Metadata Profiles to Folder(s)]**.

   1. Seleccione la carpeta que contiene los recursos de Commerce.

      Cree una carpeta de Commerce si no existe.

   1. Haga clic en **[!UICONTROL Apply]**.

### Agregar campos de Commerce a un formulario de esquema de metadatos

1. AEM En el panel Administración de contenido de autor de la para Assets, abra **[!UICONTROL Metadata Schemas]** ([!UICONTROL Manage metadata schema forms]).

   AEM ![Esquema de metadatos de actualización de administración de autor de](./assets/aem-assets-manage-metadata-schema.png){width="600" zoomable="yes"}

1. **[!UICONTROL Create]** creó un esquema de metadatos para Commerce.

   AEM ![Esquema de metadatos de actualización de administración de autor de](./assets/aem-assets-create-metadata-schema.png){width="600" zoomable="yes"}

1. En [!UICONTROL Metadata Schema Form], cree los campos `Does Commerce exist?` y `Commerce mappings` y asigne las propiedades.

1. Haga clic en **[!UICONTROL Save]**.


## Publish un recurso

AEM Después de configurar los metadatos y el perfil de esquema de los recursos de Commerce, cree el primer recurso de Commerce para asignar los campos de metadatos de Commerce.

1. Desde el Experience Manager, ve a [!UICONTROL Assets > Files] y selecciona la carpeta **Commerce**.

1. Cargue una imagen para un proyecto de Commerce arrastrando el archivo a la carpeta o haciendo clic en **[!UICONTROL Add Assets]**.

1. Compruebe la configuración de metadatos: **isCommerce** está establecido en `true` y que la propiedad `commerce:skus` está establecida en el SKU del producto de Commerce asociado a la imagen.

1. Apruebe el recurso.


## Añadir un recurso a la carpeta de Commerce

Cree al menos un recurso en la carpeta Commerce de AEM Assets que tenga asignados los atributos de metadatos de Commerce.

Este recurso es necesario para configurar la sincronización entre la instancia de Commerce y AEM Assets.

## Asignar metadatos a los recursos

Los metadatos se asignan cuando se publica un recurso de Commerce por primera vez.  de Commerce por primera vez. Los recursos de medios que tienen los campos integrados o personalizados se asignan automáticamente a los campos especificados la primera vez que se envía un recurso a Experience Manager Assets.

Antes de comenzar la asignación de recursos, complete las siguientes tareas:

- [Instalación y configuración de la integración de AEM Assets para Commerce](aem-assets-configure-commerce.md)
- [Configure los servicios de sincronización para transferir recursos entre el entorno del proyecto de Adobe Commerce y el entorno del proyecto de AEM Assets](aem-assets-setup-synchronization.md)
