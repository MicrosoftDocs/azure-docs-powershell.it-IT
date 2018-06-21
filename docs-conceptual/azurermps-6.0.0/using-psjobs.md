---
title: Esecuzione in parallelo dei cmdlet tramite processi di PowerShell
description: Come eseguire i cmdlet in parallelo tramite il parametro -AsJob.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: dfc1efa752c9c9fa42ad5904adacd83c2dc333b8
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
ms.locfileid: "33911936"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="afa73-103">Esecuzione in parallelo dei cmdlet tramite processi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="afa73-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="afa73-104">PowerShell supporta l'azione asincrona con i [processi di PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="afa73-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="afa73-105">Azure PowerShell dipende in modo significativo dall'effettuazione e dall'attesa di chiamate di rete in Azure.</span><span class="sxs-lookup"><span data-stu-id="afa73-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="afa73-106">È possibile che gli sviluppatori provino spesso a effettuare più chiamate non bloccanti ad Azure in uno script oppure che vogliano creare risorse di Azure in REPL senza bloccare la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="afa73-106">As a developer, you may often find yourself looking to make multiple non-blocking calls to Azure in a script, or you may find that you want to create Azure resources in the REPL without blocking the current session.</span></span> <span data-ttu-id="afa73-107">Per soddisfare queste esigenze, Azure PowerShell offre supporto di qualità elevata per [processi di PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="afa73-107">To address these needs, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="afa73-108">Persistenza del contesto e processi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="afa73-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="afa73-109">I processi di PowerShell vengono eseguiti in processi separati. È quindi necessario che le informazioni sulla connessione di Azure siano condivise correttamente con i processi creati.</span><span class="sxs-lookup"><span data-stu-id="afa73-109">PSJobs are run in separate processes, which means that information about your Azure connection must be properly shared with the jobs you create.</span></span> <span data-ttu-id="afa73-110">Al momento della connessione dell'account Azure alla sessione di PowerShell con `Connect-AzureRmAccount`, è possibile passare il contesto a un processo.</span><span class="sxs-lookup"><span data-stu-id="afa73-110">Upon connecting your Azure account to your PowerShell session with `Connect-AzureRmAccount`, you can pass the context to a job.</span></span>

```powershell
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="afa73-111">Se tuttavia si ha scelto di salvare automaticamente il contesto con `Enable-AzureRmContextAutosave`, il contesto viene condiviso automaticamente con qualsiasi processo creato.</span><span class="sxs-lookup"><span data-stu-id="afa73-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```powershell
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="afa73-112">Processi automatici con `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="afa73-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="afa73-113">Per comodità, Azure PowerShell fornisce anche un'opzione `-AsJob` per alcuni cmdlet a esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="afa73-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="afa73-114">L'opzione `-AsJob` semplifica la creazione di processi di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="afa73-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```powershell
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="afa73-115">È possibile esaminare il processo e il rispettivo stato in qualsiasi momento con `Get-Job` e `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="afa73-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

```powershell
Get-Job $job
Get-AzureRmVM MyVm
```

```Output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="afa73-116">Dopo il completamento, è possibile ottenere il risultato del processo con `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="afa73-116">Subsequently, upon completion, you can obtain the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="afa73-117">`Receive-Job` restituisce il risultato dal cmdlet come se il flag `-AsJob` non fosse presente.</span><span class="sxs-lookup"><span data-stu-id="afa73-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="afa73-118">Ad esempio, il risultato `Receive-Job` di `Do-Action -AsJob` è dello stesso tipo del risultato di `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="afa73-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```powershell
$vm = Receive-Job $job
$vm
```

```Output
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

## <a name="example-scenarios"></a><span data-ttu-id="afa73-119">Scenari di esempio</span><span class="sxs-lookup"><span data-stu-id="afa73-119">Example Scenarios</span></span>

<span data-ttu-id="afa73-120">Creare più VM contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="afa73-120">Create multiple VMs at once.</span></span>

```powershell
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

<span data-ttu-id="afa73-121">In questo esempio il cmdlet `Wait-Job` provoca la sospensione dello script durante l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="afa73-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="afa73-122">L'esecuzione dello script continua dopo il completamento di tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="afa73-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="afa73-123">Ciò permette di creare alcuni processi in esecuzione in parallelo e quindi di attendere il completamento prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="afa73-123">This allows you to create several jobs running in parallel then wait for completion before continuing.</span></span>

```Output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
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
