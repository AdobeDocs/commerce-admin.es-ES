---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend]'
description: Revise la configuración de en [!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend] de la administración de Commerce.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![Plantillas de correo electrónico](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://docs.magento.com/user-guide/marketing/email-template-configuration.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Vista de tienda | Activa el proceso que permite a los clientes enviar correos electrónicos a sus amigos sobre los productos de su tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Select Email Template] | Vista de tienda | Identifica la plantilla de correo electrónico que se utiliza para los mensajes generados por el _Enviar un correo electrónico a un amigo_ función. Plantilla predeterminada: `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | Vista de tienda | Determina si el remitente debe ser un cliente registrado para enviar un correo electrónico sobre un producto a sus amigos. Opciones: `Yes` / `No` |
| [!UICONTROL Max Recipients] | Vista de tienda | Limita el número de personas que pueden estar en la lista de distribución para un solo correo electrónico. |
| [!UICONTROL Max Products Sent in 1  Hour] | Vista de tienda | Limita el número de productos que un solo usuario puede compartir durante un periodo de una hora. |
| [!UICONTROL Limit Sending By] | Vista de tienda | Determina el método utilizado para identificar al remitente. Las opciones incluyen: <br/>**`IP Address`**- (Recomendado) Identifica al remitente por la dirección IP del equipo que se utiliza para enviar los correos electrónicos del producto.<br/>**`Cookie (unsafe)`** - Identifica al remitente mediante una cookie del explorador. Este método no es seguro porque el usuario puede eliminar la cookie para evitar la restricción. |

{:style=&quot;table-layout:auto&quot;}
