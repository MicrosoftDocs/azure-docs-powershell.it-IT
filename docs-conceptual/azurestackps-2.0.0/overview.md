---
title: Panoramica di PowerShell per l'amministrazione dell'hub di Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per l'amministrazione dell'hub di Azure Stack con istruzioni per l'installazione e la configurazione.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 04/16/2020
ms.openlocfilehash: 166c5339c95507b8a9ef1a32d46f589b8d792794
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427956"
---
# <a name="azure-stack-hub-module-200"></a>Modulo hub di Azure Stack 2.0.0

## <a name="requirements"></a>Requisiti:

La versione minima supportata dell'hub di Azure Stack è la 2002.

Nota: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Installazione

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.0-preview -AllowPrerelease
```


## <a name="release-notes"></a>Note sulla versione

* Supportato con l'aggiornamento 2002.  

  L'hub di Azure Stack 2.0.0 rappresenta una modifica di rilievo. Il modulo usa il modulo Az invece di AzureRM. È possibile trovare una guida alla migrazione e un elenco di modifiche di rilievo in [Eseguire la migrazione da AzureRM ad Azure PowerShell Az nell'hub di Azure Stack](/azure-stack/operator/azure-stack-powershell-install).