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
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182112"
---
# <a name="query-output-of-azure-powershell"></a>Output delle query di Azure PowerShell 

I risultati di ogni cmdlet di PowerShell di Azure sono un oggetto di Azure PowerShell. Anche i cmdlet che non sono esplicitamente operazioni `Get-` potrebbero restituire un valore che può essere controllato per fornire informazioni su una risorsa che è stata creata o modificata. Mentre la maggior parte dei cmdlet restituisce un singolo oggetto, alcuni restituiscono una matrice da scorrere.

In quasi tutti i casi, è possibile eseguire una query sull'output di Azure PowerShell con il cmdlet [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), spesso abbreviato in `select`. L'output può essere filtrato con [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) o con il relativo alias `where`.

## <a name="select-simple-properties"></a>Selezionare proprietà semplici

Nel formato di tabella predefinito i cmdlet di Azure PowerShell non visualizzano tutte le relative proprietà disponibili. È possibile ottenere tutte le proprietà usando il cmdlet [Format-List](/powershell/module/microsoft.powershell.utility/format-list) o inviando l'output tramite pipe a `Select-Object *`:

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

Dopo aver individuato i nomi delle proprietà a cui si è interessati, è possibile usare quei nomi di proprietà con `Select-Object` per richiamarli direttamente:

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

L'output derivante dall'uso di `Select-Object` viene sempre formattato per visualizzare le informazioni richieste. Per altre informazioni sull'uso della formattazione come parte della query su risultati dei cmdlet, vedere [Formattare l'output dei cmdlet di Azure PowerShell](formatting-output.md).

## <a name="select-nested-properties"></a>Selezionare proprietà annidate

Alcune proprietà nell'output dei cmdlet di Azure PowerShell usano oggetti annidati come ad esempio la proprietà `StorageProfile` dell'output di `Get-AzVM`. Per ottenere un valore da una proprietà annidata, fornire un nome visualizzato e il percorso completo del valore che si vuole controllare come parte di un argomento dizionario a `Select-Object`:

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

Ogni argomento dizionario seleziona una proprietà dall'oggetto. La proprietà da estrarre deve far parte di un'espressione.

## <a name="filter-results"></a>Filtrare i risultati 

Il cmdlet `Where-Object` consente di filtrare i risultati in base a qualsiasi valore della proprietà, comprese le proprietà annidate. L'esempio seguente mostra come usare `Where-Object` per trovare le macchine virtuali Linux in un gruppo di risorse.

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

È possibile inviare tramite pipe i risultati di `Select-Object` e `Where-Object` l'uno all'altro. Ai fini delle prestazioni, è sempre consigliabile inserire l'operazione `Where-Object` prima di `Select-Object`:

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