---
title: Reescrituras de URL personalizadas
description: Aprenda a utilizar las reescrituras de URL personalizadas para administrar redirecciones diversas en su tienda de Commerce.
exl-id: b15054be-e463-48e6-b6c1-0a8a2141cc01
feature: Search, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Reescrituras de URL personalizadas

Se puede utilizar una reescritura personalizada para administrar varias redirecciones, como redirigir una página desde la tienda a un sitio web externo. Por ejemplo: puede tener dos sitios web de Commerce, cada uno con su propio dominio. Puede utilizar un redireccionamiento personalizado para redirigir las solicitudes de un producto, categoría o página al otro sitio web. A diferencia de otros tipos de redireccionamiento, el destino de un redireccionamiento personalizado no se elige de una lista de páginas existentes en la tienda.

Antes de empezar, asegúrese de comprender exactamente para qué sirve la redirección. Piense en términos de _destino_ / _origen_ o _redirigir a_ / _redirigir desde_. Aunque es posible que los visitantes sigan navegando a la página anterior desde motores de búsqueda o vínculos obsoletos, la redirección hace que la tienda cambie al nuevo destino.

## Paso 1. Planificar la reescritura

Para evitar errores, escriba la dirección URL del _redirigir a_ y la clave URL de la _redirigir desde_ página.

Si no está seguro, abra cada página y copie la dirección URL de la barra de direcciones del explorador.

**Ejemplo**

Redirigir a:

    http://www.different-website.com/page.html

Redirigir desde:

    cms-page
    category.html
    category/subcategory.html
    product.html
    category/product.html

## Paso 2. Creación de la reescritura

{{url-rewrite-params}}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Antes de continuar, haga lo siguiente para comprobar que la ruta de solicitud está disponible:

   - En el filtro de búsqueda, en la parte superior de la **[!UICONTROL Request Path]** , introduzca la clave URL de la página a redirigir y haga clic en **[!UICONTROL Search]**.

   - Si hay varios registros de redirección para la página, busque el que coincida con la vista de tienda aplicable y ábralo en modo de edición.

   - En la esquina superior derecha, haga clic en **[!UICONTROL Delete]**. Cuando se le solicite, haga clic en **[!UICONTROL OK]** para confirmar.

1. Cuando vuelva a la página Reescrituras de URL, haga clic en **[!UICONTROL Add URL Rewrite]**.

1. Establecer **[!UICONTROL Create URL Rewrite]** hasta `Custom`.

   ![Reescrituras de URL: personalizadas](./assets/url-rewrite-custom.png){width="600" zoomable="yes"}

1. En Información de reescritura de URL, haga lo siguiente:

   - Si tiene varias vistas de tienda, seleccione la opción **[!UICONTROL Store]** donde se aplica la reescritura.

   - Para **[!UICONTROL Request Path]**, introduzca la clave de URL y la ruta (si corresponde) de la página del producto, categoría o CMS que se va a redirigir.

     >[!NOTE]
     >
     >La ruta solicitada debe ser única para el almacén especificado. Si ya hay una redirección que utiliza la misma ruta de solicitud, recibirá un error cuando intente guardar la redirección. Debe eliminarse la redirección anterior para poder crear una.

   - Para **[!UICONTROL Target Path]**, introduzca la dirección URL del destino. Si el destinatario está en otro sitio web, introduzca la dirección URL completa.

   - Establecer **Redirigir** a uno de los siguientes:

      - `Temporary (302)`
      - `Permanent (301)`

   - Para su referencia, introduzca una breve descripción de la reescritura.

1. Antes de guardar la redirección, revise lo siguiente:

   - El [!UICONTROL Request Path] contiene la clave URL o la ruta del original _redirigir desde_ página.
   - El [!UICONTROL Target Path] contiene la dirección URL del _redirigir a_ página.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

   La nueva reescritura aparece en la cuadrícula de la parte superior de la lista.

## Paso 3. Prueba del resultado

1. Vaya a la página principal de la tienda.

1. Realice una de las siguientes acciones:

   - Ir al original _redirigir desde_ página.
   - En la barra de direcciones del explorador, introduzca el nombre del original _redirigir desde_ inmediatamente después de la URL de la tienda y pulse **Entrar**.

   Aparecerá la nueva página de destino en lugar de la solicitud de página original.

## Descripciones de campos

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indica el tipo de reescritura. El tipo no se puede cambiar una vez creada la reescritura. Opciones: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | La página que se va a redirigir. La ruta de solicitud debe ser única y no puede estar siendo utilizada por otra redirección. Si recibe un mensaje de error indicando que la ruta de solicitud existe, elimine la redirección existente e inténtelo de nuevo. |
| [!UICONTROL Target Path] | Ruta interna que utiliza el sistema para señalar al destino. La ruta de destino aparece atenuada y no se puede editar. |
| [!UICONTROL Redirect] | Determina el tipo de redirección. Opciones: <br/>**No** - No se ha especificado ninguna redirección. <br/>**[!UICONTROL Temporary (302)]**- Indica a los motores de búsqueda que la reescritura es por un tiempo limitado. Los motores de búsqueda generalmente no conservan la información de clasificación de páginas para las reescrituras temporales.<br/>**[!UICONTROL Permanent (301)]** : indica a los motores de búsqueda que la reescritura es permanente. Los motores de búsqueda generalmente conservan la información de clasificación de páginas para reescrituras permanentes. |
| [!UICONTROL Description] | Describe el propósito de la reescritura para referencia interna. |

{style="table-layout:auto"}
