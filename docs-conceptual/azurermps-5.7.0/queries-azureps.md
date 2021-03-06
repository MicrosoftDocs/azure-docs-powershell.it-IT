---
title: Output delle query dei cmdlet di Azure PowerShell
description: Come eseguire una query delle risorse in Azure e formattare i risultati.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/08/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 664829721843020745cf24a913e1d09a4e68a3da
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243685"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a>Output delle query dei cmdlet di Azure PowerShell

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Usando i cmdlet incorporati è possibile eseguire una query in PowerShell. In PowerShell, i nomi dei cmdlet assumono la forma di **_verbo-sostantivo_**. I cmdlet che usano il verbo **_Get_**(ottenere) sono cmdlet di query. I sostantivi dei cmdlet sono i tipi di risorse di Azure che vengono ignorati per i verbi di cmdlet.

## <a name="select-simple-properties"></a>Selezionare proprietà semplici

Azure PowerShell include la formattazione predefinita definita per ciascun cmdlet. Le proprietà più comuni per ogni tipo di risorsa vengono visualizzate automaticamente in formato di tabella o elenco. Per altre informazioni sulla formattazione dell'output, vedere [Formattazione dei risultati delle query](formatting-output.md).

Usare il cmdlet `Get-AzureRmVM` per eseguire la query di un elenco di macchine virtuali nel proprio account.

```azurepowershell-interactive
Get-AzureRmVM
```

L'output predefinito viene automaticamente formattato come tabella.

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Il cmdlet `Select-Object` può essere usato per selezionare le proprietà specifiche di interesse.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a>Selezionare proprietà annidate complesse

Se la proprietà che si desidera selezionare è annidata nell'output JSON sarà necessario fornire il percorso completo di tale proprietà annidata. L'esempio seguente illustra come selezionare il nome della macchina virtuale e il tipo di sistema operativo dal cmdlet `Get-AzureRmVM`.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a>Filtrare i risultati con il cmdlet Where-Object

Il cmdlet `Where-Object` consente di filtrare i risultati in base a qualsiasi valore della proprietà. Nell'esempio seguente, il filtro consente di selezionare solo le macchine virtuali con il testo "RGD" nel nome.

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

Nell'esempio successivo, i risultati riporteranno le macchine virtuali con vmSize "Standard_DS1_V2".

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
