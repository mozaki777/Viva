---
ms.date: 7/12/2023
title: "Overview of Native Mode for Microsoft 365"
description: "Learn about Native Mode for Microsoft 365."
ms.reviewer: auhosford
ms.author: v-bvrana
author: Starshine89
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Overview of Viva Engage in Native Mode for Microsoft 365 

As of January 2020, all new Viva Engage tenants start in Native Mode.

 > [!NOTE]
> Native Mode is strongly recommended for reasons of security, compliance, and Microsoft 365 integration. Existing Viva Engage tenants are eligible to migrate to Native Mode. The deprecation of hybrid and non-native networks was announced in 2022, and existing non-native networks are being automatically migrated to Native Mode. For more information, see [Automatic Native Mode migration and network consolidation](/viva/engage/automatic-migration-native-mode.md)

## Frequently asked questions

In Native Mode, all Viva Engage users are in Microsoft Entra ID, all groups are Microsoft 365 groups, and all files are stored in SharePoint Online.

 > [!NOTE]
> There are no bandwidth requirements for Native Mode migration because nothing is downloaded. You are essentially moving from a separate Viva Engage site to Microsoft 365 and SharePoint Online. The only consideration is the SharePoint Online quota if Viva Engage has been extensively used.

A tenant must be in one of three modes:

- **Native Mode for Microsoft 365**. In this mode, the network only uses features that allow users, groups, and content to be compatible with and mapped to their counterparts in Microsoft Entra ID and Microsoft 365.

  When Viva Engage content is in Native Mode, you can search for it in the [Microsoft Purview compliance portal](https://go.microsoft.com/fwlink/?linkid=2132455).
  
  In this mode, users and admins can't add features that would take the network out of Native Mode.

- **Non-Native Mode**. In this mode, the network doesn't meet one or more requirements. For example, the network might not enforce Microsoft 365 identity. All external networks and Viva Engage Basic networks are in this mode because they can't connect to Microsoft 365.

- **Hybrid Mode**. In this mode, users and groups might not be associated with their counterparts in Microsoft Entra ID and Microsoft 365, and files might not be stored in SharePoint. The network might be in the process of meeting all requirements for Native Mode, but the admin hasn't committed the network to Native Mode.

> [!NOTE]
> Non-Native and Hybrid modes are being deprecated in 2023.


When you align your network in Native Mode, the [Native Mode Alignment Tool](./native-mode-guide.md) automates the process and guides you through the steps to get there.

 > [!NOTE]
> All Company now works like any other community in Native Mode. Admins can customize All Company and use advanced management features, such as restricting posts and promoting others as admins. For more information, see [All Company now works like other Viva Engage communities](/viva/engage/manage-viva-engage-groups/all-company-community).

## Key differences between modes

### Native Mode

- No one can inadvertently take your network out of Native Mode.
- eDiscovery through the [Microsoft Purview compliance portal](https://go.microsoft.com/fwlink/?linkid=2132455) is supported for your home network.
- All Viva Engage groups, users, and group memberships are managed through Microsoft 365. Management should be done through the Microsoft 365 admin center, Microsoft Entra admin center, or other Microsoft Entra management tools.
- All communities or groups, including All Company, are Microsoft 365-connected, which means they have access to Microsoft 365 features, including live events.
- Viva Engage honors Microsoft 365 group creation rights and enforces Microsoft 365 group creation restrictions.
- Guests can only be added at the community level. But external networks are supported in the [US geo](/viva/engage/manage-security-and-compliance/security-and-compliance).
- All files uploaded to groups are stored in SharePoint.
- Files can't be uploaded to Viva Engage private messages.
- Engage admins (Yammer administrators) must have Microsoft Global administrator privileges or Group admin privileges from Microsoft 365 to administer changes to communities they don't own.

### Non-Native Mode (not connected)

- All Viva Engage users can create communities.
- Files aren't stored in SharePoint.
- Files can be attached to Viva Engage private messages.
- Engage admins (Yammer administrators) aren't required to have any more admin privileges from Microsoft 365 to administer changes to groups.

### Hybrid Mode

- This step on the way to Native Mode lets you learn how Native Mode will work.
- All Viva Engage users can create communities.
- New files uploaded to Microsoft 365-connected groups are stored in SharePoint.
- Files can be attached to Viva Engage private messages.
- Engage admins (Yammer administrators) aren't required to have any other admin privileges from Microsoft 365 to administer changes to groups.

## Related articles

[Troubleshoot problems with Native Mode for Microsoft 365](./troubleshoot-native-mode.md)

[Microsoft Purview compliance portal](https://go.microsoft.com/fwlink/?linkid=2132455)
