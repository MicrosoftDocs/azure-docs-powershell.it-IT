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
ms.openlocfilehash: 72974ac2fec42da962513c161c506e83f047bfb6
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427378"
---
# <a name="azure-stack-module-172"></a>Modulo di Azure Stack 1.7.2

## <a name="requirements"></a>Requisiti:

La versione minima supportata di Azure Stack è la 1904.

Nota: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Installazione

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a>Note sulla versione

* Supportato con l'aggiornamento 1904
* Questa è una versione con modifiche che causano interruzioni. Per informazioni dettagliate, fare riferimento a <https://aka.ms/azspshmigration170>
* Modifica che causa un'interruzione: passaggio dal backup alla modalità di crittografia basata su certificato. Il supporto delle chiavi simmetriche è deprecato.
* Per informazioni dettagliate, fare riferimento a https://aka.ms/azspshmigration170
* Modulo Azs.Storage.Admin 
* Correzione dei bug - In assenza di valori, la nuova quota di archiviazione usa quelli predefiniti.