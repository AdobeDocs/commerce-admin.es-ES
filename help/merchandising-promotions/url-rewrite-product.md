---
title: Reescrituras de URL del producto
description: Aprenda a utilizar las reescrituras de direcciones URL de productos para redirigir vínculos a la dirección URL de otro producto en su tienda de Commerce.
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# Reescrituras de URL del producto

Antes de empezar, asegúrese de comprender exactamente lo que debe lograr la redirección. Piense en términos de _destino_ / _solicitud original_ o _redireccionamiento a_ / _redireccionamiento desde_. Aunque es posible que los visitantes sigan navegando a la página anterior desde motores de búsqueda o vínculos obsoletos, la redirección hace que la tienda cambie al nuevo destino.

Si las [redirecciones automáticas](url-redirect-product-automatic.md) están habilitadas para su tienda, no es necesario crear una reescritura cuando se cambia una [clave URL](../catalog/catalog-urls.md) del producto.

{{url-rewrite-skip}}

## Paso 1. Planificar la reescritura

Para evitar errores, anote la ruta _redirigir a_ y la ruta _redirigir desde_, e incluya la clave de URL y el sufijo (si corresponde).

Si no está seguro, abra cada página de producto de la tienda y copie la ruta de la barra de direcciones del explorador. Al crear una redirección de producto, puede incluir o excluir la [ruta de categoría](../catalog/catalog-urls.md). Para este ejemplo, creamos un redireccionamiento de producto sin una ruta de categoría.

### Producto con ruta de categoría

Redirigir a: `gear/bags/impulse-duffle.html`

Redirigir desde: `gear/bags/overnight-duffle.html`

### Producto sin ruta de categoría

Redirigir a: `impulse-duffle.html`

Redirigir desde: `overnight-duffle.html`

## Paso 2. Creación de la reescritura

{{url-rewrite-params}}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Antes de continuar, haga lo siguiente para comprobar que la ruta de solicitud está disponible.

   - En el filtro de búsqueda que se encuentra en la parte superior de la columna **[!UICONTROL Request Path]**, ingrese la clave URL de la página a redirigir y haga clic en **[!UICONTROL Search]**.

   - Si hay varios registros de redirección para la página, busque el que coincida con la vista de tienda aplicable y ábralo en modo de edición.

   - En la esquina superior derecha, haga clic en **[!UICONTROL Delete]**. Cuando se le solicite, haga clic en **[!UICONTROL OK]** para confirmar.

1. En la esquina superior derecha de la página Reescrituras de URL, haga clic en **Agregar reescritura de URL**.

1. Establezca **[!UICONTROL Create URL Rewrite]** en `For product`.

1. En la cuadrícula, busque el producto que es el destino de la redirección y haga clic en la fila.

   ![reescrituras de URL: producto](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. Debajo del árbol de categorías, haga clic en **[!UICONTROL Skip Category Selection]**.

   Para este ejemplo, la redirección no incluye una categoría.

   ![Reescritura de URL del producto: omitir selección de categoría](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   La página Agregar reescritura de URL para un producto muestra un vínculo al destino en la esquina superior izquierda, y el campo Ruta de destino muestra la versión del sistema de la ruta, que no se puede cambiar. Inicialmente, el campo Redirect Path también muestra la ruta de destino.

   - Si tiene varias vistas de tienda, establezca **[!UICONTROL Store]** en la vista donde se aplique la reescritura. De lo contrario, se crea una reescritura para cada vista.

   - Para **[!UICONTROL Request Path]**, reemplace el valor predeterminado al escribir la clave de URL y el sufijo (si corresponde) de la solicitud de producto original. Este es el _redireccionamiento de_ producto que identificó en el paso de planificación.

     >[!NOTE]
     >
     >La ruta solicitada debe ser única para el almacén especificado. Si ya hay una redirección que utiliza la misma ruta de solicitud, recibirá un error cuando intente guardar la redirección. Debe eliminarse la redirección anterior para poder crear una.

   - Establezca **[!UICONTROL Redirect Type]** en una de las siguientes opciones:

      - `Temporary (302)`
      - `Permanent (301)`

   - Para su propia referencia, escriba un **[!UICONTROL Description]** breve de la reescritura.

   ![Reescritura de URL del producto: información](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. Antes de guardar la redirección, revise lo siguiente:

   - El vínculo de la esquina superior izquierda muestra el nombre del producto de destino.
   - La ruta de solicitud contiene la ruta de acceso para el redireccionamiento _original del producto_.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   La nueva reescritura de producto ahora aparece en la parte superior de la cuadrícula Reescritura de URL.

## Paso 3. Prueba del resultado

1. Vaya a la página principal de la tienda.

1. Realice una de las siguientes acciones:

   - Vaya a la página de _redirección de_ solicitud de producto original.
   - En la barra de direcciones del explorador, escribe la ruta al producto _redirect from_ original inmediatamente después de la URL de la tienda y presiona **Enter**.

   Aparece el nuevo producto de destino en lugar de la solicitud de producto original.

## Descripciones de campos

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indica el tipo de reescritura. El tipo no se puede cambiar una vez creada la reescritura. Opciones: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | El producto que se va a redirigir. Según la configuración, la ruta de solicitud puede incluir el sufijo `.html` o `.htm`, así como la categoría. La ruta de solicitud debe ser única y no puede estar siendo utilizada por otra redirección. Si recibe un error que indica que la ruta de solicitud existe, elimine la redirección existente e inténtelo de nuevo. |
| [!UICONTROL Target Path] | Ruta interna que utiliza el sistema para señalar al destino de la redirección. La ruta de destino aparece atenuada y no se puede editar. |
| [!UICONTROL Redirect] | Determina el tipo de redirección. Opciones: <br/>**[!UICONTROL No]**- No se especificó ninguna redirección. Muchas operaciones crean solicitudes de redireccionamiento de este tipo. Por ejemplo, cada vez que agrega productos a una categoría, se crea una redirección del tipo `No` en cada vista de tienda.<br/>**[!UICONTROL Temporary (302)]**: indica a los motores de búsqueda que la reescritura es por un tiempo limitado. Los motores de búsqueda generalmente no conservan la información de clasificación de páginas para las reescrituras temporales. <br/>**[!UICONTROL Permanent (301)]**: indica a los motores de búsqueda que la reescritura es permanente. Los motores de búsqueda generalmente conservan la información de clasificación de páginas para reescrituras permanentes. |
| [!UICONTROL Description] | Describe el propósito de la reescritura para referencia interna. |

{style="table-layout:auto"}

## Varias reescrituras de URL

Puede actualizar rápidamente las reescrituras de URL para varios o todos los productos simultáneamente mediante los siguientes pasos.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Seleccione todos los productos para los que desea actualizar las reescrituras de URL.

1. En _[!UICONTROL Actions]_, elija **[!UICONTROL Update attributes]**&#x200B;para actualizar varias o todas las reescrituras.

1. En _[!UICONTROL PRODUCTS INFORMATION]_, haga clic en la ficha **[!UICONTROL Websites]**.

1. En la sección _[!UICONTROL Add Product To Websites]_, seleccione todos los sitios web para los que desee restaurar las reescrituras de URL.

1. Cuando esté listo para actualizar, haga clic en **[!UICONTROL Save]**.

>[!NOTE]
>
>Todos los productos seleccionados se leen en los sitios web seleccionados y se regeneran las reescrituras de URL.

![Actualizar atributos - actualizar varias reescrituras de URL](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
