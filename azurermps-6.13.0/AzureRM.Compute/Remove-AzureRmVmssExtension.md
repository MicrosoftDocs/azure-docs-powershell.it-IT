---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 7ede92fa653fe04072b75ce03dd6928421e01c6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507579"
---
# Remove-AzureRmVmssExtension

## Sinossi
Rimuove un'estensione da VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### NameParameterSet
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IdParameterSet
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureRmVmssExtension** consente di rimuovere un'estensione dal set di scale della macchina virtuale (VMSS).

## ESEMPI

### Esempio 1: rimuovere un'estensione VMSS
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzureRmVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

Questo comando rimuove l'estensione di un VMSS e aggiorna VMSS dopo la modifica.

### Esempio 2: rimuovere un'istanza dall'interno di un VMSS
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzureRmVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

Questo comando rimuove specifica l'ID di estensione da VMSS che appartiene al gruppo di risorse denominato Group002.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Specifica l'ID dell'estensione rimossa da questo cmdlet da VMSS.

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome dell'estensione rimossa da questo cmdlet da VMSS.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Specifica il VMSS da cui rimuovere l'estensione.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureRmVmssExtension](./Add-AzureRmVmssExtension.md)
