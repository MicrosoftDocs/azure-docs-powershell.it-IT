---
title: Formattare l'output dei cmdlet di Azure PowerShell
description: Come formattare l'output dei cmdlet per Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/07/2018
ms.openlocfilehash: 833c82903305f99be5ad43f707e22644bb568abe
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406388"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="a2327-103">Formattare l'output dei cmdlet di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a2327-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="a2327-104">Per impostazione predefinita, ogni cmdlet di Azure PowerShell genera un output con formattazione predefinita, per semplificarne la lettura.</span><span class="sxs-lookup"><span data-stu-id="a2327-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="a2327-105">PowerShell offre inoltre la flessibilità necessaria per modificare l'output o convertire l'output del cmdlet in un formato diverso con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2327-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="a2327-106">Formattazione</span><span class="sxs-lookup"><span data-stu-id="a2327-106">Formatting</span></span>      | <span data-ttu-id="a2327-107">Conversione</span><span class="sxs-lookup"><span data-stu-id="a2327-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="a2327-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="a2327-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="a2327-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="a2327-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="a2327-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="a2327-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="a2327-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="a2327-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="a2327-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="a2327-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="a2327-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="a2327-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="a2327-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="a2327-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="a2327-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="a2327-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="a2327-116">Esempi di formattazione</span><span class="sxs-lookup"><span data-stu-id="a2327-116">Format examples</span></span>

<span data-ttu-id="a2327-117">L'esempio seguente mostra un elenco di macchine virtuali di Azure nella sottoscrizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a2327-117">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="a2327-118">Per impostazione predefinita, il comando `Get-AzureRmVM` genera l'output in formato tabella.</span><span class="sxs-lookup"><span data-stu-id="a2327-118">The `Get-AzureRmVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="a2327-119">Se si desidera limitare le colonne restituite è possibile usare il cmdlet `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="a2327-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="a2327-120">Nell'esempio seguente si ottiene lo stesso elenco di macchine virtuali, ma l'output è limitato al solo nome della macchina virtuale, al gruppo di risorse e al percorso della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2327-120">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="a2327-121">Il parametro `-Autosize` ridimensiona le colonne in base alla dimensione dei dati.</span><span class="sxs-lookup"><span data-stu-id="a2327-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="a2327-122">L'output può anche essere formattato in un elenco.</span><span class="sxs-lookup"><span data-stu-id="a2327-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="a2327-123">L'esempio seguente illustra questa opzione, con l'uso del cmdlet `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="a2327-123">The following example shows this using the`Format-List` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a><span data-ttu-id="a2327-124">Convertire in altri tipi di dati</span><span class="sxs-lookup"><span data-stu-id="a2327-124">Convert to other data types</span></span>

<span data-ttu-id="a2327-125">PowerShell consente anche di convertire l'output del comando in più formati di dati.</span><span class="sxs-lookup"><span data-stu-id="a2327-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="a2327-126">Nell'esempio seguente viene usato il cmdlet `Select-Object` per recuperare gli attributi delle macchine virtuali nella sottoscrizione e convertire l'output in formato CSV per importarlo facilmente in un database o un foglio di calcolo.</span><span class="sxs-lookup"><span data-stu-id="a2327-126">In the following example the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="a2327-127">L'output può anche essere convertito in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="a2327-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="a2327-128">Nell'esempio seguente viene creato lo stesso elenco di macchine virtuali, ma il formato di output è modificato in JSON.</span><span class="sxs-lookup"><span data-stu-id="a2327-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
