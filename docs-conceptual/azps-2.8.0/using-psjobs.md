---
title: Eseguire i cmdlet di Azure PowerShell nei processi di PowerShell
description: Informazioni su come eseguire i cmdlet di Azure PowerShell in parallelo o come attività in background con -AsJob e Start-Job.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5d9028c0a433149c8f6cc346651bb8bf875bb42a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241492"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a>Eseguire i cmdlet di Azure PowerShell nei processi di PowerShell

Il funzionamento di Azure PowerShell dipende dalla connessione a un cloud di Azure e dall'attesa di risposte, per cui molti cmdlet bloccano la sessione di PowerShell finché non ottengono una risposta dal cloud.
I processi di PowerShell consentono di eseguire i cmdlet in background o di svolgere più attività contemporaneamente all'interno di una singola sessione di PowerShell.

Questo articolo include una breve panoramica sull'uso dei cmdlet di Azure PowerShell come processi di PowerShell e su come controllarne il completamento. L'esecuzione di comandi in Azure PowerShell richiede l'uso di contesti di Azure PowerShell, che vengono descritti in dettaglio nell'articolo [Contesti e credenziali di accesso di Azure](context-persistence.md).
Per altre informazioni sui processi di PowerShell, vedere [Informazioni sui processi di PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="azure-contexts-with-powershell-jobs"></a>Contesti di Azure con processi di PowerShell

I processi di PowerShell vengono eseguiti come processi separati, senza una sessione di PowerShell collegata, quindi è necessario condividere con essi le credenziali di Azure. Le credenziali vengono passate come oggetti contesto di Azure, usando uno di questi metodi:

* Persistenza automatica del contesto. La persistenza del contesto è abilitata per impostazione predefinita e mantiene le informazioni di accesso tra più sessioni. Con la persistenza del contesto abilitata, il contesto di Azure corrente viene passato al nuovo processo:

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* Usare il parametro `-AzContext` con qualsiasi cmdlet di Azure PowerShell per specificare un oggetto contesto di Azure:

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  Se la persistenza del contesto è disabilitata, è necessario l'argomento `-AzContext`.

* Usare l'opzione `-AsJob` disponibile in alcuni cmdlet di Azure PowerShell. Questa opzione avvia automaticamente il cmdlet come processo di PowerShell, usando il contesto di Azure attivo:

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  Per verificare se un cmdlet supporta `-AsJob`, vedere la relativa documentazione di riferimento. L'opzione `-AsJob` non richiede che il salvataggio automatico dei contesti sia abilitato.

È possibile controllare lo stato di un processo in esecuzione con il cmdlet [Get-Job](/powershell/module/microsoft.powershell.core/get-job). Per ottenere l'output immediato di un processo, usare il cmdlet [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).

Per controllare lo stato di avanzamento di un'operazione in remoto in Azure, usare i cmdlet `Get-` associati al tipo di risorsa modificato dal processo:

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a>Vedere anche

* [Contesti di Azure PowerShell](context-persistence.md)
* [Informazioni sui processi di PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [Informazioni di riferimento su Get-Job](/powershell/module/microsoft.powershell.core/get-job)
* [Informazioni di riferimento su Receive-Job](/powershell/module/microsoft.powershell.core/receive-job)
