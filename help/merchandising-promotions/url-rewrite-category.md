---
title: Reescrituras de URL de categoría
description: Aprenda a utilizar las reescrituras de direcciones URL de categorías para redirigir los vínculos a la dirección URL de otra categoría de la tienda de Commerce.
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Reescrituras de URL de categoría

Si se elimina una categoría del catálogo, se puede reescribir una categoría para redirigir los vínculos a la dirección URL de otra categoría de la tienda. Piense en términos de _destino_ / _petición original_  o _redirigir a_ / _redirigir desde_. Aunque es posible que los visitantes sigan navegando a la página anterior desde motores de búsqueda o vínculos obsoletos, la redirección hace que la tienda cambie al nuevo destino.

If [redirecciones automáticas](url-redirect-product-automatic.md) están activados para la tienda, no es necesario crear una nueva escritura cuando una categoría [Clave de URL](../catalog/catalog-urls.md) se ha cambiado.

{{url-rewrite-skip}}

## Paso 1. Planificar la reescritura

Para evitar errores, anote el _redirigir a_ ruta y _redirigir desde_ ruta e incluir la clave URL y el sufijo (si corresponde).

Si no está seguro, abra todas las páginas de categorías de la tienda y copie la ruta de la barra de direcciones del explorador.

**Ejemplo:**

Redirigir a: `gear/backpacks-and-bags.html`

Redirigir desde: `gear/bags.html`

## Paso 2. Creación de la reescritura

{{url-rewrite-params}}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Antes de continuar, haga lo siguiente para comprobar que la ruta de solicitud está disponible:

   - En el filtro de búsqueda, en la parte superior de la **[!UICONTROL Request Path]** , introduzca la clave URL de la categoría a la que se va a redirigir y haga clic en **[!UICONTROL Search]**.

   - Si hay varios registros de redirección para la página, busque el que coincida con la vista de tienda aplicable y abra el registro de redirección en modo de edición.

   - En la esquina superior derecha, haga clic en **[!UICONTROL Delete]**. Cuando se le solicite, haga clic en **[!UICONTROL OK]** para confirmar.

1. Cuando vuelva a la _[!UICONTROL URL Rewrites]_página, haga clic en **[!UICONTROL Add URL Rewrite]**.

1. Establecer **[!UICONTROL Create URL Rewrite]** hasta `For category` y elija la categoría de destino en el árbol que es el destino de la redirección.

   ![Reescritura de URL: elija una categoría](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. En el _Reescritura de URL_ , haga lo siguiente:

   - Si tiene varias tiendas, seleccione la **[!UICONTROL Store]** donde se aplica la reescritura.

   - Para **[!UICONTROL Request Path]**, introduzca la clave URL de la categoría que solicita el cliente. Este es el _redirigir desde_ categoría.

     >[!NOTE]
     >
     >La ruta solicitada debe ser única para el almacén especificado. Si ya hay una redirección que utiliza la misma ruta de solicitud, recibirá un error cuando intente guardar la redirección. Debe eliminarse la redirección anterior para poder crear una.

   - Establecer **[!UICONTROL Redirect]** a uno de los siguientes:

      - `Temporary (302)`
      - `Permanent (301)`

   - Para su referencia, introduzca una breve descripción de la reescritura.

   ![Añadir reescritura de URL para la categoría](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. Antes de guardar la redirección, revise lo siguiente:

   - El vínculo de la esquina superior izquierda muestra el nombre de la categoría de destino.
   - La ruta de solicitud contiene la ruta del original _redirigir desde_ categoría.

1. Cuando termine, haga clic en **[!UICONTROL Save]** botón.

   La nueva reescritura de categoría aparece en la parte superior de la cuadrícula Reescritura de URL.

## Paso 3. Prueba del resultado

1. Vaya a la página principal de la tienda.

1. Realice una de las siguientes acciones:

   - Ir al original _redirigir desde_ categoría.
   - En la barra de direcciones del explorador, introduzca la ruta al original _redirigir desde_ inmediatamente después de la URL de la tienda y pulse **[!UICONTROL Enter]**.

   Aparecerá la nueva categoría de destino en lugar de la solicitud de categoría original.

## Descripciones de campos

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indica el tipo de reescritura. El tipo no se puede cambiar una vez creada la reescritura. Opciones: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | La categoría que se va a redirigir. Según la configuración, la ruta de solicitud puede incluir el sufijo .html o .htm y la categoría principal. La ruta de solicitud debe ser única y no puede estar siendo utilizada por otra redirección. Si recibe un error que indica que la ruta de solicitud existe, elimine la redirección existente e inténtelo de nuevo. |
| [!UICONTROL Target Path] | Ruta interna que utiliza el sistema para señalar al destino de la redirección. La ruta de destino aparece atenuada y no se puede editar. |
| [!UICONTROL Redirect] | Determina el tipo de redirección. Opciones: <br/>**[!UICONTROL No]**- No se ha especificado ninguna redirección. Muchas operaciones crean solicitudes de redireccionamiento de este tipo. Por ejemplo, cada vez que agrega productos a una categoría, se redirige el `No` El tipo se crea en cada vista de tienda.<br/>**[!UICONTROL Temporary (302)]** - Indica a los motores de búsqueda que la reescritura es por un tiempo limitado. Los motores de búsqueda generalmente no conservan la información de clasificación de páginas para las reescrituras temporales. <br/>**[!UICONTROL Permanent (301)]**: indica a los motores de búsqueda que la reescritura es permanente. Los motores de búsqueda generalmente conservan la información de clasificación de páginas para reescrituras permanentes. |
| [!UICONTROL Description] | Describe el propósito de la reescritura para referencia interna. |

{style="table-layout:auto"}
