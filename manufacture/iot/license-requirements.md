---
author: parameshbabu
Description: 'Detailing OEM license requirements that are necessary to complete in order to commercialize with Windows 10 IoT.'
title: 'OEM license requirements'
ms.author: pabab
ms.date: 08/28/18
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-oem
---

# OEM license requirements

Have questions about commercialization? Check out our Commercialization FAQ [here](CommercializationFAQ.md). 

## Windows 10 IoT Core Services 
 
[Windows 10 IoT Core Services](https://docs.microsoft.com/en-us/windows-hardware/manufacture/iot/iotcoreservicesoverview) is a new cloud services subscription that provides the essential services needed to commercialize a device on Windows 10 IoT Core. For optimal security, update control, and device health, we highly recommend subscribing to Windows 10 IoT Core Services. Through this subscription, OEMs have access to 10 years of support on Windows 10 IoT Core Long Term Servicing Channel (LTSC) releases along with services to manage device updates and assess device health. 
 
## Semi-Annual Channel (SAC) 

If you are handling the maintenance and upkeep of commercialized devices on your own, SAC may be another option for you to consider when commercializing a device. While SAC comes at no cost, you will not have access to the features that Windows 10 IoT Core Services provides. You will also need to come back every six months to renew SAC. 
 
To start your commercialization journey with SAC, you will need to sign a license, which you will need to request the license agreement [here](https://www.surveygizmo.com/s3/4619100/SAC-Commercialization-Agreement). A member of the team will get back to you with the agreement form within 48 to 72 hours.  

You can view a copy of this agreement before requesting to sign it [here](https://az835927.vo.msecnd.net/sites/iot/Resources/documents/Commercial-License.pdf). 


## SMBIOS Support

The system firmware must implement support for SMBIOS that complies with System Management BIOS Reference Specification, Version 2.4 or later. The SMBIOS implementation must follow all conventions and include all required structures and fields as indicated in the SMBIOS Specification, Section 3.2, and follow all conformance requirements as indicated in Section 4. Bit 2 in the BIOS Characteristics Extension Byte 2 field must be set (Section 3.3.1.2.2 of the specification). The length of the Type 1 (System Information) table must be at least 1Bh bytes (includes SKU Number and Family fields from Version 2.4 of the specification).

The following are the minimum required fields in SMBIOS for IoTCore 

* (Table 1, offset 04h) System Manufacturer
* (Table 1, offset 05h) System Product Name
* (Table 1, offset 19h) System SKU
* (Table 1, offset 1Ah) System Family
* (Table 2, offset 05h) Baseboard Product

These fields gain prominence as fields which will be used for identifying unique system configurations for telemetry and servicing. The *Manufacturer*, *Product Name*, *SKU Number* and *Family* fields must not be longer than 64 characters in length. Avoid leading or trailing spaces or other invisible characters.

> [!TIP]
> Design Notes: SKU Number has been moved to a required field in order to improve telemetry reporting. We encourage the OEM to be careful to fill in *Manufacturer* consistently and to fill in *SKU Number* with a value that can identify what the OEM considers a unique system configuration for telemetry and servicing.

For more information, see Section **System.Fundamentals.SMBIOS** in *WHCP-Systems-Specification.pdf* available at [Windows Hardware Compatibility Program Specifications and Policies](https://docs.microsoft.com/windows-hardware/design/compatibility/whcp-specifications-policies) .

> [!IMPORTANT]
> If you are re-using the BIOS/Firmware/UEFI, make sure make sure to update the entries.


## Compliance with minimum hardware requirements

Review the IoT Core sections of [minimum hardware requirements](https://msdn.microsoft.com/library/windows/hardware/dn915086(v=vs.85).aspx).


