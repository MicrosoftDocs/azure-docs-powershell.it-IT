---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: 46a0ffcaece93328447405f78af2af0785b329c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863713"
---
# Get-AzVMSize

## Sinossi
Ottiene le dimensioni della macchina virtuale disponibili.

## SINTASSI

### ListVirtualMachineSizeParamSet (impostazione predefinita)
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAvailableSizesForAvailabilitySet
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAvailableSizesForVirtualMachine
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzVMSize** ottiene le dimensioni della macchina virtuale disponibili.

## ESEMPI

### Esempio 1: ottenere le dimensioni della macchina virtuale per una posizione
```
PS C:\> Get-AzVMSize -Location "Central US"
```

Questo comando consente di ottenere le dimensioni disponibili per le macchine virtuali nella posizione specificata.

### Esempio 2: ottenere le dimensioni per un set di disponibilità
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

Questo comando consente di ottenere le dimensioni disponibili per le macchine virtuali che è possibile distribuire nel set di disponibilità denominato AvailabilitySet17.

### Esempio 3: ottenere le dimensioni per una macchina virtuale esistente
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

Questo comando ottiene le dimensioni disponibili per la macchina virtuale esistente denominata VirtualMachine12.
È possibile ridimensionare la macchina virtuale in base alle dimensioni ottenute dal comando.

## PARAMETRI

### -AvailabilitySetName
Specifica il nome del set di disponibilità per cui questo cmdlet ottiene le dimensioni della macchina virtuale disponibile.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Posizione
Specifica la posizione per cui questo cmdlet ottiene le dimensioni della macchina virtuale disponibile.

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse della macchina virtuale.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Specifica il nome della macchina virtuale che questo cmdlet ottiene le dimensioni della macchina virtuale disponibile per il ridimensionamento.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineSize

## Note

## COLLEGAMENTI CORRELATI

[Get-AzVM](./Get-AzVM.md)


