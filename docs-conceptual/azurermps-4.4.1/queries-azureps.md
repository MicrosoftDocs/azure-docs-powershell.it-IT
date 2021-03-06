---
title: Query per le risorse di Azure e formattazione dei risultati | Microsoft Docs
description: Come eseguire una query delle risorse in Azure e formattare i risultati.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7c8bac8430c4e1f1ad2067a68aa7768f4683d6b7
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243923"
---
# <a name="querying-for-azure-resources"></a>Query per le risorse di Azure

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Usando i cmdlet incorporati è possibile eseguire una query in PowerShell. In PowerShell, i nomi dei cmdlet assumono la forma di **_verbo-sostantivo_**. I cmdlet che usano il verbo **_Get_**(ottenere) sono cmdlet di query. I sostantivi dei cmdlet sono i tipi di risorse di Azure che vengono ignorati per i verbi di cmdlet.

## <a name="selecting-simple-properties"></a>Selezione di proprietà semplici

Azure PowerShell include la formattazione predefinita definita per ciascun cmdlet. Le proprietà più comuni per ogni tipo di risorsa vengono visualizzate automaticamente in formato di tabella o elenco. Per altre informazioni sulla formattazione dell'output, vedere [Formattazione dei risultati delle query](formatting-output.md).

Usare il cmdlet `Get-AzureRmVM` per eseguire la query di un elenco di macchine virtuali nel proprio account.

```powershell-interactive
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

```powershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a>Selezione di proprietà nidificate complesse

Se la proprietà che si desidera selezionare è annidata nell'output JSON sarà necessario fornire il percorso completo di tale proprietà annidata. L'esempio seguente illustra come selezionare il nome della macchina virtuale e il tipo di sistema operativo dal cmdlet `Get-AzureRmVM`.

```powershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a>Filtrare i risultati usando il cmdlet Where-Object

Il cmdlet `Where-Object` consente di filtrare i risultati in base a qualsiasi valore della proprietà. Nell'esempio seguente, il filtro consente di selezionare solo le macchine virtuali con il testo "RGD" nel nome.

```powershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

Nell'esempio successivo, i risultati riporteranno le macchine virtuali con vmSize "Standard_DS1_V2".

```powershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
