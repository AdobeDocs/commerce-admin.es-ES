---
title: Notas de la versión de AI Product Discovery
description: Consulte las notas de la versión de AI Product Discovery para ver las funciones de enriquecimiento de catálogos y PDP, correcciones, directrices de actualización, versiones de Commerce compatibles y problemas conocidos.
feature: Release Notes
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%
---
# Notas de la versión de AI Product Discovery

Estas notas de la versión abarcan las actualizaciones del enriquecimiento del catálogo y del enriquecimiento de PDP, incluidas las nuevas funciones, correcciones, requisitos de actualización y problemas conocidos. Cada entrada de versión identifica la extensión o el flujo de trabajo afectado.

![Nuevas](../assets/new.svg) nuevas características
![Se corrigió el problema](../assets/fix.svg) Correcciones y mejoras
![Problema conocido](../assets/bug.svg) Problemas conocidos

## Versión 2.1.3 {#release-2-1-3}

*30 de noviembre de 2026*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} [!DNL Adobe Commerce] 2.4.9, 2.4.8 y 2.4.7 en PHP 8.3 a 8.5. [!DNL Adobe Commerce as a Cloud Service]

La versión 2.1.3 combina el enriquecimiento de la página de detalles del producto con el enriquecimiento del catálogo en un nuevo elemento del menú Administrador llamado **Descubrimiento del producto de IA**. Además, la compatibilidad se extiende a [!DNL Adobe Commerce as a Cloud Service].

## Versión 2.1.2 {#release-2-1-2}

*22 de octubre de 2026*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} [!DNL Adobe Commerce] 2.4.9, 2.4.8 y 2.4.7 en PHP 8.3 a 8.5.

La versión 2.1.2 convierte el enriquecimiento del catálogo en una extensión independiente. Ahora incluye todo lo que se proporcionó anteriormente con la extensión independiente [!DNL Adobe Brand Visibility] (`magento/llm-optimizer`): aplicar sugerencias aprobadas al catálogo, revertirlas y proteger sus propias ediciones para que no se sobrescriban.

### Actualización de versiones anteriores {#upgrade-from-earlier-versions}

>[!IMPORTANT]
>
>La versión 2.1.2 no se puede instalar junto con la extensión [!DNL Adobe Brand Visibility]. Si lo tiene instalado, elimínelo como parte de la actualización.

1. Quite la extensión [!DNL Adobe Brand Visibility], si está instalada:

   ```bash
   composer remove magento/llm-optimizer
   ```

   Si la extensión se instaló copiando o vinculando simbólicamente `Magento/LlmoCatalog` en `app/code`, elimine ese directorio. No solo deshabilite el módulo: un módulo deshabilitado que aún esté en el disco puede hacer que `setup:upgrade` elimine la tabla que almacena los valores originales de los productos enriquecidos.

1. Actualice el enriquecimiento del catálogo y aplique los cambios:

   ```bash
   composer require magento/module-catalog-enrichment:^2.1
   bin/magento setup:upgrade
   bin/magento cache:flush
   ```

   Vaciar la caché después de la actualización. La actualización mueve las concesiones de acceso existentes a nuevos recursos de permisos, y esas concesiones no surten efecto hasta que se borra la caché.

### Requisitos

![Nuevo](../assets/new.svg) **PHP 8.3 y [!DNL Adobe Commerce] 2.4.7 o posterior**—PHP 8.1 es el fin de su vida útil y PHP 8.2 llega al fin de su vida útil el 31 de diciembre de 2026, por lo que ninguno de los dos es compatible. [!DNL Adobe Commerce] 2.4.6 y versiones anteriores no son compatibles.

### Nuevas funciones

![Nuevo](../assets/new.svg) **[!UICONTROL AI Product Discovery]menú**: las páginas de enriquecimiento del catálogo ahora tienen su propia sección en la barra lateral de administración. Ir a **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**. Anteriormente, la página estaba en **[!UICONTROL Catalog]**.

![Nuevo](../assets/new.svg) [!BADGE Beta]{type=Informative tooltip="Aún no está disponible de forma general"} **[!UICONTROL Product Details Page Enrichment (Beta)]**—Una nueva página bajo **[!UICONTROL AI Product Discovery]** para revisar las sugerencias de enriquecimiento para las páginas de detalles del producto. El enriquecimiento de la página de detalles del producto está en versión beta y aún no está disponible de forma general.

![Nuevo](../assets/new.svg) **Aplicar y revertir sugerencias aprobadas**: esta extensión escribe en el catálogo las actualizaciones de nombre y descripción aprobadas. Commerce registra el valor original de cada atributo enriquecido la primera vez que cambia, por lo que una reversión siempre restaura el valor que tenía antes del enriquecimiento, incluso después de aplicar varias sugerencias al mismo atributo.

![Nuevo](../assets/new.svg) **Se respetan sus ediciones**: al cambiar un nombre o una descripción enriquecidos en el formulario del producto de administrador, con **[!UICONTROL Update Attributes]** o mediante una importación, se conserva su valor y la sugerencia relacionada se marca como *Desactualizado*. Un cambio realizado en el ámbito predeterminado sólo afecta a las vistas de almacén que heredan el valor.

![Nuevo](../assets/new.svg) **acceso de sólo lectura al catálogo para sugerencias**—[!DNL Commerce Catalog Agent] puede leer datos de productos, categorías, conjuntos de atributos y tipos de productos para seleccionar productos para su análisis. La lectura devuelve solamente los atributos marcados **[!UICONTROL Used in Product Listing]**, además de los atributos que se pueden enriquecer. No puede cambiar los datos del catálogo.

### Correcciones y mejoras

![Se ha corregido un problema](../assets/fix.svg) **Se ha reintentado aplicar informes correctamente**: si se vuelve a intentar una solicitud de aplicación una vez que ya se ha completado, el reintento ahora informa de los cambios aplicados en lugar de informar de ningún cambio. Nada se escribe dos veces.

![Se ha corregido un problema](../assets/fix.svg) **Solo los servicios aprobados pueden cambiar el catálogo**—Aplicar y revertir aceptar solo las solicitudes de [!DNL Commerce Catalog Agent]. Anteriormente, se aceptaba cualquier token de IMS de Adobe válido. La misma comprobación ahora también se aplica a las solicitudes de SOAP.

![Se ha corregido un problema](../assets/fix.svg) **Errores más claros**: una interrupción de Adobe IMS ahora devuelve `401` en lugar de `500`, por lo que no se vuelve a intentar realizar la solicitud en el catálogo y se rechaza un entorno de Adobe IMS no reconocido en lugar de tratarse como de ensayo.

![Se ha corregido un problema](../assets/fix.svg) **Entorno de Adobe IMS**—El enriquecimiento del catálogo ahora inicia sesión en el entorno de producción de Adobe IMS de forma predeterminada, incluso en instancias conectadas a un espacio de datos de [!DNL Commerce Services] que no es de producción. Anteriormente, esas instancias se enviaban al entorno de ensayo.

![Se ha corregido un problema](../assets/fix.svg) **Iniciar sesión después del cambio de dominio [!DNL Adobe Brand Visibility]**: la página de enriquecimiento del catálogo ahora se carga desde `abv.adobe.com`, lo que corrige un bucle de inicio de sesión después de que el dominio anterior empezara a redirigir.

### Problemas conocidos

![Problema conocido](../assets/bug.svg) **Roles con acceso total de [!UICONTROL Catalog]**: un rol de usuario guardado antes de esta versión con todos los **[!UICONTROL Catalog]** concedidos mantiene el acceso al recurso **[!UICONTROL Catalog Enrichment Service API]**. Revise estos roles en **[!UICONTROL System]** > **[!UICONTROL Permissions]** > **[!UICONTROL User Roles]** y borre ese recurso donde no se necesite.

## Versión 1.0.2 {#release-1-0-2}

Versión inicial de la página de administración del enriquecimiento del catálogo. Requiere la extensión [!DNL Adobe Brand Visibility] para aplicar sugerencias al catálogo.
