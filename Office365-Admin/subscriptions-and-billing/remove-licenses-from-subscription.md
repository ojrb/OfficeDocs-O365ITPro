---
title: "Remove licenses from your Office 365 for business subscription"
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
f1_keywords:
- 'O365P_ProductLicenseRemove'
- 'O365M_ProductLicenseRemove'
- 'O365E_ProductLicenseRemove'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management
- Adm_O365
- Adm_TOC
- commerce
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: 9c64d127-e2dd-4ecc-81f5-2f87e5a74803
description: "Learn how to remove a license from your Office 365 for business subscription when the license is already assigned to someone."
---
<!-- Clone: AgentUniversity\admin\Remove-licenses-subscription.md -->

# Remove licenses from your Office 365 for business subscription

You can't remove a license from a subscription if it's assigned to a user. If you want to remove a license that is currently assigned to someone, you'll need to [remove the license from the user](remove-licenses-from-users.md) before you can remove the license from the subscription.

::: moniker range="o365-worldwide"

### Use the admin center (preview) to remove licenses from your subscription

The preview is available to all Microsoft 365 admins, you can opt in by selecting **Try the preview** toggle located at the top of the Home page. For more information, see [About Microsoft 365 admin center preview](../microsoft-365-admin-center-preview.md).

1. In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Products & services</a> page.

2. On the **Products & services** page, find the subscription from which you want to remove licenses, then choose **Add/Remove licenses**.

    [What if I don't see the Add/Remove licenses link?](#what-if-i-dont-see-the-addremove-licenses-link)

3. In the **Total licenses** box, enter the total number of licenses that you need for this subscription, and then choose **Submit change**. For example, if you have 110 licenses and you want to remove 5 of them, enter 105.

::: moniker-end

::: moniker range="o365-worldwide"
### Use the old admin center to remove licenses from your subscription
::: moniker-end

1. In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Subscriptions</a> page.

    If you're using Office 365 Germany, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Subscriptions</a> page.

    If you're using Office 365 operated by 21Vianet, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Subscriptions</a> page.

2. On the **Subscriptions** page, choose the subscription from which you want to remove licenses, then choose **Add/Remove licenses**.

    [What if I don't see the Add/Remove licenses link?](#what-if-i-dont-see-the-addremove-licenses-link)

3. In the **Total licenses** box, enter the total number of licenses that you need for this subscription and then choose **Submit**. For example, if you have 110 licenses and you want to remove 5 of them, enter 105.

## What if I don't see the Add/Remove licenses link?

This section describes the reasons why the **Add/Remove licenses** link might not be available, and what you can do about it.
  
### A credit check is pending

If a credit check is pending, you'll see a "Pending credit check" message, and you won't be able to remove licenses until the credit check is completed. If a credit check is pending, check back later to see if the credit check has completed. Credit checks typically take up to two working days to complete.
  
After the credit check is complete, you should see the **Add/Remove licenses** link in the **Users** section. If so, go to [Remove licenses from your Office 365 for business subscription](#remove-licenses-from-your-office-365-for-business-subscription).
  
### You activated the subscription using a product key

If the subscription was purchased and activated using a 25-character product key product key, you'll see the text "Prepaid". If your subscription was prepaid using a product key, you can't remove licenses because they have already been paid for. However, you can remove the extra licenses when you renew the subscription.
  
### You bought your subscription through a partner

If the subscription was purchased via a partner, you'll see the Volume Licensing Service Center (VLSC) link. If your licenses were purchased via a partner then you can't remove user licenses because they have already been prepaid. 
  
## What you need to know about removing licenses from users in Office 365 for business

- You need to be either a Global admin or a User management admin. For more information, see [About Office 365 admin roles](../add-users/about-admin-roles.md).

- Use these steps to add a license to an existing user account. [Learn how to add a user account and assign a license at the same time](../add-users/add-users.md).

## Articles about managing licenses for your subscription

- [Understand subscriptions and licenses](subscriptions-and-licenses.md)

- [Remove licenses from users](remove-licenses-from-users.md)

- [Assign licenses to users](assign-licenses-to-users.md)

- [Buy licenses for your subscription](buy-licenses.md)

- [Buy another subscription](buy-another-subscription.md)

- [Buy or edit an add-on](buy-or-edit-an-add-on.md)

- [Manage Yammer user licenses](https://docs.microsoft.com/en-us/yammer/manage-yammer-users/manage-yammer-licenses-in-office-365)

## Related links

[Cancel your subscription](cancel-your-subscription.md)