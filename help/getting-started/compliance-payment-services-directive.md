---
title: Cumplimiento de PSD2
description: Conozca los requisitos de la Directiva de servicios de pago (PSD2) que podrían afectar a su tienda.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
TQID: https://experienceleague.adobe.com/paVa-tpYYzrINAPRFs4TOzbp4b4CLJDlxqNlL1gzp2Q
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c32adafa-ed01-4b31-997e-2413013911b0id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f0ca7b10-ef6c-4ee4-b63f-030819bdd1f3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 0%

---

# Cumplimiento de PSD2

A partir del 14 de septiembre de 2019, la Unión Europea exige que todos los comerciantes de la UE y del Reino Unido cumplan los requisitos de [Autenticación sólida del cliente](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) de la Directiva de servicios de pago (PSD2). Se recomienda a los comerciantes de todos los demás países que cumplan con PSD2 como práctica recomendada.

>[!NOTE]
>
>Este tema tiene fines meramente informativos y no debe interpretarse como asesoramiento jurídico. Para determinar si su empresa debe cumplir con alguna obligación legal y cómo debe hacerlo, consulte con su asesor legal.

La autenticación sólida del cliente es un componente clave de PSD2 y requiere dos de los siguientes elementos:

- Algo que solo tiene el cliente (contraseña o PIN)
- Algo que solo el cliente conoce (token de seguridad único generado por teléfono o teclado)
- Algo que solo es el cliente (autenticación biométrica, como una huella digital o reconocimiento facial)

Los bancos europeos pueden rechazar los pagos que no cumplan los requisitos. Sin embargo, es posible que se acepten transacciones de bajo riesgo y bajo valor, y pagos subsiguientes en una suscripción recurrente.

Debido a este cambio significativo y con el fin de garantizar que los pagos de los clientes no se rechacen, Adobe ha introducido los siguientes cambios y recomendaciones para las integraciones de pago nativas de [!DNL Commerce].

| Método de pago | Requisitos de cumplimiento |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | Para la mayoría de las soluciones de PayPal, no es necesario realizar ninguna acción para cumplir con PSD2, ya que los requisitos los gestiona PayPal. Para obtener información sobre soluciones específicas, consulte la nota situada en la parte superior de cada tema de PayPal. |
| [Braintree](../stores-purchase/braintree.md) | A partir del cambio a la extensión instalada en 2.4.0, los requisitos se gestionan dentro del módulo Braintree Payments incluido y no se requiere ninguna acción para cumplir con PSD2. <br /><br />**_Nota:_** Para cumplir con PSD2 usando la integración principal de versiones anteriores, realice una de las siguientes acciones:<br/>- (Recomendado) Instalar la extensión oficial de Braintree Payment Integration desde [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&idx=m2_cloud_prod_default_products&p=0&nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target="_blank"}.<br/>- Habilitar y configurar el método de pago Braintree en la configuración [!DNL Commerce].<br/><br/>Estas integraciones principales anteriores admiten la verificación 3D Secure 2.0. Sin embargo, las implementaciones de Braintree que se ejecutan en JavaScript SDK v2 no admiten 3D Secure 2.0. |
| Otros | Para todas las demás integraciones de pago, comprueba las extensiones disponibles en [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target="_blank"}. Pida a su proveedor de pagos que le recomiende una solución para los requisitos de PSD2. |

{style="table-layout:auto"}
