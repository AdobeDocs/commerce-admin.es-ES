---
title: Configurar lista de solicitudes máxima
description: Obtenga información sobre la configuración de listas de solicitudes, que controla el número máximo que se puede mantener para cada cuenta de cliente.
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Configurar lista de solicitudes máxima

Cuando la función de lista de solicitudes está activada, los clientes pueden crear varias listas de artículos comprados con frecuencia y utilizarlas para realizar pedidos. Está disponible tanto para usuarios como para invitados que hayan iniciado sesión. Puede habilitar listas de solicitudes al [configurar las características B2B](enable-basic-features.md).

Un cliente puede tener varias listas que se centren en productos de diferentes proveedores, compradores, equipos, campañas o cualquier otro elemento que optimice los flujos de trabajo comunes. [La funcionalidad de la lista de solicitudes](requisition-lists.md) es similar a las listas de deseos, con las siguientes diferencias:

- Una lista de solicitudes no se borra después de enviar artículos al carro de compras. Se puede utilizar varias veces.
- La interfaz de usuario de las listas de solicitudes utiliza una vista compacta para mostrar muchos artículos.

De forma predeterminada, los clientes pueden mantener hasta 999 listas de solicitudes para su cuenta. Sin embargo, puede modificar la configuración y especificar un número menor para reducir la carga en el almacén.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Requisition Lists]**.

   ![Listas de solicitudes - configuración general](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Number of Requisition Lists]**, introduzca el número máximo de listas de solicitudes que se pueden mantener para cada cuenta de cliente.

   El número mínimo es `2` y el máximo es `999`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
