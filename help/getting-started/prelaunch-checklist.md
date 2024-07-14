---
title: Lista de comprobación previa al lanzamiento
description: Utilice esta lista para comprobar los ajustes de configuración necesarios y asegurarse de que todo es correcto antes de que la tienda entre en producción.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Lista de comprobación previa al lanzamiento

Después de completar el diseño, el desarrollo y las pruebas de la tienda, comprueba las siguientes opciones de configuración para asegurarte de que todo es correcto antes de que la tienda _se ponga en marcha_. Para obtener una descripción completa de cada opción de configuración, vea la [_Referencia de configuración_](../configuration-reference/guide-overview.md).

## Configuración general

- [URL de la tienda](../stores-purchase/store-urls.md): comprueba que las URL de la tienda y el administrador sean correctas para un entorno de producción en vivo.
- Certificado de seguridad: antes de iniciar el almacén, instale un certificado de seguridad 100% firmado y de confianza para el dominio especificado en la URL base.
- [Direcciones de correo electrónico de tienda](../getting-started/store-details.md#store-email-addresses): complete todas las direcciones de correo electrónico que se usan para enviar y recibir notificaciones por correo electrónico, como nuevos pedidos, facturas, envíos, notas de crédito, alertas de precios de productos y boletines. Asegúrese de que cada campo contenga una dirección de correo electrónico empresarial válida.

## Configuración de marketing

- [Plantillas de correo electrónico](../systems/email-templates.md): actualice las plantillas de correo electrónico predeterminadas para que reflejen su marca. Si crea plantillas, asegúrese de actualizar la configuración.
- [Comunicaciones de ventas](../stores-purchase/introduction.md#order-management-and-operations) - Asegúrese de que las facturas y los albaranes incluyan la información comercial correcta y reflejen su marca.
- [Herramientas de Google](../merchandising-promotions/google-tools.md) - [!DNL Commerce] proporciona integración con la API de Google para permitir que su empresa utilice Google Analytics y Google AdWords.

## Configuración de ventas

- [Opciones del carro de compras](../stores-purchase/cart-configuration.md) - Observe la configuración del carro de compras para ver si hay algo que desee cambiar, como establecer la cantidad mínima del pedido y la duración de los precios del carro de compras.
- [Opciones de cierre de compra](../stores-purchase/checkout-process.md#checkout-options) - Mira las opciones de cierre de compra, para ver si hay algo que quieras cambiar, como configurar los términos y condiciones y configurar el cierre de compra de los invitados.
- [Impuestos](../stores-purchase/taxes.md) - Asegúrese de que los impuestos estén correctamente configurados de acuerdo con las reglas de impuestos empresariales y los requisitos locales.
- [Métodos de envío](../stores-purchase/delivery.md) - Habilite todos los operadores y métodos de envío para que los use la compañía.
- [PayPal](../stores-purchase/paypal.md): si planeas ofrecer a tus clientes la comodidad de pagar con PayPal, abre una cuenta de comerciante de PayPal y configura una forma de pago. Ejecute algunas transacciones de prueba en el modo de espacio aislado antes de que el almacén se active.
- [Métodos de pago](../stores-purchase/payments.md): habilita los métodos de pago que planeas usar y asegúrate de que estén correctamente configurados. Compruebe la configuración del estado del pedido, la moneda aceptada, los países permitidos, etc.

## Configuración del sistema

[Cron (Tareas programadas)](../systems/cron.md): los trabajos de Cron se usan para procesar correos electrónicos, reglas de precios de catálogo, boletines informativos, alertas de clientes, mapas del sitio de Google, actualizar tasas de cambio, etc. Asegúrese de que los trabajos de Cron están configurados para ejecutarse en el intervalo de tiempo adecuado, en minutos.
