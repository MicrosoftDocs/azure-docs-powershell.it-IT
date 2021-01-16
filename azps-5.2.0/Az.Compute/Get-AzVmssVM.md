---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368910"
---
# Get-AzVmssVM

## Sinossi
Ottiene le proprietà di una macchina virtuale VMSS.

## SINTASSI

### DefaultParameter (impostazione predefinita)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzVmssVM** ottiene la visualizzazione modello e la visualizzazione istanza di una macchina virtuale vmss (Virtual Machine scale set).
La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.
La visualizzazione istanza è lo stato del livello di istanza della macchina virtuale.
Specifica il parametro *status* per ottenere solo la visualizzazione istanza di una macchina virtuale.

## ESEMPI

### Esempio 1: ottenere le proprietà di una macchina virtuale VMSS
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Questo comando consente di ottenere le proprietà della macchina virtuale VMSS denominata VMSS001 che appartiene al gruppo di risorse denominato Group001.
Poiché il comando non specifica il parametro *InstanceView* switch, il cmdlet ottiene la visualizzazione modello della macchina virtuale.

### Esempio 2: ottenere le proprietà della visualizzazione modello di una macchina virtuale VMSS
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Questo comando consente di ottenere le proprietà della macchina virtuale VMSS denominata VMSS004 che appartiene al gruppo di risorse denominato Group002.
Il comando ottiene l'ID istanza archiviato nella variabile $ID per cui ottenere la visualizzazione modello.

### Esempio 3: ottenere le proprietà della visualizzazione istanza di una macchina virtuale VMSS
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Questo comando consente di ottenere le proprietà della macchina virtuale VMSS denominata VMSS004 che appartiene al gruppo di risorse denominato Group002.
Poiché il comando specifica il parametro *InstanceView* switch, il cmdlet ottiene la visualizzazione dell'istanza della macchina virtuale.
Il comando ottiene l'ID istanza archiviato nella variabile $ID per cui ottenere la visualizzazione istanza.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Specifica l'ID istanza per cui ottenere la visualizzazione modello.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
Indica che questo cmdlet ottiene solo la visualizzazione istanza della macchina virtuale.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse di VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Specie il nome del VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM

## Note

## COLLEGAMENTI CORRELATI

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


