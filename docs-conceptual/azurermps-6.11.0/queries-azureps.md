---
title: Output delle query dei cmdlet di Azure PowerShell
description: Come eseguire una query delle risorse in Azure e formattare i risultati.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 6bd1bea43303e9f5a2b46d63a3ac51b4c4031b9f
ms.sourcegitcommit: 1f699b72bf544d92459da9d888cc0091f9415b65
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2018
ms.locfileid: "50971840"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a><span data-ttu-id="ddfec-103">Output delle query dei cmdlet di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ddfec-103">Query output of Azure PowerShell cmdlets</span></span>

<span data-ttu-id="ddfec-104">Usando i cmdlet incorporati è possibile eseguire una query in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ddfec-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="ddfec-105">In PowerShell, i nomi dei cmdlet assumono la forma di **_verbo-sostantivo_**.</span><span class="sxs-lookup"><span data-stu-id="ddfec-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="ddfec-106">I cmdlet che usano il verbo **_Get_**(ottenere) sono cmdlet di query.</span><span class="sxs-lookup"><span data-stu-id="ddfec-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="ddfec-107">I sostantivi dei cmdlet sono i tipi di risorse di Azure che vengono ignorati per i verbi di cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddfec-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="ddfec-108">Selezionare proprietà semplici</span><span class="sxs-lookup"><span data-stu-id="ddfec-108">Select simple properties</span></span>

<span data-ttu-id="ddfec-109">Azure PowerShell include la formattazione predefinita definita per ciascun cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddfec-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="ddfec-110">Le proprietà più comuni per ogni tipo di risorsa vengono visualizzate automaticamente in formato di tabella o elenco.</span><span class="sxs-lookup"><span data-stu-id="ddfec-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="ddfec-111">Per altre informazioni sulla formattazione dell'output, vedere [Formattazione dei risultati delle query](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="ddfec-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="ddfec-112">Usare il cmdlet `Get-AzureRmVM` per eseguire la query di un elenco di macchine virtuali nel proprio account.</span><span class="sxs-lookup"><span data-stu-id="ddfec-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="ddfec-113">L'output predefinito viene automaticamente formattato come tabella.</span><span class="sxs-lookup"><span data-stu-id="ddfec-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="ddfec-114">Il cmdlet `Select-Object` può essere usato per selezionare le proprietà specifiche di interesse.</span><span class="sxs-lookup"><span data-stu-id="ddfec-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="ddfec-115">Selezionare proprietà annidate complesse</span><span class="sxs-lookup"><span data-stu-id="ddfec-115">Select complex nested properties</span></span>

<span data-ttu-id="ddfec-116">Se la proprietà desiderata è annidata nell'output JSON, è necessario specificare il percorso completo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ddfec-116">If the property you want is nested in the JSON output, you need to supply the full path to the property.</span></span> <span data-ttu-id="ddfec-117">L'esempio seguente illustra come selezionare il nome della macchina virtuale e il tipo di sistema operativo dal cmdlet `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="ddfec-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a><span data-ttu-id="ddfec-118">Filtrare i risultati con il cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="ddfec-118">Filter results with the Where-Object cmdlet</span></span>

<span data-ttu-id="ddfec-119">Il cmdlet `Where-Object` consente di filtrare i risultati in base a qualsiasi valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ddfec-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="ddfec-120">Nell'esempio seguente, il filtro consente di selezionare solo le macchine virtuali con il testo "RGD" nel nome.</span><span class="sxs-lookup"><span data-stu-id="ddfec-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="ddfec-121">Nell'esempio successivo, i risultati riporteranno le macchine virtuali con vmSize "Standard_DS1_V2".</span><span class="sxs-lookup"><span data-stu-id="ddfec-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```