---
title: Configuración de enriquecimiento
description: Configure la entrega, los trabajos de tráfico agénticos mensuales y los agentes de IA aptos compartidos por Enriquecimiento de catálogo y Enriquecimiento de PDP en Descubrimiento de productos de IA.
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# Configuración de enriquecimiento

Utilice la pestaña **[!UICONTROL Settings]** del área de trabajo de detección de productos de IA para configurar la instancia de Adobe Commerce. Cuando se configura, los enriquecimientos de catálogo y PDP aparecen en el espacio de trabajo de descubrimiento de productos de IA.

Los campos de esta ficha identifican el entorno [!DNL Adobe Commerce] y la vista de almacén a los que se conecta el descubrimiento de productos de IA. Para conocer los requisitos de organización e inicio de sesión de IMS, consulte los [requisitos previos de detección de productos de IA](prerequisites.md).

1. En el Administrador, vaya a **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]** o **[!UICONTROL Product Details Page Enrichment]**.
1. En la lista **[!UICONTROL Scope]** de la parte superior de la página, seleccione la vista de tienda que desee configurar o deje **[!UICONTROL All Store Views]** para administrar la configuración en las vistas de tienda.
1. Abra la ficha **[!UICONTROL Settings]**.
1. En **[!UICONTROL Commerce Configuration]**, expanda el panel de vista de tienda etiquetado con su dirección URL.

   Proporcione los detalles de su entorno [!DNL Adobe Commerce] para habilitar el servicio de detección de productos de IA y los flujos de trabajo de auditoría.

   ![Configuración de Commerce en la ficha Configuración de enriquecimiento del catálogo](./assets/catalog-enrichment-commerce-config.png){zoomable="yes"}

1. Introduzca los detalles de conexión necesarios para la vista de tienda.

   - **[!UICONTROL Store View URL]**: dirección URL correspondiente a la vista de la tienda (por ejemplo, `https://brand.example.com/fr/`).
   - **[!UICONTROL Environment ID]**: Identificador único del entorno [!DNL Adobe Commerce] al que accede la conexión.
   - **[!UICONTROL Website Code]**, **[!UICONTROL Store Code]** y **[!UICONTROL Store View Code]**: Sitio web, tienda y códigos de vista de tienda para el sitio web de Commerce. Estos valores deben coincidir con los códigos del administrador de Commerce.
   - **[!UICONTROL Host Name]**: nombre de host de su instancia [!DNL Adobe Commerce].
   - **(Opcional: solo para enriquecimiento de catálogo)** En **[!UICONTROL Catalog field limits]**, seleccione **[!UICONTROL Limit maximum characters for product name]** y especifique el límite de caracteres para cualquier nombre de producto generado. Seleccione **[!UICONTROL Limit maximum characters for product description]** y especifique el límite de caracteres para cualquier descripción de producto generada.

1. Haga clic en **[!UICONTROL Save]**.

Después de guardar, espere a que se complete cualquier trabajo de sincronización o validación inicial antes de depender de los resultados del catálogo o de la auditoría para esa vista de tienda. Las sugerencias de productos pueden tardar hasta 24 horas en aparecer en la página **[!UICONTROL Catalog Enrichment]**.

Para quitar una configuración de vista de tienda, expanda esa entrada y haga clic en **[!UICONTROL Delete]**.

## Descripciones de campos {#commerce-connection-fields}

Los campos obligatorios están marcados con un asterisco (*) en el formulario **[!UICONTROL Commerce Configuration]**.

| Campo | Requerido | Descripción |
| --- | --- | --- |
| URL de vista de tienda | Sí | URL correspondiente a la vista de tienda (por ejemplo, `https://brand.example.com/fr/`). |
| ID de entorno | Sí | Identificador único del entorno [!DNL Adobe Commerce] al que tiene acceso la conexión. |
| Código del sitio web | Sí | Código del sitio web de Commerce. |
| Código de tienda | Sí | Código de tienda del sitio web de Commerce. |
| Código de vista de tienda | Sí | Vista de tienda del sitio web de Commerce. |
| Nombre de host | Sí | Nombre de host de su instancia [!DNL Adobe Commerce]. |
| Límites del campo de catálogo (solo enriquecimiento de catálogo) | No | Defina límites de caracteres para cualquier nombre de producto y descripción generados. |
