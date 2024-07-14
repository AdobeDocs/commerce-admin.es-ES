---
title: Administrar orígenes de inventario
description: Obtenga información sobre las fuentes y cómo definen las ubicaciones físicas en las que se administra y envía el inventario de productos para la realización de pedidos o en las que hay servicios disponibles.
exl-id: 1315a8c9-7791-4c4b-9463-3126b79793c2
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Administrar fuentes

Las fuentes son las ubicaciones físicas en las que se administra y envía el inventario de productos para la satisfacción de pedidos o en las que hay servicios disponibles. Estas ubicaciones pueden incluir almacenes, tiendas físicas, centros de distribución, ubicaciones de recogida y expedidores de entrega. Usted asigna cantidades de inventario a estos orígenes y [!DNL Commerce] agrega automáticamente el total de productos vendibles para sus existencias. Para las grandes empresas, añada múltiples fuentes para todas sus ubicaciones: en diferentes ubicaciones geográficas por país y continente, ubicaciones en una ciudad, en función del tipo de inventario, incluso en función de los servicios.

Se recomienda proporcionar ubicaciones geográficas físicas específicas al crear una fuente. Esto permite que el _Algoritmo de prioridad de distancia_ compare la ubicación de la dirección de destino de envío con las ubicaciones de origen disponibles para determinar la fuente más cercana a los envíos. Puede utilizar Mapas de Google o cálculos sin conexión, que utilizan geocódigos. Para obtener más información sobre este _algoritmo de prioridad de distancia_, consulte [Configurar el algoritmo de prioridad de distancia](distance-priority-algorithm.md).

Comience con un _Source predeterminado_ que pueda actualizar pero no deshabilitar. Los comerciantes de un solo origen y para la migración de productos utilizan esta fuente. Siempre necesita un origen predeterminado.

- **Información de ubicación** - Cada origen incluye el nombre, el país, la dirección física de la ubicación y un punto de contacto.
- **Habilitando recursos**: puede habilitar y deshabilitar orígenes según sea necesario. Habilite una fuente solo si acepta y cumple pedidos y pedidos pendientes.
- **Inventario disponible**: asigne y actualice las cantidades de inventario para cada origen a través de la página de productos. Las cantidades de inventario se calculan, proporcionan y reservan a través de la asignación de origen y stock.

El siguiente diagrama ayuda a ilustrar las fuentes de un comerciante de la tienda de bicicletas que vende una bicicleta de montaña, que está disponible para las existencias y accesible por la SSA para los envíos.

![Ejemplo de diagrama de orígenes](assets/diagram-sources.png){width="600" zoomable="yes"}

Todas las tiendas comienzan con una Source predeterminada que debe permanecer habilitada:

- Todos los productos nuevos importados en [!DNL Commerce] requieren un origen y un stock, asignados automáticamente para el acceso inmediato a [!DNL Inventory Management].
- Los comerciantes de origen único utilizan la Source predeterminada como único punto de ubicación de inventario y envíos.

## Editar fuentes

Puede actualizar el nombre, la dirección, la ubicación GPS y la información del punto de contacto. El código fuente es un valor protegido que actúa como ID único que asocia el origen con las cantidades y existencias de sus productos.

Si edita la Source predeterminada, puede editar todas las configuraciones excepto el nombre y el código. Se recomienda que los comerciantes de un solo origen agreguen información que coincida con su ubicación.

La página _[!UICONTROL Manage Sources]_enumera todas las ubicaciones de inventario e instalaciones de cumplimiento disponibles. Puede agregar nuevos orígenes de inventario y editar las ubicaciones existentes.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Para agregar una ubicación de inventario, consulte [Agregar un nuevo Source](sources-add.md).

1. Busque el origen del inventario y ábralo en el modo _Editar_.

1. Actualice la información y guarde los cambios.

   ![Administrar orígenes](assets/inventory-sources.png){width="600" zoomable="yes"}

## Barra de botones

| Botón | Descripción |
|--|--|
| [!UICONTROL Add New Source] | Abre el formulario Nuevo Source, que se utiliza para especificar un nuevo origen de inventario, servicio de satisfacción de pedidos o ubicación. |

## Descripciones de columnas de Administrar fuentes

| Columna | Descripción |
|--|--|
| [!UICONTROL Code] | Código alfanumérico único que el sistema utiliza para identificar el origen del inventario. |
| [!UICONTROL Name] | Un nombre único que identifica el origen de inventario para los usuarios administradores. |
| [!UICONTROL Is Enabled] | Indica si el origen de inventario está activo y disponible para usar. |
| [!UICONTROL Pickup Location] | Indica si el origen está activo como ubicación de recogida para [envío en tienda](../stores-purchase/shipping-in-store-delivery.md). |
| [!UICONTROL Action] | Al hacer clic en **[!UICONTROL Edit]**, se abre el registro de origen de inventario en modo de edición. |

## Otras columnas

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Latitude] | Especifica la coordenada de latitud del origen de inventario para GPS. Introduzca el valor como un número, precedido por un signo más o menos según sea necesario. No se permiten el símbolo de grado ni las letras. Por ejemplo: `32.7555` |
| [!UICONTROL State/Province] | Estado o provincia donde se encuentra el origen. |
| [!UICONTROL Postcode] | El código postal del origen. |
| [!UICONTROL Email] | Correo electrónico del contacto principal. |
| [!UICONTROL Longitude] | Especifica la coordenada de longitud del origen de inventario para GPS. Introduzca el valor como un número, precedido por un signo más o menos según sea necesario. No se permiten el símbolo de grado ni las letras. Por ejemplo: Longitud -97.3308 |
| [!UICONTROL City] | Ciudad donde se encuentra el origen. |
| [!UICONTROL Phone] | Número de teléfono del contacto principal. |
| [!UICONTROL Country] | El país donde se encuentra el origen. |
| [!UICONTROL Street] | La dirección de la calle de origen. |
| [!UICONTROL Fax] | El código de área y el número de fax del contacto principal. |
