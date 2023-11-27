---
title: Medios sociales y fuentes RSS
description: Aprenda a añadir redes sociales y otra integración de fuentes RSS para crear imagen de marca y producto.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 0%

---

# Medios sociales y fuentes RSS

Muchos comerciantes utilizan las redes sociales y otras herramientas digitales para crear conciencia de marca y producto. Puede integrar su tienda con sus redes sociales instalando una extensión de Marketplace o añadiendo un complemento a sus páginas de contenido. Utilice fuentes RSS para publicar la información de sus productos en sitios de agregación de compras e incluso incluirlos en sus boletines. Los clientes pueden suscribirse a sus fuentes RSS para conocer nuevos productos y promociones.

## Redes sociales

Tu tienda se puede conectar a las redes sociales instalando un [Extensión Marketplace](../getting-started/commerce-marketplace.md). Además, puede agregar fácilmente complementos sociales como _Like_ para crear bloques de CMS que se puedan incorporar a páginas de toda la tienda.

Los sitios de redes sociales tienen numerosos complementos que se pueden agregar fácilmente a su tienda. Además, hay muchas extensiones en el Commerce Marketplace que se pueden utilizar para integrar su tienda con los medios sociales. El siguiente ejemplo muestra cómo agregar un Facebook _Like_ a su tienda.

>[!NOTE]
>
>Adobe Commerce ha eliminado el nativo _Magento Social_ La integración de facebook y ya no admite la extensión de. Vaya a la [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} para localizar extensiones alternativas para la integración de Facebook.

### Paso 1. Obtener el código del botón

1. En el sitio web de desarrolladores de Meta, vaya a [configuración del botón](https://developers.facebook.com/docs/plugins/like-button) página.

1. Para **[!UICONTROL URL to Like]**, introduzca la dirección URL de la página de la tienda que desea que los demás utilicen _Like_.

   Por ejemplo, puede introducir la dirección URL de la página principal de la tienda.

1. Elija la **[!UICONTROL Layout]** para el botón.

1. Introduzca el **[!UICONTROL Width]** en píxeles que está disponible en el sitio para el botón y cualquier mensaje de texto asociado.

1. Establecer **[!UICONTROL Action Type]** a uno de los siguientes:

   - `Like`
   - `Recommend`

1. Clic **[!UICONTROL Get Code]** para copiar el código generado en el portapapeles.

### Paso 2. Creación de un bloque de contenido

1. Vuelva al administrador de la tienda.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Block]**.

1. Introduzca un elemento descriptivo **[!UICONTROL Block Title]** para consulta interna.

   Por ejemplo: `Facebook Like Button`.

1. Asignar un único **[!UICONTROL Identifier]** al bloque, con todos los caracteres en minúsculas y guiones bajos en lugar de espacios.

   Por ejemplo: `facebook_like_button`.

1. Si la instancia de Commerce tiene varias vistas de tiendas, elija cada una **[!UICONTROL Store View]** donde el bloque va a estar disponible.

1. Agregue el fragmento de código al contenido del bloque, según la herramienta de contenido:

   - Al utilizar [!DNL Page Builder], añada un [Código de HTML](../page-builder/html-code.md) Bloquee en el escenario y pegue el fragmento de código que ha copiado del sitio de Facebook. De lo contrario, pegue el fragmento de código en **[!UICONTROL Content]** cuadro.

   - Con el editor, pegue el fragmento de código que copió del sitio de Facebook en la **[!UICONTROL Content]** cuadro.

1. Si el bloque no está listo para su activación, establezca **[!UICONTROL Enable Block]** hasta `No`.

1. Cuando termine, haga clic en **[!UICONTROL Save Block]**.

### Paso 3. Colocar el bloque

1. Añada el bloque en función de la herramienta de contenido:

   - Al utilizar [!UICONTROL Page Builder], siga las instrucciones para [añadir el bloque](../page-builder/block.md) al escenario.

   - En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Widget]** y haga lo siguiente:

   - ![B2B para Adobe Commerce](../assets/b2b.svg) (Disponible con B2B solo para Adobe Commerce) En el _Configuración_ sección, conjunto **[!UICONTROL Type]** hasta `CMS Static Block` y haga clic en **[!UICONTROL Continue]**.

   - Compruebe que **[!UICONTROL Design Theme]** se establece en la temática actual.

   - Haga clic **[!UICONTROL Continue]**.

1. En el **[!UICONTROL Storefront Properties]** , haga lo siguiente:

   - Para **[!UICONTROL Widget Title]**, introduzca un título para la referencia interna.

   - Establecer **[!UICONTROL Assign to Store Views]** hasta `All Store Views`o a la vista donde desea que la aplicación esté disponible. Para seleccionar varias vistas, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

   - Introduzca un número en la **[!UICONTROL Sort Order]** para determinar el orden del bloque si está asignado para que aparezca en la misma ubicación de la página como otros elementos de contenido. La posición superior es cero.

1. En el _[!UICONTROL Layout Updates]_, haga clic en **[!UICONTROL Add Layout Update]**y establecer **[!UICONTROL Display On]**a la categoría, el producto o la página donde desea que aparezca el bloque.

   Por ejemplo, si elige `All Pages` y coloque el bloque en el encabezado o en el pie de página, el bloque aparecerá en el mismo lugar en todas las páginas del almacén.

   Para colocar el bloque en una página específica, haga lo siguiente:

   - Establecer **[!UICONTROL Display On]** hasta `Specified Page` y seleccione la **[!UICONTROL Page]** donde desea que aparezca el bloque.

   - Elija la **[!UICONTROL Block Reference]** para identificar el lugar de la página donde se va a colocar el bloque.

   - Acepte la configuración predeterminada para **[!UICONTROL Template]**, que se establece en `CMS Static Block Default Template`.

   - Haga clic **[!UICONTROL Save and Continue Edit]**.

1. En el panel de la izquierda, elija **[!UICONTROL Widget Options]**.

1. Clic **[!UICONTROL Select Block…]** y elija el bloque que desea colocar.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

1. Cuando se le solicite, siga las instrucciones de la parte superior del espacio de trabajo para actualizar el índice y la caché de la página.

   El widget ahora aparece en la _[!UICONTROL Widgets]_lista.

### Paso 4. Comprobar la ubicación en la tienda

Regresa a tu tienda para verificar que el bloque esté en la ubicación correcta. Para mover el bloque, puede volver a abrir el widget y probar con una página o referencia de bloque diferente.

## Fuentes RSS

RSS (Really Simple Syndication) es un formato de datos basado en XML que se utiliza para distribuir información en línea. Sus clientes pueden suscribirse a sus fuentes RSS para conocer nuevos productos y promociones. Las fuentes RSS también se pueden utilizar para publicar la información del producto en sitios de agregación de compras y se pueden incluir en boletines informativos.

Cuando las fuentes RSS están habilitadas, cualquier adición a productos, ofertas especiales, categorías y cupones se envía automáticamente a los suscriptores de cada fuente. Un vínculo a todas las fuentes RSS que publique se encuentra al pie de página de la tienda.

![Icono de fuente RSS](./assets/icon-rss.png){width="100"}<br/>

El software necesario para leer una fuente RSS se denomina lector de fuentes y permite a las personas suscribirse a titulares, blogs, podcasts y mucho más. Google Reader es uno de los muchos lectores de fuentes que están disponibles en línea de forma gratuita.

![Ejemplo de tienda - Fuente RSS](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### Ventajas de configurar una fuente RSS

- Descargue la última actualización de su tienda o blog
- Anuncios ligeros
- Acciones ordinarias
- Impulso de SEO
- Aumentar las ventas

### Tipos de fuentes RSS

| Fuente RSS | Descripción |
|--- |--- |
| [!UICONTROL Wish List] | Cuando se habilita, aparece un vínculo de fuente RSS en la parte superior de las páginas de la lista de deseos del cliente. Además, la página para compartir listas de deseos incluye una casilla de verificación que permite incluir un vínculo a la fuente desde listas de deseos compartidas. |
| [!UICONTROL New Products] | Publica la notificación de los nuevos productos añadidos al catálogo. |
| [!UICONTROL Special Products] | Publica una notificación de cualquier producto con precios especiales. |
| [!UICONTROL Coupons / Discounts] | Publica una notificación de los cupones o descuentos especiales disponibles en la tienda. |
| [!UICONTROL Top Level Category] | Publica una notificación de cualquier cambio realizado en la estructura de categorías de nivel superior del catálogo, que se refleja en el menú principal. |
| [!UICONTROL Customer Order Status] | Permite a los clientes realizar un seguimiento del estado de sus pedidos por fuente RSS. Cuando se habilita, aparece un vínculo de fuente RSS en el pedido. |

{style="table-layout:auto"}

### Configurar fuentes RSS para su tienda

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En la esquina superior derecha, establezca **[!UICONTROL Store View]** a las vistas donde las fuentes van a estar disponibles.

   Si se le solicita que confirme, haga clic en **[!UICONTROL OK]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL RSS Feeds]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Rss Config]** sección y conjunto **[!UICONTROL Enable RSS]** hasta `Enable`.

   ![Configuración del catálogo: fuentes RSS](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Si es necesario, borre la **[!UICONTROL Use Default]** para cambiar el valor predeterminado.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Wish List]** sección y conjunto **[!UICONTROL Enable RSS]** hasta `Enable`.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Catalog]** y establecer otras fuentes en `Enable` según sea necesario.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Catálogo: configuración de fuentes RSS](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Order]** sección y conjunto **[!UICONTROL Customer Order Status Notification]** hasta `Enable`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

1. Ver resultado en la tienda con `/rss` al final de la dirección URL de la página.

