---
title: Installare Azure PowerShell con un file MSI
description: Come installare Azure PowerShell senza PowerShellGet usando un programma di installazione MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: d16aea3fa2059cd32f584134e2da43e01e3def31
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "72821470"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installare Azure PowerShell in Windows con un programma di installazione MSI

Questo articolo illustra come installare Azure PowerShell in Windows con un programma di installazione MSI. Il programma di installazione MSI viene fornito per gli ambienti in cui PowerShell Gallery può essere bloccato da un firewall oppure è necessario un programma di installazione offline. È consigliabile installare Azure PowerShell con PowerShellGet. Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-az-ps.md).

## <a name="requirements"></a>Requisiti

Il programma di installazione MSI per Azure PowerShell funziona __solo__ per PowerShell 5.1 in Windows. Per l'installazione su piattaforme non Windows o su versioni successive di PowerShell, [eseguire l'installazione con PowerShellGet](install-az-ps.md).
Per controllare la versione di PowerShell, eseguire il comando:

```powershell-interactive
$PSVersionTable.PSVersion
```

Per usare Azure PowerShell in PowerShell 5.1, è necessario:

1. Se necessario, eseguire l'aggiornamento a [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell). Se si usa Windows 10, PowerShell 5.1 è già installato.
2. Installare [.NET Framework 4.7.2 o versioni successive](/dotnet/framework/install).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI

Azure PowerShell può essere installato usando il file MSI disponibile su [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v2.8.0-October2019). Se le versioni precedenti dei moduli di Azure sono state installate come pacchetto MSI, il programma di installazione le rimuove automaticamente. Il pacchetto MSI installa i moduli in `${env:ProgramFiles}\WindowsPowerShell\Modules`.

Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
>
> Se il caricamento automatico dei moduli è stato disabilitato, è necessario importare manualmente il modulo con `Import-Module Az`. A causa del modo in cui è strutturato il modulo, l'operazione può richiedere fino a un minuto.

È necessario ripetere questo passaggio per ogni nuova sessione di PowerShell avviata. Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).

## <a name="provide-feedback"></a>Fornire commenti e suggerimenti

Se si trova un bug in Azure Powershell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues).
Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md).
Se si ha familiarità con Azure PowerShell ed è necessario eseguire la migrazione da AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).
