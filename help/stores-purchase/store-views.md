---
title: Vistas de tienda
description: Aprenda a añadir y editar una vista de tienda en Adobe Commerce, que permite a los compradores cambiar de configuración regional utilizando el selector de idioma en el encabezado de la tienda.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
TQID: https://experienceleague.adobe.com/2VMBTnzG3lqsNEyx-e46rqDs1wHofaDeHL3j3SuqxOE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: bc4baccc4b40fb7ecdc7f489bfaf3c797881db88
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%
---
# Vistas de tienda

Las vistas de tienda se suelen utilizar para que la tienda esté disponible en diferentes configuraciones regionales. Los compradores pueden utilizar el selector de idioma en el encabezado de la tienda para cambiar la vista de la tienda.

![Ámbito: vistas de varias tiendas](./assets/scope-multiview.svg){width="550"}

## [!DNL Adobe Commerce Optimizer] estado de sincronización {#optimizer-sync-status}

Si [!DNL Adobe Commerce Optimizer Connector] está instalado y habilitado para un sitio web o una vista de tienda, la cuadrícula [!UICONTROL All Stores] muestra un indicador de estado de sincronización. Si está instalado [!DNL Adobe Commerce Optimizer Connector for B2B], los datos también se sincronizan para los catálogos compartidos B2B disponibles. Consulte [Administrar vistas de catálogo](../b2b/catalog-views-manage.md).

| Columna | Indicador | Descripción |
| ----- | ----- | ----- |
| [!UICONTROL Web Site] | [!UICONTROL Price sync enabled for Commerce Optimizer] | Los precios y los libros de precios de este sitio web están sincronizados con [!DNL Adobe Commerce Optimizer]. |
| [!UICONTROL Store View] | [!UICONTROL Product sync enabled for Commerce Optimizer] | Los productos y atributos de esta vista de tienda se sincronizan con [!DNL Adobe Commerce Optimizer]. |

![Cuadrícula de todas las tiendas con indicadores de sincronización de Adobe Commerce Optimizer](./assets/stores-all-optimizer-sync.png){width="700" zoomable="yes"}

Para habilitar o deshabilitar la sincronización, edite **[!UICONTROL Adobe Commerce Optimizer exporter settings]** al [crear un sitio web](stores.md#step-1-create-a-website) o [agregar una vista de tienda](#add-a-store-view), o al actualizar un sitio web o una vista de tienda existente.

## Agregar una vista de tienda

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![Todas las tiendas](./assets/stores-all.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Create Store View]**.

   ![Crear vista de tienda](./assets/create-store-view.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Store]** en el almacén principal de esta vista.

1. Escriba un **[!UICONTROL Name]** para esta vista de tienda.

   El nombre aparece en el selector de idioma del encabezado de la tienda. Por ejemplo: `Spanish`.

1. Para **[!UICONTROL Code]**, escriba el código que identifica la vista (en caracteres en minúsculas).

   Por ejemplo: `spanish`.

1. Para activar la vista, establezca **[!UICONTROL Status]** en `Enabled`.

1. (Opcional) Escriba un número **[!UICONTROL Sort Order]** para determinar la secuencia en la que esta vista se muestra con otras vistas.

1. (Opcional) Si [!DNL Adobe Commerce Optimizer Connector] está instalado, seleccione **[!UICONTROL Sync products and attributes]** en la sección **[!UICONTROL Adobe Commerce Optimizer exporter settings]** para sincronizar los productos y atributos de esta vista de tienda con [!DNL Adobe Commerce Optimizer]. Si [!DNL Adobe Commerce Optimizer Connector for B2B] también está instalado, esta opción sincroniza también los datos del catálogo compartido B2B con [!DNL Adobe Commerce Optimizer]. Consulte [Administrar vistas de catálogo](../b2b/catalog-views-manage.md).

   ![Crear vista de tienda - Configuración del exportador de Adobe Commerce Optimizer](./assets/stores-optimizer-export-settings.png){width="600" zoomable="yes"}

   Cambiar esta configuración después de la sincronización inicial déclencheur una reindexación completa. Consulte [Personalizar la configuración de exportación de los ámbitos de Commerce](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/get-started#customize-the-commerce-scopes-export-configuration) en la *Guía del conector de Adobe Commerce Optimizer*.

1. Haga clic en **[!UICONTROL Save Store View]**.

## Editar una vista de tienda

Dado que el nombre de la vista aparece en el selector de idioma, puede que desee cambiar el nombre de la vista predeterminada por otro más descriptivo. El campo _Name_ es simplemente una etiqueta y se puede cambiar fácilmente.

Si la instalación de Adobe Commerce o Magento Open Source tiene una instalación de varios sitios o de varias tiendas, no cambie el campo Código de almacén sin comprobar que no se hace referencia al valor en el archivo `index.php`. Si no tiene acceso al servidor para examinar el archivo, pida ayuda a un desarrollador.

| Campo | Valor original | Valor actualizado |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. En la columna _[!UICONTROL Store View]_de la cuadrícula, haga clic en el nombre de la vista que desee editar.

   Al editar la vista predeterminada, los campos _[!UICONTROL Store]_y_[!UICONTROL Status]_ no están disponibles.

   ![Vista de tienda - editar vista predeterminada](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Actualice los campos siguientes según sea necesario:

   - **[!UICONTROL Store]** (solo vistas no predeterminadas)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (solo si no se usa en `index.php`)
   - **[!UICONTROL Status]** (solo vistas no predeterminadas)
   - **[!UICONTROL Sort Order]**
   - **[!UICONTROL Sync products and attributes]** (solo si [!DNL Adobe Commerce Optimizer Connector] está instalado)

   ![Vista de tienda: editar vista predeterminada con la configuración del exportador de Adobe Commerce Optimizer](./assets/stores-optimizer-exporter-settings.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save Store View]**.
