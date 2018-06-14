---
title: Query per le risorse di Azure e formattazione dei risultati | Microsoft Docs
description: Come eseguire una query delle risorse in Azure e formattare i risultati.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 1584c8166078b7d7d24ce8748307fde0f565b662
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853339"
---
# <a name="querying-for-azure-resources"></a><span data-ttu-id="4eb18-103">Query per le risorse di Azure</span><span class="sxs-lookup"><span data-stu-id="4eb18-103">Querying for Azure resources</span></span>

<span data-ttu-id="4eb18-104">Usando i cmdlet incorporati è possibile eseguire una query in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4eb18-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="4eb18-105">In PowerShell, i nomi dei cmdlet assumono la forma di **_verbo-sostantivo_**.</span><span class="sxs-lookup"><span data-stu-id="4eb18-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="4eb18-106">I cmdlet che usano il verbo **_Get_**(ottenere) sono cmdlet di query.</span><span class="sxs-lookup"><span data-stu-id="4eb18-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="4eb18-107">I sostantivi dei cmdlet sono i tipi di risorse di Azure che vengono ignorati per i verbi di cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eb18-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>


## <a name="selecting-simple-properties"></a><span data-ttu-id="4eb18-108">Selezione di proprietà semplici</span><span class="sxs-lookup"><span data-stu-id="4eb18-108">Selecting simple properties</span></span>

<span data-ttu-id="4eb18-109">Azure PowerShell include la formattazione predefinita definita per ciascun cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eb18-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="4eb18-110">Le proprietà più comuni per ogni tipo di risorsa vengono visualizzate automaticamente in formato di tabella o elenco.</span><span class="sxs-lookup"><span data-stu-id="4eb18-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="4eb18-111">Per altre informazioni sulla formattazione dell'output, vedere [Formattazione dei risultati delle query](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="4eb18-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="4eb18-112">Usare il cmdlet `Get-AzureRmVM` per eseguire la query di un elenco di macchine virtuali nel proprio account.</span><span class="sxs-lookup"><span data-stu-id="4eb18-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```powershell
Get-AzureRmVM
```

<span data-ttu-id="4eb18-113">L'output predefinito viene automaticamente formattato come tabella.</span><span class="sxs-lookup"><span data-stu-id="4eb18-113">The default output is automatically formatted as a table.</span></span>

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="4eb18-114">Il cmdlet `Select-Object` può essere usato per selezionare le proprietà specifiche di interesse.</span><span class="sxs-lookup"><span data-stu-id="4eb18-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```powershell
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="4eb18-115">Selezione di proprietà nidificate complesse</span><span class="sxs-lookup"><span data-stu-id="4eb18-115">Selecting complex nested properties</span></span>

<span data-ttu-id="4eb18-116">Se la proprietà che si desidera selezionare è annidata nell'output JSON sarà necessario fornire il percorso completo di tale proprietà annidata.</span><span class="sxs-lookup"><span data-stu-id="4eb18-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="4eb18-117">L'esempio seguente illustra come selezionare il nome della macchina virtuale e il tipo di sistema operativo dal cmdlet `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="4eb18-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a><span data-ttu-id="4eb18-118">Filtrare i risultati usando il cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="4eb18-118">Filter result using the Where-Object cmdlet</span></span>

<span data-ttu-id="4eb18-119">Il cmdlet `Where-Object` consente di filtrare i risultati in base a qualsiasi valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="4eb18-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="4eb18-120">Nell'esempio seguente, il filtro consente di selezionare solo le macchine virtuali con il testo "RGD" nel nome.</span><span class="sxs-lookup"><span data-stu-id="4eb18-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```powershell
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="4eb18-121">Nell'esempio successivo, i risultati riporteranno le macchine virtuali con vmSize "Standard_DS1_V2".</span><span class="sxs-lookup"><span data-stu-id="4eb18-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```powershell
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
