---
title: Cumplimiento de PSD2
description: Conozca los requisitos de la Directiva de servicios de pago (PSD2) que podrían afectar a su tienda.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Cumplimiento de PSD2

A partir del 14 de septiembre de 2019, la Unión Europea exige que todos los comerciantes de la UE y del Reino Unido cumplan los requisitos de [Autenticación sólida del cliente](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) de la Directiva de servicios de pago (PSD 2). Se recomienda a los comerciantes de todos los demás países que cumplan con PSD2 como práctica recomendada.

>[!NOTE]
>
>Este tema tiene fines meramente informativos y no debe interpretarse como asesoramiento jurídico. Para determinar si su empresa debe cumplir con alguna obligación legal y cómo debe hacerlo, consulte con su asesor legal.

La autenticación sólida del cliente es un componente clave de PSD2 y requiere dos de los siguientes elementos:

- Algo que solo tiene el cliente (contraseña o PIN)
- Algo que solo el cliente conoce (token de seguridad único generado por teléfono o teclado)
- Algo que solo es el cliente (autenticación biométrica, como una huella digital o reconocimiento facial)

Los bancos europeos pueden rechazar los pagos que no cumplan los requisitos. Sin embargo, es posible que se acepten transacciones de bajo riesgo y bajo valor, y pagos subsiguientes en una suscripción recurrente.

Debido a este cambio significativo y para garantizar que los pagos de los clientes no se rechacen, Adobe ha introducido los siguientes cambios y recomendaciones para las integraciones de pagos nativas de [!DNL Commerce].

| Método de pago | Requisitos de cumplimiento |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | Para la mayoría de las soluciones de PayPal, no es necesario realizar ninguna acción para cumplir con PSD2, ya que los requisitos los gestiona PayPal. Para obtener información sobre soluciones específicas, consulte la nota situada en la parte superior de cada tema de PayPal. |
| [Braintree](../stores-purchase/braintree.md) | A partir del cambio a la extensión instalada en la versión 2.4.0, los requisitos se gestionan dentro del módulo de pagos de Braintree incluido y no se requiere ninguna acción para cumplir con PSD2. <br /><br />**_Nota:_**&#x200B;Para cumplir con PSD2 mediante la integración principal de versiones anteriores, realice una de las siguientes acciones:<br/>- (Recomendado) Instalar la extensión oficial de integración de pagos de Braintree de [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target=&quot;_blank&quot;}.<br/>- Habilitar y configurar el método de pago del Braintree en la configuración de [!DNL Commerce].<br/><br/>Estas integraciones principales anteriores admiten la verificación 3D Secure 2.0. Sin embargo, las implementaciones de Braintree que se ejecutan en el SDK v2 de JavaScript no admiten 3D Secure 2.0. |
| Otros | Para todas las demás integraciones de pagos, comprueba las extensiones disponibles en [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target=&quot;_blank&quot;}. Pida a su proveedor de pagos que le recomiende una solución para satisfacer los requisitos de PSD2. |

{style="table-layout:auto"}
