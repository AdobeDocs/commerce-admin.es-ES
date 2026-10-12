---
title: Configurar lista de solicitudes máxima
description: Obtenga información sobre la configuración de listas de solicitudes, que controla el número máximo que se puede mantener para cada cuenta de cliente.
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
TQID: 'https://experienceleague.adobe.com/we9sPvRg20kEV4EpfemuA7WW-rjv7G6evjr5MwzRGyM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
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
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '215'
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
