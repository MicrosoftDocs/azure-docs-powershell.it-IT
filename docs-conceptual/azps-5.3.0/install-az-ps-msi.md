---
title: Installare Azure PowerShell con un file MSI
description: Come installare Azure PowerShell senza PowerShellGet usando un programma di installazione MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: de9ac41b86e97c948943d22b2019c8022bdf52e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893721"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installare Azure PowerShell in Windows con un programma di installazione MSI

Questo articolo illustra come installare Azure PowerShell in Windows con un programma di installazione MSI. Il programma di installazione MSI viene fornito per gli ambienti in cui PowerShell Gallery può essere bloccato da un firewall oppure è necessario un programma di installazione offline. È consigliabile installare Azure PowerShell con PowerShellGet. Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-az-ps.md).

## <a name="requirements"></a>Requisiti

Il programma di installazione MSI in Windows è progettato per installare solo Azure PowerShell per PowerShell 5.1. Per l'installazione su piattaforme diverse da Windows o in versioni successive di PowerShell, [eseguire l'installazione con PowerShellGet](install-az-ps.md). Per controllare la versione di PowerShell, eseguire il comando:

```powershell-interactive
$PSVersionTable.PSVersion
```

Per usare Azure PowerShell in PowerShell 5.1, è necessario:

1. Se necessario, eseguire l'aggiornamento a [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell). Se si usa Windows 10, PowerShell 5.1 è già installato.
2. Installare [.NET Framework 4.7.2 o versioni successive](/dotnet/framework/install).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI

Il pacchetto MSI per Azure PowerShell è disponibile in [GitHub](https://github.com/Azure/azure-powershell/releases):

1. Passare a https://github.com/Azure/azure-powershell/releases.
2. Cercare il modulo della raccolta più recente per Azure PowerShell. Tali versioni sono elencate in ordine cronologico e sono in genere solo una versione di rilascio senza nome, ad esempio "4.7.0".
3. Scorrere fino alla fine delle note sulla patch e fare clic sulla freccia accanto ad "Asset" per visualizzare le opzioni del pacchetto MSI.
4. Fare clic sul pacchetto MSI Az-Cmdlets scelto per avviare il download.

Se le versioni precedenti dei moduli di Azure PowerShell sono state installate con il pacchetto MSI, il programma di installazione le rimuove automaticamente. Il pacchetto MSI installa i moduli in `${env:ProgramFiles}\WindowsPowerShell\Modules`.

Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> Se il caricamento automatico dei moduli è stato disabilitato, è necessario importare manualmente il modulo con `Import-Module Az`. A causa del modo in cui è strutturato il modulo, l'operazione può richiedere fino a un minuto.

È necessario ripetere questo passaggio per ogni nuova sessione di PowerShell avviata. Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).

## <a name="provide-feedback"></a>Fornire commenti e suggerimenti

Se si trova un bug in Azure PowerShell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues). Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md). Se si ha familiarità con Azure PowerShell ed è necessario eseguire la migrazione da AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).
