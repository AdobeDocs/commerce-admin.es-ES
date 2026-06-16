---
title: Configuración del transportista de envío
description: Obtenga información acerca de la compatibilidad con las cuentas de envío comerciales disponibles en su tienda.
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
TQID: https://experienceleague.adobe.com/zKN3BQWHywAOLJ-zaJX1-8b7aAYxtzl8v9J7uJG1rFg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 496
ht-degree: 0%

---

# Configuración del transportista de envío

Si tiene una cuenta comercial con un transportista admitido, puede ofrecer a sus clientes la comodidad de elegir ese transportista durante el cierre de compra. Las tarifas se descargan automáticamente, por lo que no es necesario buscar la información.

>[!NOTE]
>
>Consulta [Commerce Marketplace](../getting-started/commerce-marketplace.md) para obtener servicios de envío adicionales para tu instalación de Commerce.

Antes de poder ofrecer a sus clientes una selección de transportistas, debe completar los siguientes pasos:

- Configure [configuración de envío](shipping-settings.md) para establecer el punto de origen de su tienda.

- Configure las opciones de cada servicio de operador que desee ofrecer.

   - [**UPS**](ups.md) - United Parcel Service (UPS) ofrece servicios de envío nacionales e internacionales por tierra y aire a más de 220 países.
   - [**USPS**](usps.md) - El Servicio Postal de los Estados Unidos (USPS) es el servicio postal independiente del gobierno de los Estados Unidos. USPS ofrece servicios de envío nacionales e internacionales por tierra y aire.
   - [**FedEx**](fedex.md) - FedEx ofrece servicios de envío nacionales e internacionales por tierra y aire a más de 220 países.
   - [**DHL**](dhl.md) - DHL ofrece servicios internacionales integrados y soluciones adaptadas y centradas en el cliente para administrar y transportar cartas, bienes e información.

## Peso dimensional

El peso dimensional, a veces llamado peso volumétrico, es una práctica común en la industria que basa el precio de transporte en una combinación de peso y volumen de paquete. En términos simples, el peso dimensional determina la tarifa de envío en función de la cantidad de espacio que un paquete ocupa en el área de carga del porteador. El peso dimensional se suele utilizar cuando un paquete es relativamente ligero en comparación con su volumen.

Todos los principales transportistas aplican peso dimensional a algunos envíos. Sin embargo, la forma en que se aplica el precio del peso dimensional varía de un transportista a otro. Si su empresa tiene un gran volumen de envíos, incluso una ligera diferencia en el precio de envío puede traducirse en miles de dólares en el transcurso de un año.

## Configuración

Las opciones de configuración varían para cada operador. Sin embargo, todos requieren los siguientes pasos:

1. Abre una cuenta de envío con el transportista.

1. Introduzca su número de cuenta o ID de usuario, y la URL de la puerta de enlace a su sistema en la configuración de su tienda.

### Desaprobación de la API de herramientas web USPS

Las versiones 2.4.6, 2.4.7 y 2.4.8 de Adobe Commerce usan las API de herramientas web heredadas para la integración de envío lista para usar con USPS. USPS ha introducido las API de USPS, una plataforma basada en REST para reemplazar las API de herramientas web heredadas.

El 25 de enero de 2026, USPS retiró las API de herramientas web heredadas. Después de esta fecha, todas las solicitudes a las API de herramientas web producirán un error.

Para evitar interrupciones en los servicios de envío de USPS, actualice a la versión más reciente de Adobe Commerce o realice las siguientes acciones:

- Aplique el [parche de calidad de migración de la API REST de USPS](https://experienceleague.adobe.com/es/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/v1-1-70/ac-15210) para agregar compatibilidad con la integración con las API REST de USPS.

- Actualice la configuración de Commerce USPS para utilizar las API de REST:

   - [Configuración de transportista de envío USPS](usps.md)

   - [Configuración de etiquetas de envío](shipping-label-create.md)

