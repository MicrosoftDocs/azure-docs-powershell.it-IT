---
title: Output delle query dei cmdlet di Azure PowerShell
description: Come eseguire una query delle risorse in Azure e formattare i risultati.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.openlocfilehash: 9141f5640467722608cb7748f425ce3942668fb8
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "81445459"
---
# <a name="query-output-of-azure-powershell"></a><span data-ttu-id="a2f78-103">Output delle query di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a2f78-103">Query output of Azure PowerShell</span></span> 

<span data-ttu-id="a2f78-104">I risultati di ogni cmdlet di PowerShell di Azure sono un oggetto di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a2f78-104">The results of each Azure PowerShell cmdlet are an Azure PowerShell object.</span></span> <span data-ttu-id="a2f78-105">Anche i cmdlet che non sono esplicitamente operazioni `Get-` potrebbero restituire un valore che può essere controllato per fornire informazioni su una risorsa che è stata creata o modificata.</span><span class="sxs-lookup"><span data-stu-id="a2f78-105">Even cmdlets that aren't explicitly `Get-` operations might return a value that can be inspected, to give information about a resource that was created or modified.</span></span> <span data-ttu-id="a2f78-106">Mentre la maggior parte dei cmdlet restituisce un singolo oggetto, alcuni restituiscono una matrice da scorrere.</span><span class="sxs-lookup"><span data-stu-id="a2f78-106">While most cmdlets return a single object, some return an array that should be iterated through.</span></span>

<span data-ttu-id="a2f78-107">In quasi tutti i casi, è possibile eseguire una query sull'output di Azure PowerShell con il cmdlet [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), spesso abbreviato in `select`.</span><span class="sxs-lookup"><span data-stu-id="a2f78-107">In almost all cases, you query output from Azure PowerShell with the [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet, often abbreviated to `select`.</span></span> <span data-ttu-id="a2f78-108">L'output può essere filtrato con [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) o con il relativo alias `where`.</span><span class="sxs-lookup"><span data-stu-id="a2f78-108">Output can be filtered with [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), or its alias `where`.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="a2f78-109">Selezionare proprietà semplici</span><span class="sxs-lookup"><span data-stu-id="a2f78-109">Select simple properties</span></span>

<span data-ttu-id="a2f78-110">Nel formato di tabella predefinito i cmdlet di Azure PowerShell non visualizzano tutte le relative proprietà disponibili.</span><span class="sxs-lookup"><span data-stu-id="a2f78-110">In the default table format, Azure PowerShell cmdlets don't display all of their available properties.</span></span> <span data-ttu-id="a2f78-111">È possibile ottenere tutte le proprietà usando il cmdlet [Format-List](/powershell/module/microsoft.powershell.utility/format-list) o inviando l'output tramite pipe a `Select-Object *`:</span><span class="sxs-lookup"><span data-stu-id="a2f78-111">You can get the full properties by using the [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet, or by piping output to `Select-Object *`:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

<span data-ttu-id="a2f78-112">Dopo aver individuato i nomi delle proprietà a cui si è interessati, è possibile usare quei nomi di proprietà con `Select-Object` per richiamarli direttamente:</span><span class="sxs-lookup"><span data-stu-id="a2f78-112">Once you know the names of the properties that you're interested in, you can use those property names with `Select-Object` to get them directly:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

<span data-ttu-id="a2f78-113">L'output derivante dall'uso di `Select-Object` viene sempre formattato per visualizzare le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="a2f78-113">Output from using `Select-Object` is always formatted to display the requested information.</span></span> <span data-ttu-id="a2f78-114">Per altre informazioni sull'uso della formattazione come parte della query su risultati dei cmdlet, vedere [Formattare l'output dei cmdlet di Azure PowerShell](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="a2f78-114">To learn about using formatting as part of querying cmdlet results, see [Format Azure PowerShell cmdlet output](formatting-output.md).</span></span>

## <a name="select-nested-properties"></a><span data-ttu-id="a2f78-115">Selezionare proprietà annidate</span><span class="sxs-lookup"><span data-stu-id="a2f78-115">Select nested properties</span></span>

<span data-ttu-id="a2f78-116">Alcune proprietà nell'output dei cmdlet di Azure PowerShell usano oggetti annidati come ad esempio la proprietà `StorageProfile` dell'output di `Get-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="a2f78-116">Some properties in Azure PowerShell cmdlet output use nested objects, like the `StorageProfile` property of `Get-AzVM` output.</span></span> <span data-ttu-id="a2f78-117">Per ottenere un valore da una proprietà annidata, fornire un nome visualizzato e il percorso completo del valore che si vuole controllare come parte di un argomento dizionario a `Select-Object`:</span><span class="sxs-lookup"><span data-stu-id="a2f78-117">To get a value from a nested property, provide a display name and the full path to the value you want to inspect as part of a dictionary argument to `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

<span data-ttu-id="a2f78-118">Ogni argomento dizionario seleziona una proprietà dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a2f78-118">Each dictionary argument selects one property from the object.</span></span> <span data-ttu-id="a2f78-119">La proprietà da estrarre deve far parte di un'espressione.</span><span class="sxs-lookup"><span data-stu-id="a2f78-119">The property to extract must be part of an expression.</span></span>

## <a name="filter-results"></a><span data-ttu-id="a2f78-120">Filtrare i risultati</span><span class="sxs-lookup"><span data-stu-id="a2f78-120">Filter results</span></span> 

<span data-ttu-id="a2f78-121">Il cmdlet `Where-Object` consente di filtrare i risultati in base a qualsiasi valore della proprietà, comprese le proprietà annidate.</span><span class="sxs-lookup"><span data-stu-id="a2f78-121">The `Where-Object` cmdlet allows you to filter the result based on any property value, including nested properties.</span></span> <span data-ttu-id="a2f78-122">L'esempio seguente mostra come usare `Where-Object` per trovare le macchine virtuali Linux in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a2f78-122">The next example shows how to use `Where-Object` to find the Linux VMs in a resource group.</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

<span data-ttu-id="a2f78-123">È possibile inviare tramite pipe i risultati di `Select-Object` e `Where-Object` l'uno all'altro.</span><span class="sxs-lookup"><span data-stu-id="a2f78-123">You can pipe the results of `Select-Object` and `Where-Object` to each other.</span></span> <span data-ttu-id="a2f78-124">Ai fini delle prestazioni, è sempre consigliabile inserire l'operazione `Where-Object` prima di `Select-Object`:</span><span class="sxs-lookup"><span data-stu-id="a2f78-124">For performance purposes, it's always recommended to put the `Where-Object` operation before `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```