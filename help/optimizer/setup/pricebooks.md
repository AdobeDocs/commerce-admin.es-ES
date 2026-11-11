---
title: Libros de precios
description: Descubra cómo se asignan los libros de precios a partir de los datos de catálogo y precios en [!DNL Adobe Commerce].
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a instancias de Adobe Commerce as a Cloud Service aprovisionadas con CCDM (infraestructura de SaaS administrada por Adobe)."
TQID: 'https://experienceleague.adobe.com/8gpl-l6oQebTnrt-00-n1FEdKnzqhTQi3hRz4lrGQoE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 3033d2ab-c1d2-5b52-b865-72d9e5ad2c37
    internal-label: Currency
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 1041abe0e7d7c1212a717d5fd03180ce7fd32958
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%
---
# Libros de precios

Los libros de precios definen los precios de los productos para un origen de catálogo en todos los niveles y mercados de clientes. Admiten una jerarquía de libros de precios principales y secundarios.

![Jerarquía de libros de precios](../assets/price-book-hier.png)

## Conceptos clave

| Término | Descripción |
| ------ | ------------- |
| **Libro de precios** | Agrupación lógica que define los precios para un origen de catálogo; por ejemplo, una región específica o nivel de cliente y se utiliza para administrar los precios de los productos. |
| **Reserva de precios de reserva** | El libro de precios más alto de una jerarquía. No tiene principal y es el libro de precios *solamente* que define la moneda para sí mismo y para todos sus libros de precios descendientes.<br/><br/>Si no se define ningún libro principal durante la creación del libro de precios (a través de la API), se crea un nuevo libro de precios de reserva. |
| **Libro de precios principal** | Un libro de precios de nivel superior del que un libro de precios para niños puede heredar los precios si no se establecen explícitamente en el niño. |
| **Profundidad de jerarquía** | No se aplica un máximo de tres niveles (Alternativa -> Secundario -> Nieto)<br/><br/>en el momento de la ingesta. |
| **Moneda** | Definido solo para el libro de precios de reserva. Heredado de todos los libros de precios secundarios.<br/><br/>Si no se especifica la divisa durante la creación del libro de precios de reserva (a través de la API), el valor predeterminado de la divisa será USD. |
| **Precio del producto** | El precio específico asignado a un producto (SKU) dentro de un libro de precios en particular. |
| **Descuentos** | Los descuentos se definen en el precio del producto. No heredado. |

## Implementación del libro de precios

Al utilizar Adobe Commerce as a Cloud Service con el modelo de datos de catálogo maquetable (CCDM), los libros de precios se asignan a partir de los datos de catálogo y de precios. No se crean de forma manual.

En un nivel superior, la asignación es:

- **Vista de tienda → origen de catálogo**: los datos de productos de vista de tienda, incluidos los atributos localizados, se asignan a un origen de catálogo.
- **→ de sitio web Libro de precios o libros de precios**: los precios del sitio web se asignan al libro o libros de precios aplicables.
- **Entradas del libro de precios → precios del grupo de clientes**—Los precios del grupo de clientes se asignan a las entradas de precios relevantes.

Mantenga la configuración de catálogo de origen, sitio web y asignación de precios en la configuración de Adobe Commerce y, a continuación, asigne los libros de precios asignados en la vista de catálogo correspondiente configurando los libros de precios disponibles. Si no hay libros de precios asignados, la vista de catálogo utiliza el libro de precios predeterminado.

Una vista de catálogo utiliza la configuración de libros de precios disponible con sus datos de catálogo y directivas para determinar la experiencia de comercialización, incluidos los precios devueltos para los productos.

>[!NOTE]
>
>Para Commerce B2B, el sistema crea y asigna un único libro de precios a cada vista de catálogo en función de la configuración del catálogo compartido. No es necesario configurar la disponibilidad del libro de precios para estas vistas.

## Precios de pago y envío

Los libros de precios admiten la experiencia de comercialización y catálogo de tiendas. Commerce Core sigue gestionando el carro de compras y el cierre de compra. Un precio disponible solo en CCDM no se convierte automáticamente en el precio utilizado por el cierre de compra.

Mantenga los precios consistentes con la configuración principal de Commerce y pruebe los precios mostrados, los complementos al carro de compras, las promociones y el cierre de compra como parte de la validación de la implementación.

## Ver libros de precios

Una vez finalizada la sincronización de datos del catálogo, vea los libros de precios disponibles y sus identificadores en el área de trabajo **[!UICONTROL Catalog views]**.

1. Vaya a _Configuración de la tienda_ y haga clic en **[!UICONTROL Catalog views]**.

1. Haga clic en **[!UICONTROL Create catalog view]**.

1. Revise los libros de precios disponibles en la sección **[!UICONTROL Price Books]** de la configuración de la vista de catálogo.

   ![Nombres e ID del libro de precios](../assets/price-book-name-ids.png)

## Configurar disponibilidad del libro de precios

Asocie los libros de precios asignados a las vistas de catálogo configurando los libros de precios disponibles en el espacio de trabajo de vistas de catálogo en el administrador de Commerce.

>[!NOTE]
>
>Una vista de catálogo privado (una con [!UICONTROL Catalog Protection] habilitado) sólo puede hacer referencia a un libro de precios.

1. En el área de trabajo **[!UICONTROL Catalog views]**, seleccione la vista de catálogo que desee configurar.

1. En la sección **[!UICONTROL Price Books]**, seleccione los libros de precios disponibles para las tiendas respaldadas por la vista de catálogo.
