---
title: Eseguire i cmdlet di Azure PowerShell nei processi di PowerShell
description: Informazioni su come eseguire i cmdlet di Azure PowerShell in parallelo o come attività in background con -AsJob e Start-Job.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b76e310e1677e539927ebc4746df67c1d1accc16
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407018"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a><span data-ttu-id="7a462-103">Eseguire i cmdlet di Azure PowerShell nei processi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="7a462-103">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>

<span data-ttu-id="7a462-104">Il funzionamento di Azure PowerShell dipende dalla connessione a un cloud di Azure e dall'attesa di risposte, per cui molti cmdlet bloccano la sessione di PowerShell finché non ottengono una risposta dal cloud.</span><span class="sxs-lookup"><span data-stu-id="7a462-104">Azure PowerShell depends on connecting to an Azure cloud and waiting for responses, so most of these cmdlets block your PowerShell session until they get a response from the cloud.</span></span>
<span data-ttu-id="7a462-105">I processi di PowerShell consentono di eseguire i cmdlet in background o di svolgere più attività contemporaneamente all'interno di una singola sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7a462-105">Powershell Jobs let you run cmdlets in the background or do multiple tasks on Azure at once, from inside a single PowerShell session.</span></span>

<span data-ttu-id="7a462-106">Questo articolo include una breve panoramica sull'uso dei cmdlet di Azure PowerShell come processi di PowerShell e su come controllarne il completamento.</span><span class="sxs-lookup"><span data-stu-id="7a462-106">This article is a brief overview of how to run Azure PowerShell cmdlets as PowerShell Jobs and check for completion.</span></span> <span data-ttu-id="7a462-107">L'esecuzione di comandi in Azure PowerShell richiede l'uso di contesti di Azure PowerShell, che vengono descritti in dettaglio nell'articolo [Contesti e credenziali di accesso di Azure](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="7a462-107">Running commands in Azure PowerShell requires the use of Azure PowerShell contexts, which are covered in detail in [Azure contexts and sign-in credentials](context-persistence.md).</span></span>
<span data-ttu-id="7a462-108">Per altre informazioni sui processi di PowerShell, vedere [Informazioni sui processi di PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="7a462-108">To learn more about PowerShell Jobs, see [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="azure-contexts-with-powershell-jobs"></a><span data-ttu-id="7a462-109">Contesti di Azure con processi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="7a462-109">Azure contexts with PowerShell jobs</span></span>

<span data-ttu-id="7a462-110">I processi di PowerShell vengono eseguiti come processi separati, senza una sessione di PowerShell collegata, quindi è necessario condividere con essi le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="7a462-110">PowerShell Jobs are run as separate processes without an attached PowerShell session, so your Azure credentials must be shared with them.</span></span> <span data-ttu-id="7a462-111">Le credenziali vengono passate come oggetti contesto di Azure, usando uno di questi metodi:</span><span class="sxs-lookup"><span data-stu-id="7a462-111">Credentials are passed as Azure context objects, using one of these methods:</span></span>

* <span data-ttu-id="7a462-112">Persistenza automatica del contesto.</span><span class="sxs-lookup"><span data-stu-id="7a462-112">Automatic context persistence.</span></span> <span data-ttu-id="7a462-113">La persistenza del contesto è abilitata per impostazione predefinita e mantiene le informazioni di accesso tra più sessioni.</span><span class="sxs-lookup"><span data-stu-id="7a462-113">Context persistence is enabled by default and preserves your sign-in information across multiple sessions.</span></span> <span data-ttu-id="7a462-114">Con la persistenza del contesto abilitata, il contesto di Azure corrente viene passato al nuovo processo:</span><span class="sxs-lookup"><span data-stu-id="7a462-114">With context persistence enabled, the current Azure context is passed to the new process:</span></span>

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* <span data-ttu-id="7a462-115">Usare il parametro `-AzContext` con qualsiasi cmdlet di Azure PowerShell per specificare un oggetto contesto di Azure:</span><span class="sxs-lookup"><span data-stu-id="7a462-115">Use the `-AzContext` parameter with any Azure PowerShell cmdlets to provide an Azure context object:</span></span>

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  <span data-ttu-id="7a462-116">Se la persistenza del contesto è disabilitata, è necessario l'argomento `-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="7a462-116">If context persistence is disabled, the `-AzContext` argument is required.</span></span>

* <span data-ttu-id="7a462-117">Usare l'opzione `-AsJob` disponibile in alcuni cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7a462-117">Use the `-AsJob` switch provided by some Azure PowerShell cmdlets.</span></span> <span data-ttu-id="7a462-118">Questa opzione avvia automaticamente il cmdlet come processo di PowerShell, usando il contesto di Azure attivo:</span><span class="sxs-lookup"><span data-stu-id="7a462-118">This switch automatically starts the cmdlet as a PowerShell Job, using the currently active Azure context:</span></span>

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  <span data-ttu-id="7a462-119">Per verificare se un cmdlet supporta `-AsJob`, vedere la relativa documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="7a462-119">To see if a cmdlet supports `-AsJob`, check its reference documentation.</span></span> <span data-ttu-id="7a462-120">L'opzione `-AsJob` non richiede che il salvataggio automatico dei contesti sia abilitato.</span><span class="sxs-lookup"><span data-stu-id="7a462-120">The `-AsJob` switch doesn't require context autosave to be enabled.</span></span>

<span data-ttu-id="7a462-121">È possibile controllare lo stato di un processo in esecuzione con il cmdlet [Get-Job](/powershell/module/microsoft.powershell.core/get-job).</span><span class="sxs-lookup"><span data-stu-id="7a462-121">You can check the status of a running job with the [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet.</span></span> <span data-ttu-id="7a462-122">Per ottenere l'output immediato di un processo, usare il cmdlet [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).</span><span class="sxs-lookup"><span data-stu-id="7a462-122">To get the output from a job so far, use the [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet.</span></span>

<span data-ttu-id="7a462-123">Per controllare lo stato di avanzamento di un'operazione in remoto in Azure, usare i cmdlet `Get-` associati al tipo di risorsa modificato dal processo:</span><span class="sxs-lookup"><span data-stu-id="7a462-123">To check an operation's progress remotely on Azure, use the `Get-` cmdlets associated with the type of resource being modified by the job:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a><span data-ttu-id="7a462-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7a462-124">See Also</span></span>

* [<span data-ttu-id="7a462-125">Contesti di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7a462-125">Azure PowerShell contexts</span></span>](context-persistence.md)
* [<span data-ttu-id="7a462-126">Informazioni sui processi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="7a462-126">About PowerShell Jobs</span></span>](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [<span data-ttu-id="7a462-127">Informazioni di riferimento su Get-Job</span><span class="sxs-lookup"><span data-stu-id="7a462-127">Get-Job reference</span></span>](/powershell/module/microsoft.powershell.core/get-job)
* [<span data-ttu-id="7a462-128">Informazioni di riferimento su Receive-Job</span><span class="sxs-lookup"><span data-stu-id="7a462-128">Receive-Job reference</span></span>](/powershell/module/microsoft.powershell.core/receive-job)
