---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 1ac6f9b17f954361d95e6855a618c7dbbf3d20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001789"
---
# Get-AzVmssVM

## SYNOPSIS
Ottiene le proprietà di una macchina virtuale VMSS.

## SINTASSI

### DefaultParameter (Default)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzVmssVM** ottiene la visualizzazione modello e la visualizzazione istanza di una macchina virtuale VMSS (Virtual Machine Scale Set).
La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.
La visualizzazione dell'istanza è lo stato a livello di istanza della macchina virtuale.
Specificare il *parametro Status* per ottenere solo la visualizzazione dell'istanza di una macchina virtuale.

## ESEMPI

### Esempio 1: Ottenere le proprietà di una macchina virtuale VMSS
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Questo comando ottiene le proprietà della macchina virtuale VMSS denominata VMSS001 che appartiene al gruppo di risorse denominato Group001.
Poiché il comando non specifica il parametro del parametro *InstanceView,* il cmdlet ottiene la visualizzazione modello della macchina virtuale.

### Esempio 2: Ottenere le proprietà della visualizzazione modello di una macchina virtuale VMSS
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Questo comando ottiene le proprietà della macchina virtuale VMSS denominata VMSS004 che appartiene al gruppo di risorse denominato Group002.
Il comando recupera l'ID istanza archiviato nella variabile $ID per cui ottenere la visualizzazione del modello.

### Esempio 3: Ottenere le proprietà della visualizzazione istanza di una macchina virtuale VMSS
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Questo comando ottiene le proprietà della macchina virtuale VMSS denominata VMSS004 che appartiene al gruppo di risorse denominato Group002.
Poiché il comando specifica il parametro *switch InstanceView,* il cmdlet ottiene la visualizzazione dell'istanza della macchina virtuale.
Il comando recupera l'ID istanza archiviato nella variabile $ID per cui ottenere la visualizzazione dell'istanza.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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
Specifica l'ID istanza per cui ottenere la visualizzazione del modello.

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
Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza della macchina virtuale.

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
Specifica il nome del gruppo di risorse del sistema VMSS.

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
Specie il nome del sistema VMSS.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## NOTE

## COLLEGAMENTI CORRELATI

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


