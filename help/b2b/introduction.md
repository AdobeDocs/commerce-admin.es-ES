---
title: Introducción a [!DNL B2B for Adobe Commerce]
description: Aprenda a utilizar las funciones B2B integradas para satisfacer sus necesidades para los clientes que son empresas.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 0%

---

# Introducción a [!DNL B2B for Adobe Commerce]

A diferencia del modelo estándar de empresa a consumidor, las funciones B2B (de empresa a empresa) integradas están diseñadas para satisfacer las necesidades de los vendedores (comerciantes de Adobe Commerce) que tienen clientes que son empresas. Se adapta a las empresas con estructuras organizativas complejas y a varios usuarios con diversas funciones y niveles de permiso de compra. Un cliente B2B típico puede ser el gerente de una tienda minorista o un comprador que realiza compras en nombre de una compañía. En ambos casos, la transacción tiene lugar entre su negocio y el de ellos. También puede vender productos directamente al consumidor. [!DNL B2B for Adobe Commerce] es una solución integrada que proporciona soporte para modelos B2B y B2C.

Con el [instalación](install.md) y [habilitación](enable-basic-features.md) Con la extensión B2B de su tienda Adobe Commerce, la experiencia de compra se puede personalizar con catálogos y precios específicos del cliente, así como con contenido y promociones segmentados.

## Cuentas de empresa

El componente Cuenta de compañía es una entidad clave dentro de B2B de la que dependen todas las demás funciones de alguna manera. Permite unir varios compradores que pertenecen a una sola compañía en una sola cuenta de compañía (o cuenta corporativa). El administrador de la empresa puede crear una estructura empresarial (divisiones, subdivisiones y usuarios) que refleje el modelo operativo de la empresa y proporcione diferentes funciones de usuario y permisos para los miembros de la empresa. Esta estructura permite al administrador de la empresa controlar la actividad del usuario en la cuenta de la empresa: pedidos, cotizaciones, compras, acceso a la información o al perfil de crédito de la empresa, etc.

Desde Admin, el administrador del sitio de Commerce puede configurar el funcionamiento de la empresa en el sitio web. La configuración determina las capacidades B2B disponibles para los usuarios de la empresa, incluidos los métodos de pago, los niveles de precios, la capacidad de negociar precios mediante ofertas, la capacidad de crear listas de solicitudes, etc.

Para obtener más información, consulte [Cuentas de empresa](account-companies.md).

>[!NOTE]
>
>Cuando está activada, su tienda puede dar a las empresas la opción de _Pagar a cuenta_, lo que significa realizar compras en una línea de crédito de la empresa. Como comerciante, puede asignar crédito para una cuenta de compañía y administrar la configuración de crédito de una compañía, así como el reembolso de crédito.

## Administración de empresa

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible solo para participantes del programa beta"}

La gestión de la empresa ayuda a los administradores de los comerciantes a optimizar la administración y gestión de las organizaciones B2B con modelos operativos complejos.

Desde Admin, los usuarios con los permisos adecuados pueden crear una **[!UICONTROL Company Hierarchy]** que refleja la estructura organizativa de una empresa empresarial compuesta por varias empresas. Esta jerarquía les permite ver y administrar compañías como un grupo. Por ejemplo, el administrador puede designar una compañía matriz y asignar todas las compañías que operan como filiales de la compañía matriz. A continuación, el administrador de la compañía principal puede ver y administrar las cuentas de compañía de todas las compañías asignadas.

Para obtener más información, consulte [Administración de empresa](manage-companies.md).

## Servicios para Adobe Commerce

Los servicios para Adobe Commerce son servicios alojados que proporcionan funcionalidades ampliadas a Adobe Commerce y a Magento Open Source. Los servicios que admiten flujos de trabajo B2B son:

* [Servicio de catálogo](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html)
* [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)
* [Product Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)

## Catálogos compartidos

Los catálogos compartidos son los niveles de precios que permiten establecer precios personalizados por producto para distintas empresas en uno o varios sitios web. Mediante el uso de catálogos compartidos, puede vender productos aplicando diferentes niveles de precios para diferentes grupos de clientes. La compatibilidad con los catálogos compartidos solo está disponible para las tiendas comerciales configuradas para admitir cuentas de empresa.

Para obtener más información, consulte [Uso de catálogos compartidos](catalog-shared.md).

## Pedido rápido

Configure el Pedido rápido para reducir el proceso de pedido a varios clics para los clientes que iniciaron sesión cuando sepan el nombre del producto o el SKU de los productos que desean solicitar.

Para obtener más información, consulte [Pedidos rápidos](quick-order.md).

## Comillas negociables

Utilice la función Ofertas para iniciar la negociación de precios entre un comprador y un vendedor de la empresa.

* Un comprador autorizado puede iniciar un presupuesto desde el carro de compras.

* Un vendedor puede iniciar un presupuesto para un comprador desde Admin.

Los compradores y vendedores utilizan la oferta para gestionar el proceso de negociación (por ejemplo, añadiendo artículos, actualizando cantidades, solicitando y aplicando descuentos) hasta que lleguen a un acuerdo. El _Comillas_ En la cuadrícula Administrador se muestra cada presupuesto recibido y se mantiene un historial de la comunicación entre el comprador y el vendedor.

La compatibilidad con ofertas negociables solo está disponible para las tiendas de comercio configuradas para admitir cuentas de compañía.

Para obtener más información, consulte [Comillas negociables](quotes.md).

## Aprobaciones de pedidos de compra

Cuando se activan los pedidos de compra para una cuenta de empresa, todos los pedidos se crean automáticamente como pedidos de compra. Los usuarios de la compañía con los permisos necesarios pueden crear, editar y eliminar los PC que crean y los creados por los usuarios subordinados. Según su función y el orden, los usuarios de la empresa podrían estar sujetos a varias reglas de aprobación.

Para obtener más información, consulte [Pedidos de compra para empresas](purchase-order-flow.md).

## Listas de solicitudes

Los clientes pueden utilizar la lista de solicitudes para ahorrar tiempo al comprar productos pedidos con frecuencia, ya que pueden agregar artículos al carro de compras directamente desde la lista. Pueden mantener varias listas que se centran en productos de diferentes proveedores, compradores, equipos, campañas o cualquier otro elemento que optimice su flujo de trabajo.

Para obtener más información, consulte [Listas de solicitudes](requisition-lists.md).
