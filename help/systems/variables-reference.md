---
title: Referencia de variables
description: Revise ejemplos de plantillas de correo electrónico utilizadas frecuentemente y sus variables asociadas.
exl-id: b5e49a56-4b7c-431d-bd44-e8591106fa4e
role: Admin, User
feature: System, Variables, Communications
TQID: https://experienceleague.adobe.com/FAJe-nOanaUmPT9Is9-ZGevULFepFE6QyyrbGhcCePY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 0%

---

# Referencia de variables

La mayoría de las [plantillas de correo electrónico](email-template-custom.md) tienen una sección de [variables predefinidas](variables-predefined.md) específicas de la plantilla. La siguiente lista incluye ejemplos de plantillas de correo electrónico utilizadas frecuentemente y sus variables asociadas.

## Variables de plantilla de correo electrónico

| Variable | Etiqueta de marcado |
|--- |--- |
| [!UICONTROL Email Footer Template] | `{{template config_path="design/email/footer_template"}}` |
| [!UICONTROL Email Header Template] | `{{template config_path="design/email/header_template"}}` |
| [!UICONTROL Email Logo Image Alt] | `{{var logo_alt}}` |
| [!UICONTROL Email Logo Image URL] | `{{var logo_url}}` |
| [!UICONTROL Email Logo Image Height] | `{{var logo_height}}` |
| [!UICONTROL Email Logo Image Width] | `{{var logo_width}}` |
| [!UICONTROL Template CSS] | `{{var template_styles\|raw}}` |

{style="table-layout:auto"}

## Almacenar variables de información de contacto

| Variable | Etiqueta de marcado |
|--- |--- |
| [!UICONTROL Base Unsecure URL] | `{{config path="web/unsecure/base_url"}}` |
| [!UICONTROL Base Secure URL] | `{{config path="web/secure/base_url"}}` |
| [!UICONTROL General Contact Name] | `{{config path="trans_email/ident_general/name"}}` |
| [!UICONTROL General Contact Email] | `{{config path="trans_email/ident_general/email"}}` |
| [!UICONTROL Sales Representative Contact Name] | `{{config path="trans_email/ident_sales/name"}}` |
| [!UICONTROL Sales Representative Contact Email] | `{{config path="trans_email/ident_sales/email"}}` |
| [!UICONTROL Customer Support Name] | `{{config path="trans_email/ident_support/name"}}` |
| [!UICONTROL Customer Support Email] | `{{config path="trans_email/ident_support/email"}}` |
| [!UICONTROL Custom1 Contact Name] | `{{config path="trans_email/ident_custom1/name"}}` |
| [!UICONTROL Custom1 Contact Email] | `{{config path="trans_email/ident_custom1/email"}}` |
| [!UICONTROL Custom2 Contact Name] | `{{config path="trans_email/ident_custom2/name"}}` |
| [!UICONTROL Custom2 Contact Email] | `{{config path="trans_email/ident_custom2/email"}}` |
| [!UICONTROL Store Name] | `{{config path="general/store_information/name"}}` |
| [!UICONTROL Store Phone Telephone] | `{{config path="general/store_information/phone"}}` |
| [!UICONTROL Store Hours] | `{{config path="general/store_information/hours"}}` |
| [!UICONTROL Country] | `{{config path="general/store_information/country_id"}}` |
| [!UICONTROL Region/State] | `{{config path="general/store_information/region_id"}}` |
| [!UICONTROL Zip/Postal Code] | `{{config path="general/store_information/postcode"}}` |
| [!UICONTROL City] | `{{config path="general/store_information/city"}}` |
| [!UICONTROL Street Address 1] | `{{config path="general/store_information/street_line1"}}` |
| [!UICONTROL Street Address 2] | `{{config path="general/store_information/street_line2"}}` |
| [!UICONTROL Store Contact Address] | `{{config path="general/store_information/address"}}` |
| [!UICONTROL VAT Number] | `{{config path="general/store_information/merchant_vat_number"}}` |

{style="table-layout:auto"}

## Nuevas variables de plantilla de cuenta

| Variable | Etiqueta de marcado |
|--- |--- |
| [!UICONTROL Customer Account URL] | `{{var this.getUrl($store, 'customer/account/')}}` |
| [!UICONTROL Customer Email] | `{{var customer.email}}` |
| [!UICONTROL Customer Name] | `{{var customer.name}}` |

{style="table-layout:auto"}

## Nuevas variables de plantilla de pedido

| Variable | Etiqueta de marcado |
|--- |--- |
| [!UICONTROL Billing Address] | `{{var formattedBillingAddress\|raw}}` |
| [!UICONTROL Email Order Note] | `{{var order.getEmailCustomerNote()}}` |
| [!UICONTROL Order ID] | `{{var order.increment_id}}` |
| [!UICONTROL Order Items Grid] | `{{layout handle="sales_email_order_items" order=$order area="frontend"}}` |
| [!UICONTROL Payment Details] | `{{var payment_html\|raw}}` |
| [!UICONTROL Shipping Address] | `{{var formattedShippingAddress\|raw}}` |
| [!UICONTROL Shipping Description] | `{{var order.getShippingDescription()}}` |

{style="table-layout:auto"}
