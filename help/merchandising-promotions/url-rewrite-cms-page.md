---
title: Reescribe la URL de la página de contenido
description: Aprenda a utilizar las reescrituras de URL de páginas de contenido para redirigir vínculos a la URL de otra página de contenido de su tienda de Commerce.
exl-id: e29c45fd-cf25-4b51-a8ae-9e188dc2a61c
feature: Page Content, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Reescribe la URL de la página de contenido

Antes de empezar, asegúrese de comprender exactamente para qué sirve la redirección. Piense en términos de _destino_ / _origen_ o _redirigir a_ / _redirigir desde_. Aunque es posible que los visitantes sigan navegando a la página anterior desde motores de búsqueda o vínculos obsoletos, la redirección hace que la tienda cambie al nuevo destino.

![Reescrituras de URL: página de CMS](./assets/url-rewrite-cms-page.png){width="700" zoomable="yes"}

## Paso 1. Planificar la reescritura

Para evitar errores, escriba la clave URL del _redirigir a_ página y _redirigir desde_ página.

Si no está seguro, abra todas las páginas de la tienda y copie la ruta de la barra de direcciones del explorador.

### Ruta de página de CMS

Redirigir a: `new-page`

Redirigir desde: `old-page`

## Paso 2. Creación de la reescritura

{{url-rewrite-params}}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Antes de continuar, haga lo siguiente para comprobar que la ruta de solicitud está disponible.

   - En el filtro de búsqueda, en la parte superior de la **[!UICONTROL Request Path]** , introduzca la clave URL de la página a redirigir y haga clic en **[!UICONTROL Search]**.

   - Si hay varios registros de redirección para la página, busque el que coincida con la vista de tienda aplicable y ábralo en modo de edición.

   - En la esquina superior derecha, haga clic en **[!UICONTROL Delete]**. Cuando se le solicite, haga clic en **[!UICONTROL OK]** para confirmar.

1. Cuando vuelva a la página Reescrituras de URL, haga clic en **[!UICONTROL Add URL Rewrite]**.

1. Establecer **[!UICONTROL Create URL Rewrite]** hasta `for CMS page`.

1. Busque la nueva página de destino en la cuadrícula y ábrala en modo de edición.

   ![Añadir reescritura de URL: para la página de CMS](./assets/url-rewrite-cms-page-add.png){width="700" zoomable="yes"}

1. En Información de reescritura de URL, haga lo siguiente:

   - Si tiene varias vistas de tienda, seleccione la opción **[!UICONTROL Store]** donde se aplica la reescritura.

   - Para **[!UICONTROL Request Path]**, introduzca la clave URL de la página original que solicita el cliente. Este es el _redirigir desde_ página.

     >[!NOTE]
     >
     >La ruta de solicitud debe ser única para el almacén especificado. Si ya hay una redirección que utiliza la misma ruta de solicitud, recibirá un error cuando intente guardar la redirección. Debe eliminarse la redirección anterior para poder crear una.

   - Establecer **[!UICONTROL Redirect]** a uno de los siguientes:

      - `Temporary (302)`
      - `Permanent (301)`

   - Para su referencia, introduzca una breve descripción de la reescritura.

   ![Información de reescritura de URL](./assets/url-rewrite-cms-page-information.png){width="600" zoomable="yes"}

1. Antes de guardar la redirección, revise lo siguiente:

   - El vínculo de la esquina superior izquierda muestra el nombre de la página de destino.
   - La ruta de solicitud contiene la ruta del original _redirigir desde_ página.

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
| [!UICONTROL Request Path] | La página de CMS que se va a redirigir. La ruta de solicitud debe ser única y no puede estar siendo utilizada por otra redirección. Si recibe un mensaje de error indicando que la ruta de solicitud existe, elimine la redirección existente e inténtelo de nuevo. |
| [!UICONTROL Target Path] | Ruta interna que utiliza el sistema para señalar al destino. La ruta de destino aparece atenuada y no se puede editar. |
| [!UICONTROL Redirect] | Determina el tipo de redirección. Opciones: <br/>**[!UICONTROL No]**- No se ha especificado ninguna redirección.<br/>**[!UICONTROL Temporary (302)]** - Indica a los motores de búsqueda que la reescritura es por un tiempo limitado. Los motores de búsqueda generalmente no conservan la información de clasificación de páginas para las reescrituras temporales. <br/>**[!UICONTROL Permanent (301)]**: indica a los motores de búsqueda que la reescritura es permanente. Los motores de búsqueda generalmente conservan la información de clasificación de páginas para reescrituras permanentes. |
| [!UICONTROL Description] | Describe el propósito de la reescritura para referencia interna. |

{style="table-layout:auto"}
