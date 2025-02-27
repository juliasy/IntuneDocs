---
# required metadata

title: Network endpoints for Microsoft Intune
titleSuffix: 
description: Review endpoints for Intune.
keywords:
author: ErikjeMS
ms.author: erikje
manager: dougeby
ms.date: 05/30/2019
ms.topic: conceptual
ms.service: microsoft-intune
ms.localizationpriority: high
ms.technology:
ms.assetid:

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: angerobe
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-classic; get-started
ms.collection: M365-identity-device-management
---

# Network endpoints for Microsoft Intune

This page lists IP addresses and port settings needed for proxy settings in your Intune deployments.

As a cloud-only service, Intune doesn't require on-premises infrastructure such as servers or gateways.

To manage devices behind firewalls and proxy servers, you must enable communication for Intune.

- The proxy server must support both **HTTP (80)** and **HTTPS (443)** because Intune clients use both protocols. Windows Information Protection uses port 444.
- For some tasks (like downloading software updates for the classic pc agent), Intune requires unauthenticated proxy server access to manage.microsoft.com

You can modify proxy server settings on individual client computers. You can also use Group Policy settings to change settings for all client computers located behind a specified proxy server.


<!--
> [!NOTE] If Windows 8.1 devices haven't cached proxy server credentials, enrollment might fail because the request doesn't prompt for credentials. Enrollment fails without warning as the request wait for a connection. If users might experience this issue, instruct them to open their browser settings and save proxy server settings to enable a connection.   -->

Managed devices require configurations that let **All Users** access services through firewalls.

The following tables list the ports and services that the Intune client accesses:

|**Domains**|**IP address**|
|---------------------|-----------|
|login.microsoftonline.com | More information [Office 365 URLs and IP address ranges](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2) |
|portal.manage.microsoft.com<br> m.manage.microsoft.com |52.175.12.209<br>20.188.107.228<br>52.138.193.149<br>51.144.161.187<br>52.160.70.20<br>52.168.54.64 |
| sts.manage.microsoft.com | 13.93.223.241 <br>52.170.32.182 <br>52.164.224.159 <br>52.174.178.4 <br>13.75.122.143 <br>52.163.120.84|
|Manage.microsoft.com <br>i.manage.microsoft.com <br>r.manage.microsoft.com <br>a.manage.microsoft.com <br>p.manage.microsoft.com <br>EnterpriseEnrollment.manage.microsoft.com <br>EnterpriseEnrollment-s.manage.microsoft.com | 40.83.123.72<br>13.76.177.110<br>52.169.9.87<br>52.174.26.23<br>104.40.82.191<br>13.82.96.212|
|portal.fei.msua01.manage.microsoft.com <br>m.fei.msua01.manage.microsoft.com<br>portal.fei.msua02.manage.microsoft.com<br>m.fei.msua02.manage.microsoft.com<br>portal.fei.msua04.manage.microsoft.com <br>m.fei.msua04.manage.microsoft.com<br>portal.fei.msua05.manage.microsoft.com <br>m.fei.msua05.manage.microsoft.com<br>portal.fei.amsua0502.manage.microsoft.com <br>m.fei.amsua0502.manage.microsoft.com<br>portal.fei.msua06.manage.microsoft.com <br>m.fei.msua06.manage.microsoft.com<br>portal.fei.amsua0602.manage.microsoft.com <br>m.fei.amsua0602.manage.microsoft.com<br>fei.amsua0202.manage.microsoft.com <br>portal.fei.amsua0202.manage.microsoft.com <br>m.fei.amsua0202.manage.microsoft.com<br>portal.fei.amsua0402.manage.microsoft.com <br>m.fei.amsua0402.manage.microsoft.com|52.160.70.20<br>52.168.54.64 |
|portal.fei.msub01.manage.microsoft.com <br>m.fei.msub01.manage.microsoft.com<br>portal.fei.amsub0102.manage.microsoft.com <br>m.fei.amsub0102.manage.microsoft.com<br>fei.msub02.manage.microsoft.com <br>portal.fei.msub02.manage.microsoft.com <br>m.fei.msub02.manage.microsoft.com<br>portal.fei.msub03.manage.microsoft.com <br>m.fei.msub03.manage.microsoft.com<br>portal.fei.msub05.manage.microsoft.com <br>m.fei.msub05.manage.microsoft.com<br>portal.fei.amsub0202.manage.microsoft.com <br>m.fei.amsub0202.manage.microsoft.com<br>portal.fei.amsub0302.manage.microsoft.com <br>m.fei.amsub0302.manage.microsoft.com|52.138.193.149<br>51.144.161.187|
|portal.fei.msuc01.manage.microsoft.com <br>m.fei.msuc01.manage.microsoft.com<br>portal.fei.msuc02.manage.microsoft.com <br>m.fei.msuc02.manage.microsoft.com<br>portal.fei.msuc03.manage.microsoft.com <br>m.fei.msuc03.manage.microsoft.com<br>portal.fei.msuc05.manage.microsoft.com <br>m.fei.msuc05.manage.microsoft.com|52.175.12.209<br>20.188.107.228|
|fef.msua01.manage.microsoft.com|138.91.243.97|
|fef.msua02.manage.microsoft.com|52.177.194.236|
|fef.msua04.manage.microsoft.com|23.96.112.28|
|fef.msua05.manage.microsoft.com|138.91.244.151|
|fef.msua06.manage.microsoft.com|13.78.185.97|
|fef.msua07.manage.microsoft.com|52.175.208.218|
|fef.msub01.manage.microsoft.com|137.135.128.214|
|fef.msub02.manage.microsoft.com|137.135.130.29|
|fef.msub03.manage.microsoft.com|52.169.82.238|
|fef.msub05.manage.microsoft.com|23.97.166.52|
|fef.msuc01.manage.microsoft.com|52.230.19.86|
|fef.msuc02.manage.microsoft.com|23.98.66.118|
|fef.msuc03.manage.microsoft.com|23.101.0.100|
|fef.msuc05.manage.microsoft.com|52.230.16.180|
|fef.amsua0202.manage.microsoft.com|52.165.165.17|
|fef.amsua0402.manage.microsoft.com|40.69.157.122|
|fef.amsua0502.manage.microsoft.com|13.85.68.142|
|fef.amsua0602.manage.microsoft.com|52.161.28.64|
|fef.amsub0102.manage.microsoft.com|40.118.98.207|
|fef.amsub0202.manage.microsoft.com|40.69.208.122|
|fef.amsub0302.manage.microsoft.com|13.74.145.65|
|enterpriseregistration.windows.net|52.175.211.189|
|Admin.manage.microsoft.com|52.224.221.227<br>52.161.162.117<br>52.178.44.195<br>52.138.206.56<br>52.230.21.208<br>13.75.125.10|
|wip.mam.manage.microsoft.com|52.187.76.84<br>13.76.5.121<br>52.165.160.237<br>40.86.82.163<br>52.233.168.142<br>168.63.101.57|
|mam.manage.microsoft.com|104.40.69.125<br>13.90.192.78<br>40.85.174.177<br>40.85.77.31<br>137.116.229.43<br>52.163.215.232<br>52.174.102.180|


### Network requirements for Powershell scripts and Win32 apps
If you're using Intune to deploy Powershell scripts or Win32 apps, you'll also need to grant access to endpoints in which your tenant currently resides.

|ASU | Storage name | CDN |
| --- | --- |--- |
| AMSUA0601 | prodmsua06data | https://prodmsua06data.azureedge.net |
| AMSUA0602 | prodamsua0602data | https://prodamsua0602data.azureedge.net |
| AMSUA0101 | prodmsua01data | https://prodmsua01data.azureedge.net |
| AMSUA0201 | prodmsua02data | https://prodmsua02data.azureedge.net |
| AMSUA0202 | Prodmsua0202rcdata | https://prodamsua0202data.azureedge.net/ |
| AMSUA0401 | prodmsua04data | https://prodmsua04data.azureedge.net |
| AMSUA0402 | Prodmsua0402rcdata | https://prodamsua0402data.azureedge.net/ |
| AMSUA0501 | prodmsua05data | https://prodmsua05data.azureedge.net |
| AMSUA0502 | prodmsua0502data | https://prodmsua0502data.azureedge.net |
| AMSUB0101 | prodmsub01data | https://prodmsub01data.azureedge.net |
| AMSUB0102 | prodamsub0102data | https://prodamsub0102data.azureedge.net |
| AMSUB0201 | prodmsub02data | https://prodmsub02data.azureedge.net |
| AMSUB0202 | Prodmsub0202rcdata | https://prodamsub0202data.azureedge.net |
| AMSUB0301 | Prodmsub03data2 | https://prodmsub03data2.azureedge.net |
| AMSUB0302 | Prodmsub0302rcdata | https://prodamsub0302data.azureedge.net |
| AMSUB0501 | prodmsub05data | https://prodmsub05data.azureedge.net |
| AMSUC0101 | prodmsuc01data | https://prodmsuc01data.azureedge.net |
| AMSUC0201 | prodmsuc02data | https://prodmsuc02data.azureedge.net |
| AMSUC0301 | prodmsuc03data | https://prodmsuc03data.azureedge.net |
| AMSUC0501 | prodmsuc05data | https://prodmsuc05data.azureedge.net |
| AMSUA0701 | pemsua07rcdata | https://pemsua07data.azureedge.net |

### Windows Push Notification Services (WNS)
For Intune-managed Windows devices managed using Mobile Device Management (MDM), device actions and other immediate activities require the use of Windows Push Notification Services (WNS). For more information see [Allowing Windows Notification traffic through enterprise firewalls](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).    

### Delivery Optimization port requirements

#### Port requirements
For peer-to-peer traffic, Delivery Optimization uses 7680 for TCP/IP or 3544 for NAT traversal (optionally Teredo). 
For client-service communication, it uses HTTP or HTTPS over port 80/443.

#### Proxy requirements
To use Delivery Optimization, you must allow Byte Range requests. For more information, see [Proxy requirements for Windows Update](https://docs.microsoft.com/windows/deployment/update/windows-update-troubleshooting).

#### Firewall requirements
Allow the following hostnames through your firewall to support Delivery Optimization.
For communication between clients and the Delivery Optimization cloud service:
- *.do.dsp.mp.microsoft.com

For Delivery Optimization metadata:
- *.dl.delivery.mp.microsoft.com
- *.emdl.ws.microsoft.com

### Apple device network information


|Used for|Hostname (IP address/subnet)|Protocol|Port|
|-----|--------|------|-------|
|Retrieving and displaying content from Apple servers|itunes.apple.com<br>\*.itunes.apple.com<br>\*.mzstatic.com<br>\*.phobos.apple.com<br> \*.phobos.itunes-apple.com.akadns.net |    HTTP    |      80      |
|Communications with APNS servers|#-courier.push.apple.com<br>'#' is a random number from 0 to 50.|    TCP     |  5223 and 443  |
|Various functionalities including accessing the World Wide Web, iTunes store, macOS app store, iCloud, messaging, etc. |phobos.apple.com<br>ocsp.apple.com<br>ax.itunes.apple.com<br>ax.itunes.apple.com.edgesuite.net| HTTP/HTTPS |  80 or 443   |

For more information, see Apple's [TCP and UDP ports used by Apple software products](https://support.apple.com/en-us/HT202944), [About macOS, iOS, and iTunes server host connections and iTunes background processes](https://support.apple.com/en-us/HT201999), and [If your macOS and iOS clients aren't getting Apple push notifications](https://support.apple.com/en-us/HT203609).
