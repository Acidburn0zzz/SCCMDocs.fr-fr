---
title: "Configurer l’inventaire matériel | Appareils mobiles | System Center Configuration Manager"
description: "Configurez l’inventaire matériel pour les appareils mobiles inscrits par Microsoft Intune et System Center Configuration Manager."
ms.custom: na
ms.date: 10/06/2016
ms.prod: configuration-manager
ms.reviewer: na
ms.suite: na
ms.technology:
- configmgr-other
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: 78a0aecc-f775-451e-aa05-56377ec91b1f
caps.latest.revision: 7
author: nbigman
ms.author: nbigman
manager: angrobe
translationtype: Human Translation
ms.sourcegitcommit: 1134bb2f04152288e72d40b1b1083f415cb4e900
ms.openlocfilehash: 59584a5b8953165e7c605c310346a00c4e0d6d51


---
# <a name="how-to-configure-hardware-inventory-for-mobile-devices-enrolled-by-microsoft-intune-and-system-center-configuration-manager"></a>Comment configurer l’inventaire matériel pour les appareils mobiles inscrits par Microsoft Intune et System Center Configuration Manager

*S’applique à : System Center Configuration Manager (Current Branch)*

Dans System Center Configuration Manager, vous pouvez collecter l’inventaire matériel sur des appareils iOS, Android et Windows à l’aide du connecteur Microsoft Intune. Pour plus d’informations sur la manière de configurer l’inventaire matériel, consultez [Guide pratique pour étendre l’inventaire matériel dans System Center Configuration Manager](../../../../core/clients/manage/inventory/extend-hardware-inventory.md).  

 Pour plus d’informations sur la façon d’inscrire vos appareils auprès de Microsoft Intune, consultez [Gérer les appareils mobiles avec Microsoft Intune](https://technet.microsoft.com/en-us/library/dn646962.aspx).  

## <a name="hardware-inventory-for-mobile-devices"></a>Inventaire matériel pour les appareils mobiles  
 Les tableaux suivants répertorient les classes d’inventaire disponibles pour l’inventaire matériel sur les plateformes mobiles couramment utilisées.  

 **iOS**  

|Classe d'inventaire matériel|iOS|  
|------------------------------|---------|  
|Nom|Device_ComputerSystem.DeviceName|  
|ID d'appareil unique|Device_ComputerSystem.UDID|  
|Numéro de série|Device_ComputerSystem.SerialNumber|  
|Adresse de messagerie|Device_Email.OwnerEmailAddress|  
|Type de système d'exploitation|Non applicable|  
|Version du système d'exploitation|Device_OSInformation.OSVersion|  
|Version de build|Non applicable|  
|Version majeure du Service Pack|Non applicable|  
|Version mineure du Service Pack|Non applicable|  
|Langue du système d'exploitation|Non applicable|  
|Espace de stockage total|Device_Memory.DeviceCapacity|  
|Espace de stockage libre|Device_Memory.AvailableDeviceCapacity|  
|IMEI (International Mobile Equipment Identity)|Device_ComputerSystem.IMEI|  
|MEID (Mobile Equipment Identifier)|Device_ComputerSystem.MEID|  
|Fabricant|Non applicable|  
|Modèle|ModelName|  
|Numéro de téléphone<sup>1</sup>|Device_ComputerSystem.PhoneNumber|  
|Opérateur de l'abonné|Device_ComputerSystem.SubscriberCarrierNetwork|  
|Technologie cellulaire|Device_ComputerSystem.CellularTechnology|  
|Adresse MAC du réseau Wi-Fi|Device_WLAN.WiFiMAC|  

 **Android**  

> [!NOTE]  
>  **REMARQUE :** les classes d’inventaire Android sont disponibles lors de l’utilisation de l’application Portail d’entreprise Android.  

|Classe d'inventaire matériel|Android|  
|------------------------------|-------------|  
|Nom|Non applicable|  
|ID d'appareil unique|Non applicable|  
|Numéro de série|Device_ComputerSystem.SerialNumber|  
|Adresse de messagerie|Non applicable|  
|Type de système d'exploitation|Device_OSInformation.Platform|  
|Version du système d'exploitation|Device_OSInformation.Version|  
|Version de build|Non applicable|  
|Version majeure du Service Pack|Non applicable|  
|Version mineure du Service Pack|Non applicable|  
|Langue du système d'exploitation|Non applicable|  
|Espace de stockage total|Device_Memory.StorageTotal|  
|Espace de stockage libre|Device_Memory.StorageFree|  
|IMEI (International Mobile Equipment Identity)|Device_ComputerSystem.IMEI|  
|MEID (Mobile Equipment Identifier)|Non applicable|  
|Fabricant|Device_Info.Manufacturer|  
|Modèle|Device_Info.Model|  
|Numéro de téléphone<sup>1</sup>|Device_ComputerSystem.PhoneNumber|  
|Opérateur de l'abonné|Device_ComputerSystem.SubscriberCarrierNetwork|  
|Technologie cellulaire|Device_ComputerSystem.CellularTechnology|  
|Adresse MAC du réseau Wi-Fi|Device_WLAN.WiFiMAC|  

 **Windows Phone 8/8.1**  

|Classe d'inventaire matériel|Windows Phone 8 et Windows Phone 8.1|  
|------------------------------|-------------------------------------------|  
|Nom|Device_ComputerSystem.DeviceName|  
|ID d'appareil unique|Device_ComputerSystem.DeviceClientID|  
|Numéro de série|Non applicable|  
|Adresse de messagerie|Device_Email.OwnerEmailAddress|  
|Type de système d'exploitation|Device_OSInformation.Platform|  
|Version du système d'exploitation|Device_ComputerSystem.SoftwareVersion|  
|Version de build|Non applicable|  
|Version majeure du Service Pack|Non applicable|  
|Version mineure du Service Pack|Non applicable|  
|Langue du système d'exploitation|Device_OSInformation.Language|  
|Espace de stockage total|Non applicable|  
|Espace de stockage libre|Non applicable|  
|IMEI (International Mobile Equipment Identity)|Non applicable|  
|MEID (Mobile Equipment Identifier)|Non applicable|  
|Fabricant|Device_ComputerSystem.DeviceManufacturer|  
|Modèle|Device_ComputerSystem.DeviceModel|  
|Numéro de téléphone<sup>1</sup>|Non applicable|  
|Opérateur de l'abonné|Non applicable|  
|Technologie cellulaire|Non applicable|  
|Adresse MAC du réseau Wi-Fi|Non applicable|  

 **Windows RT**  

|Classe d'inventaire matériel|Windows RT|  
|------------------------------|----------------|  
|Nom|Device_ComputerSystem.DeviceName|  
|ID d'appareil unique|Device_ComputerSystem.DeviceName|  
|Numéro de série|Non applicable|  
|Adresse de messagerie|Device_Email.OwnerEmailAddress|  
|Type de système d'exploitation|CCM_OperatingSystem .SystemType|  
|Version du système d'exploitation|Win32_OperatingSystem.version|  
|Version de build|Win32_OperatingSystem.BuildNumber|  
|Version majeure du Service Pack|Win32_OperatingSystem.ServicePackMajorVersion|  
|Version mineure du Service Pack|Win32_OperatingSystem.ServicePackMinorVersion|  
|Langue du système d'exploitation|Non applicable|  
|Espace de stockage total|Win32_PhysicalMemory.Capacity|  
|Espace de stockage libre|Win32_OperatingSystem.FreePhysicalMemory|  
|IMEI (International Mobile Equipment Identity)|Non applicable|  
|MEID (Mobile Equipment Identifier)|Non applicable|  
|Fabricant|Win32_ComputerSystem.Manufacturer|  
|Modèle|Win32_ComputerSystem.Model|  
|Numéro de téléphone<sup>1</sup>|Non applicable|  
|Opérateur de l'abonné|Non applicable|  
|Technologie cellulaire|Non applicable|  
|Adresse MAC du réseau Wi-Fi|Win32_NetworkAdapter.MACAddress|  

 <sup>1</sup> Le numéro de téléphone est masqué par des * sauf les 4 derniers chiffres.  

 Pour que l’inventaire recueille le numéro de téléphone, une carte SIM doit être insérée dans l’appareil et un numéro de téléphone mis en service par l’opérateur de cette carte SIM.  



<!--HONumber=Nov16_HO1-->


