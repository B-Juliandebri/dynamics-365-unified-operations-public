---
title: Place B2B bulk and repeat orders quickly
description: This article describes the capabilities of Microsoft Dynamics 365 Commerce that let business-to-business (B2B) site users quickly place bulk and repeat orders.
author: ShalabhjainMSFT
ms.date: 01/31/2024
ms.topic: article
ms.prod: 
ms.technology: 
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.23
ms.search.industry: retail
ms.search.form: RetailOperations

---

# Place B2B bulk and repeat orders quickly

[!include [banner](../../includes/banner.md)]

This article describes the capabilities of Microsoft Dynamics 365 Commerce that let business-to-business (B2B) site users quickly place bulk and repeat orders.

Dynamics 365 Commerce B2B e-commerce websites let users perform standard operations such as discovering new products via searching and browsing, viewing product details, adding items to the cart, and checking out. However, whereas the customers of business-to-consumer (B2C) sites generally order items in small quantities and order them only once, B2B customers typically order items in large quantities and reorder them multiple times. Because these customers usually know exactly what items they want to buy, they often skip the product discovery phase and move directly to ordering. To meet the needs of these customers, Commerce B2B e-commerce websites provide various capabilities that help them place orders quickly.

More capabilities are in development to further simplify the process of capturing bulk orders.

## Bulk order by item number

Commerce B2B e-commerce websites let site users add items to the cart by entering product item numbers together with the desired quantity.

The following illustration shows an example of quick order entry by product item number.

![Quick order entry by product item number.](../media/QuickAddByItem.png)

## Bulk order by variant

Commerce B2B e-commerce websites let site users quickly add different variants of the same product in a single view that shows inventory availability by size, color, and style. In addition, site users can easily enter the same quantity for all in-stock products by selecting **Enter all quantities**.

The following illustration shows an example of quick order entry where the "enter all quantities" functionality is used.

![Quick order entry that uses the "enter all quantities" functionality.](../media/MatrixView.png)

## Use order templates for quick order entry

Buyers on B2B websites often order specific items together. For example, if you're placing orders for a construction site, you might want to order shirts, jackets, pants, shoes, and hats together. If you're placing orders for a hospital where doctors, nurses, and cleaning staff have different uniforms, you might want to group each uniform type together for easier ordering. For these types of scenarios, Commerce B2B sites enable order templates to be created. Site users can create any number of custom templates and then order all or some of the items from those templates as they require. 

You can create new order templates by going to **My account \> Manage order templates** and selecting **Create an order template**. Another way to create a new order template is to navigate to a product details page (PDP) for an item, select a variant (if applicable), and then select **Add to order template**. This action opens the **Add to order template** view, where you can select **Create new** to create a new order template. 

As of Commerce version 10.0.37, order templates support catalogs. When the catalog feature is enabled, each order template line saves the corresponding catalog information. When users add one or more lines from the order template to their shopping cart, the cart lines get the correct catalog information from the order template lines. Also, a batch job named **Synchronize order templates** is available that syncs order template information from the channel database to headquarters. The **Enable restricting order templates by channel** feature is also available to use so you can restrict the order template to only appear in the channel where the template was created. This is helpful when there are multiple B2B ecommerce websites using the same Commerce Scale Unit (CSU) and you don't want buyers to see all the order templates across all the B2B websites.

> [!NOTE]
> Microsoft recommends that you run the **Synchronize order templates** job at regular intervals (for example, once per day) so that order template information is synced to headquarters. 

The following illustration shows an example of an order template.

![Example of an order template.](../media/OrderTemplateHeader.png)

The following illustration shows an example of the details view for an order template.

![Example of an order template's details view.](../media/OrderTemplateLines.png)

## Reorder from order history

Commerce B2B e-commerce websites let site users quickly reorder items from their order history. Site users can either buy selected items from their order history or add all previously purchased items to the cart.

The following illustration shows an example of a user's order history and the options for reordering items from it.

![Reordering from order history.](../media/Reorder.png)
