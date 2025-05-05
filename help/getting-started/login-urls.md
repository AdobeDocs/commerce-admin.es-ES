---
title: Credenciales y direcciones URL de inicio de sesión
description: Obtenga información acerca de las URL de Commerce y las credenciales de cuenta utilizadas para obtener acceso a su administrador y a su tienda.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Credenciales y direcciones URL de inicio de sesión

Antes de continuar con la instalación y configuración, asegúrese de que dispone de la información necesaria para acceder al administrador de su tienda y a su cuenta de Commerce.

## URL de tienda

La dirección de tu [tienda](storefront.md) suele ser el dominio asignado a tu dirección IP. Algunos almacenes se instalan en el directorio raíz o superior. Otros se instalan en un directorio debajo de la raíz. El almacén puede residir en un subdominio asociado a un dominio principal. La dirección URL de su tienda puede tener uno de los siguientes aspectos:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

Si todavía no tiene un dominio, la dirección URL de la tienda incluye una serie de cuatro números, cada uno separado por un punto en notación _dotted quad_.

## URL de administrador

La dirección de tu tienda [Admin](admin.md) se ha configurado durante la instalación. La dirección predeterminada es la misma que la tienda, pero con `/admin` al final. Aunque los ejemplos de esta guía utilizan el directorio predeterminado, se recomienda ejecutar el administrador desde una ubicación exclusiva de su tienda.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## Cuenta de [!DNL Commerce]

Su [cuenta de Commerce](commerce-account-create.md) proporciona acceso a información sobre sus productos y servicios, configuración de cuenta, historial de facturación y recursos de asistencia. Para acceder a su cuenta, vaya al sitio principal de Commerce y haga clic en **[!UICONTROL My Account]** en la esquina superior derecha.

## Cuenta de cliente

Mientras aprendes cómo moverte por la tienda, asegúrate de configurar una [cuenta de cliente](../customers/account-dashboard.md) de prueba para que puedas experimentar el proceso de compra y venta desde la perspectiva del cliente.

## Datos de muestra

Adobe proporciona un conjunto de datos de ejemplo que incluye una tienda de muestra con más de 250 productos (unos 200 de ellos son productos configurables), categorías, reglas de precios promocionales, páginas de CMS, banners, etc. Los datos de muestra usan el tema _Luma_ en la tienda. [La instalación de estos datos de ejemplo](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html?lang=es) es opcional, pero puede resultar útil para probar y desarrollar personalizaciones para su negocio de comercio electrónico.
