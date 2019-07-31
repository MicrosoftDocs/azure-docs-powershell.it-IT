---
title: Eseguire i cmdlet in parallelo tramite processi di PowerShell
description: Come eseguire i cmdlet in parallelo tramite il parametro -AsJob.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 825a07e01194a07b747712a62384c7f162e63d7d
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657876"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="2c16f-103">Esecuzione in parallelo dei cmdlet tramite processi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="2c16f-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="2c16f-104">PowerShell supporta l'azione asincrona con i [processi di PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="2c16f-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="2c16f-105">Azure PowerShell dipende in modo significativo dall'effettuazione e dall'attesa di chiamate di rete in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c16f-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="2c16f-106">Potrebbe essere spesso necessario effettuare chiamate non bloccanti.</span><span class="sxs-lookup"><span data-stu-id="2c16f-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="2c16f-107">Per soddisfare questa esigenza, Azure PowerShell offre supporto di qualità elevata per i [processi di PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="2c16f-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="2c16f-108">Persistenza del contesto e processi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="2c16f-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="2c16f-109">Dato che i processi di PowerShell vengono eseguiti come processi separati, la connessione ad Azure deve essere condivisa con tali processi.</span><span class="sxs-lookup"><span data-stu-id="2c16f-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="2c16f-110">Dopo aver eseguito l'accesso all'account Azure con `Connect-AzAccount`, passare il contesto a un processo.</span><span class="sxs-lookup"><span data-stu-id="2c16f-110">After signing in to your Azure account with `Connect-AzAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList (Get-AzContext),$creds
```

<span data-ttu-id="2c16f-111">Se tuttavia si ha scelto di salvare automaticamente il contesto con `Enable-AzContextAutosave`, il contesto viene condiviso automaticamente con qualsiasi processo creato.</span><span class="sxs-lookup"><span data-stu-id="2c16f-111">However, if you have chosen to have your context automatically saved with `Enable-AzContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -ArgumentList $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="2c16f-112">Processi automatici con `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="2c16f-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="2c16f-113">Per comodità, Azure PowerShell fornisce anche un'opzione `-AsJob` per alcuni cmdlet a esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="2c16f-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="2c16f-114">L'opzione `-AsJob` semplifica la creazione di processi di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2c16f-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="2c16f-115">È possibile esaminare il processo e il rispettivo stato in qualsiasi momento con `Get-Job` e `Get-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="2c16f-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzVM`.</span></span>

```azurepowershell-interactive
Get-Job $job
Get-AzVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzVM' AzureLongRunningJob`1 Running True        localhost New-AzVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="2c16f-116">Al termine del processo, recuperarne il risultato con `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="2c16f-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="2c16f-117">`Receive-Job` restituisce il risultato dal cmdlet come se il flag `-AsJob` non fosse presente.</span><span class="sxs-lookup"><span data-stu-id="2c16f-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="2c16f-118">Ad esempio, il risultato `Receive-Job` di `Do-Action -AsJob` è dello stesso tipo del risultato di `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="2c16f-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a><span data-ttu-id="2c16f-119">Scenari di esempio</span><span class="sxs-lookup"><span data-stu-id="2c16f-119">Example Scenarios</span></span>

<span data-ttu-id="2c16f-120">Creare più VM contemporaneamente:</span><span class="sxs-lookup"><span data-stu-id="2c16f-120">Create several VMs at once:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzVM
```

<span data-ttu-id="2c16f-121">In questo esempio il cmdlet `Wait-Job` provoca la sospensione dello script durante l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="2c16f-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="2c16f-122">L'esecuzione dello script continua dopo il completamento di tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="2c16f-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="2c16f-123">Vengono eseguiti in parallelo diversi processi, quindi lo script attende il completamento prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="2c16f-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```
