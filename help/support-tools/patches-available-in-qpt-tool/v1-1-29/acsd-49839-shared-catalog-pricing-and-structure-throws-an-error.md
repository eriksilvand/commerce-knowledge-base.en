---
title: "ACSD-49839: Shared catalog pricing and structure throws an error"
description: Apply the ACSD-49839 patch to fix the Adobe Commerce issue where the shared catalog pricing and structure throws an error in the admin when products have single or double quotes in SKU.
---
# ACSD-49839: Shared catalog pricing and structure throws an error

The ACSD-49839 patch fixes the issue where the shared catalog pricing and structure throws an error in the admin when products have single or double quotes in SKU. This patch is available when the [[!DNL Quality Patches Tool (QPT)]](/help/announcements/adobe-commerce-announcements/magento-quality-patches-released-new-tool-to-self-serve-quality-patches.md) 1.1.29 is installed. The patch ID is ACSD-49839. Please note that the issue is scheduled to be fixed in Adobe Commerce 2.4.7.

## Affected products and versions

**The patch is created for Adobe Commerce version:**

* Adobe Commerce (all deployment methods) 2.4.5-p1

**Compatible with Adobe Commerce versions:**

* Adobe Commerce (all deployment methods) 2.3.7 - 2.4.6

>[!NOTE]
>
>The patch might become applicable to other versions with new [!DNL Quality Patches Tool] releases. To check if the patch is compatible with your Adobe Commerce version, update the `magento/quality-patches` package to the latest version and check the compatibility on the [QPT landing page](https://experienceleague.adobe.com/tools/commerce-quality-patches/index.html). Use the patch ID as a search keyword to locate the patch.

## Issue

The shared catalog pricing and structure throws an error in the admin when products have single or double quotes in SKU.

<u>Steps to reproduce</u>:

1. Set some of the product SKUs with a special character, i.e., double quotes such as:
*[Product"12, Product"14, Product"15]*.
1. Go to **[!UICONTROL Admin]** > **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalog]** > **[!UICONTROL Add Shared Catalog]** (for e.g.,*[Test Shared Catalog]*).
1. Assign all **[!UICONTROL Products and Categories]** > **[!UICONTROL Generate Catalog]** > **[!UICONTROL Save]**.
1. Go to **[!UICONTROL Admin]** > **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalog]** > **[!UICONTROL Test Shared Catalog]** > **[!UICONTROL Action]** > **[!UICONTROL Set Pricing and Structure]**.
1. Mark *[!UICONTROL Root Catalog]* to select all categories and products.
1. Observe the AJAX requests in the network panel.

<u>Expected results</u>:

Shared catalog pricing and structure is not throwing an error in the admin when products have single or double quotes in SKU.

<u>Actual results</u>:

Shared catalog pricing and structure is throwing an error in the admin when products have single or double quotes in SKU.

## Apply the patch

To apply individual patches, use the following links depending on your deployment method:

* Adobe Commerce or Magento Open Source on-premises: [[!DNL Quality Patches Tool] > Usage](https://experienceleague.adobe.com/docs/commerce-operations/tools/quality-patches-tool/usage.html) in the [!DNL Quality Patches Tool] guide.
* Adobe Commerce on cloud infrastructure: [Upgrades and Patches > Apply Patches](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/upgrade/apply-patches.html) in the Commerce on Cloud Infrastructure guide.

## Related reading

To learn more about [!DNL Quality Patches Tool], refer to:

* [[!DNL Quality Patches Tool] released: a new tool to self-serve quality patches](/help/announcements/adobe-commerce-announcements/magento-quality-patches-released-new-tool-to-self-serve-quality-patches.md) in our support knowledge base.
* [Check if patch is available for your Adobe Commerce issue using [!DNL Quality Patches Tool]](/help/support-tools/patches-available-in-qpt-tool/check-patch-for-magento-issue-with-magento-quality-patches.md) in our support knowledge base.

For info about other patches available in QPT, refer to [Patches available in QPT](https://experienceleague.adobe.com/tools/commerce-quality-patches/index.html) in the [!DNL Quality Patches Tool] guide.