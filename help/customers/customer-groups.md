---
title: Grupos de clientes
description: Utilice los grupos de clientes para determinar qué descuentos están disponibles para los clientes asignados a un grupo y la clase de impuestos asociada al grupo.
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Grupos de clientes

Los grupos de clientes determinan qué descuentos están disponibles y la clase de impuestos asociada al grupo. Los grupos de clientes predeterminados son `General`, `Not Logged In`, y `Wholesale`.

![Grupos de clientes](assets/customer-groups.png){width="700" zoomable="yes"}

## Filtrar el [!UICONTROL Customer Groups] lista

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Haga clic **[!UICONTROL Filters]**.

1. Introduzca criterios para buscar grupos, incluido un rango de ID, un grupo o una clase de impuestos.

   ![Opciones de filtrado](assets/groups-filters.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Apply Filters]**.

## Crear un grupo de clientes

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Haga clic **[!UICONTROL Add New Customer Group]**.

1. Para [!DNL **Group Name]**, introduzca un nombre único de menos de 32 caracteres para identificar el grupo.

1. Seleccione el **[!UICONTROL Tax Class]** que se aplica al grupo.

   ![Información del grupo](assets/group-information.png){width="600" zoomable="yes"}

1. Seleccione el **[!UICONTROL Excluded Website(s)]** que desee excluir del grupo.

   >[!IMPORTANT]
   >
   >La exclusión de sitios web puede reducir el tiempo de indexación de precios de productos y reglas de catálogo, ya que los sitios web excluidos no están indexados. Cuando se guarda un grupo de clientes con una exclusión de sitio web agregada, el precio del producto, la regla de catálogo y los índices de búsqueda de catálogo se invalidan. Si tiene muchos productos, sitios web y grupos de clientes, se recomienda pausar el proceso de reindexación hasta que haya excluido los sitios web de los grupos de clientes.

   De forma predeterminada, no se excluye ningún sitio web. Para seleccionar varios valores, mantenga presionada la tecla _Ctrl_ clave (PC) o el _Comando_ (Mac) y haga clic en cada opción.

1. Cuando termine, haga clic en **[!UICONTROL Save Customer Group]**.

## Editar un grupo de clientes

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Abra el registro en modo de edición.

1. Realice los cambios necesarios.

1. Cuando termine, haga clic en **[!UICONTROL Save Customer Group]**.

## Asignar un cliente a un grupo diferente

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Busque el cliente en la lista y seleccione la casilla de verificación en la primera columna.

1. Configure las variables **Acciones** control a `Assign a Customer Group` y elija el grupo en el menú.

   ![Asignar un grupo de clientes](assets/group-assign.png){width="600" zoomable="yes"}

1. Cuando se le pida que confirme, haga clic en **OK**.

## Asociar un grupo de clientes con descuentos específicos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _Promociones_ > **[!UICONTROL Cart Price Rules]**.

1. Seleccione la regla de precio del carro de compras a la que desea asociar un grupo para el descuento aplicado o [crear una regla de precios](../merchandising-promotions/price-rules-catalog.md).

1. Seleccione los grupos de clientes a los que se aplica la regla.

   ![Grupo de clientes con descuentos específicos](assets/group-discount.png){width="600" zoomable="yes"}

1. Haga clic **[!UICONTROL Save]**.

>[!NOTE]
>
> También puede utilizar el sistema de asignación de precios por adelantado para aplicar descuentos de productos a grupos de clientes. Consulte [Precios avanzados](../catalog/product-price-group.md).

## Eliminar un grupo de clientes

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Abra el registro en modo de edición.

1. En la barra de botones, haga clic en **[!UICONTROL Delete Customer Group]**.

1. Cuando se le pida que confirme, haga clic en **OK**.

## Demostración de grupos de clientes

Obtenga información acerca de la creación de grupos de clientes viendo esta demostración:

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12)
