---
title: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack con istruzioni per l'installazione e la configurazione.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: 6568dc4e6c51e8f250aad2c4dd765c065fe6a8bf
ms.sourcegitcommit: d3069aba7d1ac248aff755e4b21533af1f73251d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2019
ms.locfileid: "58808061"
---
# <a name="azure-stack-module-171"></a>Modulo di Azure Stack 1.7.1

## <a name="requirements"></a>Requirements:

La versione minima supportata di Azure Stack è 1901.

Note: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Installa

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a>Note sulla versione

* Supportato con l'aggiornamento 1901
* Questa è una versione con modifiche che causano interruzioni. Per informazioni dettagliate, fare riferimento a <https://aka.ms/azspshmigration170>
* Azs.Backup.Admin Module * Modifica che causa un'interruzione: passaggio dal backup alla modalità di crittografia basata su certificato. Il supporto delle chiavi simmetriche è deprecato.
* Azs.Fabric.Admin Module       * Deprecato           * Get-AzsInfrastructureVolume è deprecato; ora è fornito il nuovo Get-AzsVolume           * Get-AzsStorageSystem è deprecato; ora è fornito il nuovo cmdlet Get-AzsStorageSubSystem           * Get-AzsStoragePool è deprecato; l'oggetto StorageSubSystem ha la proprietà di capacità
* Azs.Compute.Admin Module           * Correzione dei bug: Add-AzsPlatformImage, Get-AzsPlatformImage : Chiamata a ConvertTo-PlatformImageObject solo nel percorso di riuscita           * Correzione dei bug: Add-AzsVmExtension, Get-AzsVmExtension : Chiamata a ConvertTo-VmExtensionObject solo nel percorso di riuscita
* Modulo Azs.Storage.Admin           * Correzione dei bug - In assenza di valori, la nuova quota di archiviazione usa quelli predefiniti.'
