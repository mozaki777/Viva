---
title: Set up Secure File Transfer Protocol (SFTP) in Viva Glint
description: Use Microsoft Viva Glint Secure File Transfer Protocol (SFTP) to establish regular, automated imports of employee data.
ms.author: aweixelman
author: AliciaWeixelman
manager: skaradzic
audience: admin
f1.keywords: NOCSH
keywords: sftp, public ip address, pgp encryption, data transfer, ssh key
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 10/18/2023
---

# Set up Secure File Transfer Protocol (SFTP)

Use Microsoft Viva Glint [Secure File Transfer Protocol (SFTP)](https://go.microsoft.com/fwlink/?linkid=2247429) to establish regular, automated imports of employee data. In Viva Glint General Settings, import SSH Public Keys and specify public IP addresses to connect, specify users that should be notified about data uploads and warnings, opt-in to PGP encryption, and view your credentials to access your SFTP account. Your IT team may need to add an IP exception or add hosts and ports to an allow list to connect to SFTP. [Learn more](https://go.microsoft.com/fwlink/?linkid=2238617). 

## Manage SFTP in General Settings

Manage SFTP settings to connect to your Viva Glint SFTP account:

1. From the admin dashboard, select the **Configure** symbol, then in **Service Configuration**, choose **General Settings**.
1. In the **Technical Configuration** section, go to **SFTP Setup** and select **Manage**.
1. In the SFTP pane that appears, review each field and enter information as needed:
   1. **SSH Public Key:** Enter the full text of your public SSH key in this field: `ssh-rsa ...` . **DO NOT** share your private key with Viva Glint. To generate a key pair: [Learn more](https://go.microsoft.com/fwlink/?linkid=2247507).
   1. **SFTP IP Addresses:** Any account that connects to SFTP must have valid public IP addresses added here. Contact your IT team or use [online tools](https://ifconfig.io/) to determine your public IP address(es).
   1. **Notify People:** Search for and add users that should receive file upload notification emails.
   1. **PGP Encryption:** This setting is optional. Switch toggle to **On** to enable file encryption and reveal Glint's public PGP encryption key to encrypt your employee data files.
   1. **SFTP Credentials:** Use the credentials shown here to connect to SFTP with a dedicated FTP application and your private SSH key file. Allow at least 1 hour after entering public SSH keys and IP addresses before testing your connection.

> [!IMPORTANT]
> Private IP ranges aren't internet routable and don't allow SFTP connection. Don't include private IP addresses, which fall in these ranges:
> - **10.0.0.0/8 IP addresses:** 10.0.0.0 – 10.255.255.255
> - **172.16.0.0/12 IP addresses:** 172.16.0.0 – 172.31.255.255
> - **192.168.0.0/16 IP addresses:** 192.168.0.0 – 192.168.255.255
 
> [!NOTE]
> Once a tenant is deprovisioned or considered in a "LockedOut" state, the public SSH key is deleted and SFTP will no longer work.
