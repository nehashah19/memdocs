---
title: Support for the Windows ADK
titleSuffix: Configuration Manager
description: Learn about the Windows Assessment and Deployment Kit (ADK) versions that are supported for OS deployment with Configuration Manager.
ms.date: 09/07/2021
ms.prod: configuration-manager
ms.technology: configmgr-core
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
ms.localizationpriority: medium
---

# Support for the Windows ADK in Configuration Manager

*Applies to: Configuration Manager (current branch)*

When you deploy operating systems with Configuration Manager, the Windows Assessment and Deployment Kit (ADK) is a required external dependency. For more information, see the following articles:

- [Infrastructure requirements for OS deployment](../../../osd/plan-design/infrastructure-requirements-for-operating-system-deployment.md#windows-adk)

- [Download the Windows ADK](/windows-hardware/get-started/adk-install)

    > [!IMPORTANT]
    > Windows PE is a separate installer. Make sure to download both the **Windows ADK** and the **Windows PE add-on for the ADK**.

## Windows ADK versions

The following table lists the versions of the Windows ADK that you can use with different versions of Configuration Manager.

| Windows ADK version | ConfigMgr 2002 | ConfigMgr 2006 | ConfigMgr 2010 | ConfigMgr 2103 | ConfigMgr 2107 |
|------------------------|----------------|----------------|----------------|----------------|----------------|
| **Windows 10, version 1903**<br>(10.1.18362) | ![Supported](media/green-check.png) | ![Backwards compatible](media/blue-compat.png) | ![Backwards compatible](media/blue-compat.png) | ![Not supported](media/red-x.png) | ![Not supported](media/red-x.png) |
| **Windows 10, version 2004**<br>(10.1.19041) | ![Supported](media/green-check.png) | ![Supported](media/green-check.png) | ![Supported](media/green-check.png) | ![Supported](media/green-check.png) | ![Supported](media/green-check.png) |
| **Windows Server 2022**<br>(10.1.20348) | ![Not supported](media/red-x.png) | ![Not supported](media/red-x.png) | ![Not supported](media/red-x.png) | ![Not supported](media/red-x.png) | ![Supported](media/green-check.png) |
| **Windows 11**<br>(10.1.22000) | ![Not supported](media/red-x.png) | ![Not supported](media/red-x.png) | ![Not supported](media/red-x.png) | ![Not supported](media/red-x.png) | ![Supported](media/green-check.png) |

|Key|
|--|
| ![Supported](media/green-check.png) = **Supported** <br/> This table only shows Windows ADK supportability in relation to the version of Configuration Manager. Microsoft recommends using the Windows ADK that matches the version of Windows you're deploying. Use the latest Windows ADK version when deploying the latest Windows version. The latest Windows ADK version may support deployment of older OS versions, such as Windows 8.1.<!-- SCCMDocs issue 1229 --> For more information on Windows ADK component supportability, see [DISM supported platforms](/windows-hardware/manufacture/desktop/dism-supported-platforms) and [USMT requirements](/windows/deployment/usmt/usmt-requirements#bkmk-1). |
| ![Backwards compatible](media/blue-compat.png)  = **Backward compatible** <br/> This combination isn't tested but should work. We'll document any known issues or caveats. |
| ![Not supported](media/red-x.png) = **Not supported** |

## Support notes

- Configuration Manager only supports x86 and amd64 components of the Windows ADK. It doesn't currently support ARM or ARM64 components.

- Windows Server builds have the same Windows ADK requirement as the associated Windows client version. For example, Windows Server 2016 is the same build version as Windows 10 LTSB 2016.

- If you're deploying both Windows 11 and Windows Server 2022, use the Windows ADK for Windows 11, which is the latest version. If you're deploying Windows Server 2022 and not Windows 11, you can use either Windows ADK for Windows Server 2022 or Windows 11.

## Next steps

[Support for Windows 10](support-for-windows-10.md)

[Supported OS versions for clients](supported-operating-systems-for-clients-and-devices.md)