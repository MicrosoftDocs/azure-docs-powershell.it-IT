---
title: Panoramica di PowerShell per Azure Stack | Microsoft Docs
description: Panoramica dell'installazione e della configurazione di PowerShell per Azure Stack.
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: f895992b4200f260189b3dbc541452e73a377b00
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
---
# <a name="azure-stack-powershell"></a>PowerShell per Azure Stack

Azure Stack richiede i due moduli PowerShell seguenti:  

1. Il modulo **AzureRM** compatibile con Azure Stack, disponibile installando il profilo di versione API **2017-03-09-profile**. I cmdlet installati con questo profilo possono essere usati solo dagli operatori e dagli utenti di Azure Stack.

2. La versione più recente è l'installazione **1.2.11** del modulo **AzureStack**. I cmdlet installati con questo modulo possono essere usati solo dagli operatori di Azure Stack. Un operatore può eseguire operazioni come la gestione di offerte, piani, servizi, quote e così via usando i cmdlet di PowerShell disponibili in questo modulo. Per informazioni sui cmdlet di PowerShell disponibili in questo modulo, vedere i contenuti di riferimento su [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) e [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage).

## <a name="next-steps"></a>Passaggi successivi

* [Installare PowerShell per Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [Configurare PowerShell per l'uso con Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
