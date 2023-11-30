---
title: '[!DNL Commerce Intelligence] herramientas'
description: Descubra cómo Adobe Commerce y los comerciantes Magento Open Source pueden utilizar las herramientas de Commerce Intelligence para obtener la información que se utiliza para tomar decisiones comerciales sólidas.
exl-id: 687d04e4-841b-44f7-94ca-bbb20fbe2d8b
feature: Commerce Intelligence, Reporting
source-git-commit: 78bcac16713f9ec87faf7029732972db73216e79
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 0%

---

# [!DNL Commerce Intelligence] herramientas

Utilice las herramientas de Commerce Intelligence para obtener la información que se utiliza para tomar decisiones comerciales correctas.

## [!DNL Commerce Intelligence] account

Cuando activa una [!DNL Commerce Intelligence] cuenta a través del Adobe, obtiene acceso a cinco paneles con aproximadamente 70 informes. Estos informes están diseñados para proporcionar perspectivas sobre sus datos y responder a preguntas como &quot;¿Cómo crecen mis pedidos mes tras mes?&quot;, &quot;¿Quiénes son mis clientes más fieles?&quot; y &quot;¿Funciona mi estrategia de cupones?&quot; Para obtener información detallada sobre este conjunto de herramientas, consulte la [Guía del usuario de Commerce Intelligence][1].

## [!DNL Advanced Reporting]

[!DNL Advanced Reporting] se incluye con Adobe Commerce y Magento Open Source. Esta función le permite acceder a un conjunto de informes dinámicos basados en los datos de sus productos, pedidos y clientes, con un tablero personalizado adaptado a sus necesidades comerciales. While [!DNL Advanced Reporting] utiliza [!DNL Commerce Intelligence] para Analytics, no es necesario tener una cuenta de Commerce Intelligence que utilizar [!DNL Advanced Reporting].

Para obtener información técnica, consulte la [[!DNL Advanced Reporting]][2]{:target=&quot;_blank&quot;} tema en la documentación para desarrolladores.

>[!NOTE]
>
>Debido a problemas de compatibilidad con [!DNL Adobe Commerce Intelligence], Commerce no puede admitir temporalmente los informes avanzados utilizando AWS S3 Bucket como medio para el archivo de datos de origen en [!DNL Commerce Intelligence].

![Panel de informes avanzados](./assets/reporting-advanced.png){width="700"}

### Requisitos

* El sitio web debe ejecutarse en un servidor web público.

* El dominio debe tener un certificado de seguridad (SSL) válido.

* [!DNL Commerce] debe haberse instalado o actualizado correctamente sin errores.

* En el [!DNL Commerce] configuración para [almacenar direcciones URL](../stores-purchase/store-urls.md), el **[!UICONTROL Base URL (Secure)]** la configuración de la vista de tienda debe apuntar a la dirección URL segura. Por ejemplo: `https://yourdomain.com`.

* En el [!DNL Commerce] configuración para URL de tienda, **[!UICONTROL Use Secure URLs on Storefront]** y **[!UICONTROL Use Secure URLs in Admin]** se debe establecer en `Yes`.

* [[!DNL Commerce] crontab][3] se crea y los trabajos cron se ejecutan en el servidor instalado.

>[!NOTE]
>
>[!DNL Advanced Reporting] solo se puede utilizar con [!DNL Commerce] instalaciones que han utilizado continuamente un único [divisa base](../stores-purchase/currency-configuration.md).


### Paso 1: Habilitar [!DNL Advanced Reporting]

En el [!DNL Commerce] configuración, [[!DNL Advanced Reporting]](../configuration-reference/general/advanced-reporting.md) está habilitado de forma predeterminada y se inicia automáticamente si cron está [configurado](../configuration-reference/advanced/system.md) y corriendo. Se inicia un intento de establecer la suscripción al principio de cada hora durante las siguientes 24 horas hasta que se realice correctamente. El estado de la suscripción es &quot;pendiente&quot; hasta que la suscripción se haya establecido correctamente.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo donde **[!UICONTROL General]** está expandido, elija **[!UICONTROL Advanced Reporting]** y haga lo siguiente:

   * Compruebe que **[!UICONTROL Advanced Reporting Service]** se establece en `Enable` (la configuración predeterminada).

   * Configure las variables **[!UICONTROL Time of day to send data]** a la hora, los minutos y los segundos, según un reloj de 24 horas, que desea que el servicio reciba datos actualizados de su tienda. De forma predeterminada, los datos se envían a las 2:00 a. m.

   * En **[!UICONTROL Industry Data]**, elija la **[!UICONTROL Industry]** que mejor describe su negocio.

   ![Configuración avanzada de informes](./assets/advanced-reporting-config.png){width="400"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le solicite, haga clic en **[[!UICONTROL Cache Management]](../systems/cache-management.md)** en el mensaje que hay en la parte superior de la página y actualice las cachés no válidas.

1. Espere durante la noche o hasta después de la hora de la próxima actualización programada. A continuación, compruebe el estado de su suscripción. Si el estado sigue siendo _pendiente_, asegúrese de que la instalación cumple todos los requisitos.

### Paso 2: Acceso [!DNL Advanced Reporting]

1. Realice una de las siguientes acciones:

   * En el _Administrador_ barra lateral, elija **[!UICONTROL Dashboard]**. A continuación, haga clic en **[!UICONTROL Go to Advanced Reporting]**.
   * En el _Administrador_ barra lateral, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Business Intelligence]_>**[!UICONTROL Advanced Reporting]**.

   El [!DNL Advanced Reporting] El tablero proporciona un resumen rápido de sus pedidos, clientes y productos. Asegúrese de desplazarse hacia abajo para ver el panel completo.

1. Para obtener una mejor vista de los datos, establezca el **[!UICONTROL Filters]** en la esquina superior derecha, seleccione el período de tiempo y la vista de tienda que desee incluir en el informe. A continuación, haga lo siguiente:

   * Pase el ratón sobre cualquier punto de datos para obtener más información.
   * Para ver todos los informes de tablero, haga clic en cada pestaña.

   ![Punto de datos](./assets/reporting-advanced-data-point.png){width="600" zoomable="yes"}

## Acceso [!DNL Advanced Reporting] recursos de datos

En la esquina superior derecha del panel de informes avanzados, haga clic en **[!UICONTROL Additional Resources]**.

![Recursos de datos de informes avanzados](./assets/advanced-reporting-your-data-resources.png){width="600" zoomable="yes"}

## Resolución de problemas

Si recibe el mensaje &quot;Página no encontrada&quot; 404, compruebe que su tienda cumple los requisitos de [!DNL Advanced Reporting]. A continuación, siga las instrucciones para comprobar que la integración está instalada.

### Compruebe que la integración esté activa

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integration]**.

1. Compruebe que la variable **[!UICONTROL Magento Analytics user]** La integración de aparece en la lista y **[!UICONTROL Status]** es `Active`.

1. Para restablecer el usuario, haga clic en **[!UICONTROL Reauthorize]** y haga lo siguiente:

   ![Volver a autorizar](./assets/advanced-reporting-integration-reauthorize.png){width="600"}

   * Cuando se le solicite, haga clic en **[!UICONTROL Reauthorize]** para aprobar el acceso a los recursos de la API.

     ![Volver a autorizar el acceso a los recursos API](./assets/advanced-reporting-integration-api.png){width="600"}

   * Compruebe que la lista de tokens de integración para extensiones está completa. A continuación, haga clic en **Listo**.

     ![Tokens de integración](./assets/advanced-reporting-integration-tokens-for-extensions.png){width="600"}

1. Busque el mensaje que indica la integración `Magento Analytics user` se ha vuelto a autorizar.

1. Espere durante la noche o hasta después de la hora de la próxima actualización programada.

### Verificar moneda base única

[!DNL Advanced Reporting] solo se puede utilizar con [!DNL Commerce] instalaciones que solo han utilizado una única [divisa base](../stores-purchase/currency-configuration.md) desde el momento de la instalación. El resultado es que en el historial, todos los pedidos utilizan la misma moneda base. [!DNL Advanced Reporting] no funciona si ha cambiado en cualquier momento la divisa de base y tiene pedidos en el historial procesados con distintas divisas de base.

Para determinar si la tienda tiene varias monedas base, puede consultar su [!DNL Commerce] base de datos desde la línea de comandos utilizando el siguiente ejemplo de MySQL. Es posible que deba cambiar los nombres de las tablas para que coincidan con la estructura de datos:

```sql
select distinct base_currency_code from sales_order;
```

### Discrepancia de datos

Si observa que la variable `Data last updated...` El pie de ilustración muestra la fecha de ayer y no la de hoy. Es posible que haya un retraso de hasta un día en las actualizaciones de informes avanzados. Este retraso se debe a que el tamaño de la cola es mayor de lo esperado.

## Informes del panel

**[!UICONTROL Orders]**

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Revenue] | Muestra todos los ingresos recibidos por la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Orders] | Muestra todos los pedidos realizados a través de la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL AOV] | Muestra el valor de pedido promedio realizado a través de la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Refunds] | Muestra todas las devoluciones procesadas a través de la vista de tienda durante el periodo de tiempo definido. |
| [!UICONTROL Tax Collected] | Muestra todos los impuestos recopilados a través de la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Shipping Collected] | Muestra todas las tarifas de envío recopiladas a través de la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Orders by Status] | Muestra el número de pedidos por estado para la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Orders by Status] | Muestra un resumen del número de pedidos por estado. |
| [!UICONTROL Coupon Usage] | Enumera todos los códigos de cupón y el número de usuarios de cada uno, canjeados a través de la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Orders and Revenue by Billing Region] | Enumera el número de pedidos e ingresos por región para la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Tax Collected by Billing Region] | Muestra el importe de los impuestos recopilados por región para la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Shipping Fees Collected by Shipping Region] | Indica las tarifas de envío recopiladas por región para la vista de tienda durante el período de tiempo definido. |

{style="table-layout:auto"}

**[!UICONTROL Customers]**

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Unique Customers] | Muestra el número de cuentas de cliente únicas asociadas a la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL New Registered Accounts] | Muestra el número de cuentas de cliente nuevas registradas con la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Top Coupon Users] | Muestra los principales usuarios de cupones por ID de cliente y el número de pedidos realizados con cupones en la vista de tienda durante el periodo de tiempo definido. |
| [!UICONTROL Customer KPI Table] | Indica el número de pedidos, los ingresos y el valor de pedido promedio por ID de cliente para la vista de tienda durante el período de tiempo definido. |

{style="table-layout:auto"}

**[!UICONTROL Products]**

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Quantity of Products Sold] | Muestra el número de productos vendidos a través de la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Products Added to Wishlists] | Enumera todos los productos agregados a las listas de deseos a través de la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Best Selling Products by Quantity] | Enumera los productos más vendidos y la cantidad vendida a través de la vista de tienda durante el período de tiempo definido. |
| [!UICONTROL Best Selling Products by Revenue] | Enumera los productos más vendidos y los ingresos generados por la venta del producto a través de la vista de tienda durante el período de tiempo definido. |

{style="table-layout:auto"}


[1]: https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/guide-overview.html
[2]: https://developer.adobe.com/commerce/php/development/advanced-reporting/
[3]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
