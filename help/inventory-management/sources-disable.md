---
title: Deshabilitar orígenes de inventario
description: Obtenga información sobre cómo deshabilitar fuentes y modificar información, incluida la ubicación y el punto de contacto.
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Deshabilitar orígenes

Para asegurarse de que todos los datos del pedido se conservan en [!DNL Commerce]No obstante, las fuentes no se pueden eliminar. Los orígenes, pedidos y envíos están conectados directamente entre sí. Puede deshabilitar los orígenes y modificar la información, incluida la ubicación y el punto de contacto.

Según el estado de las ubicaciones, es posible que desee deshabilitar un origen. Un origen desactivado conserva todas las asignaciones por stock y productos, pero no se accede a él para el inventario y los pedidos.

Cuando una fuente está deshabilitada:

- [!DNL Inventory Management] ignora y no enumera el origen del envío o del procesamiento de pedidos.
- Las existencias no tienen acceso a las cantidades de inventario de origen para los totales de inventario agregados.
- Los envíos de pedidos no se pueden asignar a ubicaciones desactivadas.

No puede desactivar el origen predeterminado. [!DNL Commerce] utiliza esta fuente para todos los productos nuevos importados, para los productos agrupados y para el soporte del sistema de terceros. Puede habilitar o deshabilitar las fuentes personalizadas en cualquier momento.

Configuración de una fuente en `disabled` es útil en las siguientes situaciones:

- Adición de una tienda o almacén: a medida que abre nuevas tiendas o pone en línea nuevos almacenes y ubicaciones de envío, agregue una entrada de origen para configurar el inventario de productos mediante la importación y conéctese a las existencias potenciales.
- Envíos de temporada: las vacaciones pueden ser una época ajetreada del año. Es posible que desee restringir el envío únicamente desde ubicaciones de envío específicas, como almacenes, para mantener las ubicaciones de ladrillo y mortero bien abastecidas y centradas en los compradores locales. O puede añadir nuevas ubicaciones de envío durante un tiempo limitado para gestionar tasas más altas de ventas y pedidos entrantes.
- Cerrar una ubicación: cuando se cierra una ubicación para el movimiento a nuevas instalaciones o de forma permanente, se desactiva para detener los nuevos envíos desde la ubicación.

## Deshabilitar uno o varios orígenes personalizados

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Seleccione la casilla de verificación de cada origen personalizado habilitado que desee deshabilitar.

1. Haga clic en _Acciones_ en la esquina superior izquierda y seleccione **[!UICONTROL Disable]**.

   ![[!DNL Inventory Management] fuentes: menú Acciones](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. En el diálogo de confirmación, haga clic en **[!UICONTROL OK]**.

## Habilitar o deshabilitar un único origen personalizado

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Busque un origen personalizado y haga clic en **[!UICONTROL Edit]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el _General_ y cambiar **[!UICONTROL Is Enabled]**:

   | Opción | Descripción |
   | ----- | ----- |
   | `Yes` | El origen está habilitado. La cantidad se suma a la cantidad vendible. El origen muestra la cantidad actual al enviar los pedidos. El algoritmo de selección de origen comprueba el origen para el envío. |
   | `No` | El origen está deshabilitado. Las cantidades no se añaden a Cantidades vendibles. El origen no incluye al enviar pedidos. Las opciones de envío omiten este origen. |

1. Haga clic **[!UICONTROL Save and Close]**.
