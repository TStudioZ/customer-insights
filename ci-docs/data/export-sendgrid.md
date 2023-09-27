---
title: "Export segments to SendGrid (preview)"
description: "Learn how to configure the connection and export to SendGrid."
ms.date: 09/01/2023
ms.reviewer: mhart
ms.topic: how-to
author: pkieffer
ms.author: philk
---

# Export segments to SendGrid (preview)

[!INCLUDE [public-preview-banner](includes/public-preview-banner.md)]

[!INCLUDE [consolidated-sku](./includes/consolidated-sku.md)]

Export segments of unified customer profiles to SendGrid contact lists and use them for campaigns and email marketing in SendGrid.

## Prerequisites

- A [SendGrid account](https://sendgrid.com/) and corresponding administrator credentials.
- [Existing contact lists in SendGrid](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts) and the corresponding IDs.
- A [SendGrid API key](https://sendgrid.com/docs/ui/account-and-settings/api-keys/).
- [Configured segments](segments.md).
- Unified customer profiles in the exported segments contain a field representing an email address.

## Known limitations

- Private link in combination with Bring your own storage (BYOS) is not supported.
- Up to 100,000 customer profiles in total to SendGrid, which can take up to a few hours to complete. The number of customer profiles that you can export to SendGrid depends on your contract with SendGrid.
- Segments only.

## Set up connection to SendGrid

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Go to **Settings** > **Connections**.

1. Select **Add connection** and choose **SendGrid**.

1. Give your connection a recognizable name in the **Display name** field. The name and the type of the connection describe this connection. We recommend choosing a name that explains the purpose and target of the connection.

1. Choose who can use this connection. By default, it's only administrators. For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Enter your **SendGrid API key**.

1. Review the [data privacy and compliance](connections.md#data-privacy-and-compliance) and select **I agree**.

1. Select **Connect** to initialize the connection.

1. Select **Add yourself as export user** and provide your Dynamics 365 Customer Insights - Data credentials.

1. Select **Save** to complete the connection.

## Configure an export

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Go to **Data** > **Exports**.

1. Select **Add export**.

1. In the **Connection for export** field, choose a connection from the SendGrid section. Contact an administrator if no connection is available.

1. Enter a name for the export.

1. Enter your **SendGrid list ID**.

1. In the **Data matching** section, in the **Email** field, select the field that represents a customer's email address.

1. Optionally, select fields such as **First name**, **Last name**, **Country/Region**, **State**, **City**, and **Post code**.

1. Select the segments you want to export following the known limitations.

1. Select **Save**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]