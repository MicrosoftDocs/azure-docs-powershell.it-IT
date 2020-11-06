---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: b3e9f2608703eebd5ad24846aad7b5a1ad11e8ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521088"
---
# Get-AzureRmVmss

## Sinossi
Ottiene le proprietà di un VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### DefaultParameter (impostazione predefinita)
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmVmss** ottiene il modello e la visualizzazione dell'istanza di un set di scale della macchina virtuale (VMSS).
La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.
La visualizzazione istanza è lo stato del livello di istanza della macchina virtuale.
Specifica il parametro *status* per ottenere solo la visualizzazione istanza di una macchina virtuale.

## ESEMPI

### Esempio 1: ottenere le proprietà di un VMSS
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Questo comando consente di ottenere le proprietà del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.
Poiché il comando non specifica il parametro *InstanceView* switch, il cmdlet ottiene la visualizzazione modello della macchina virtuale.

## PARAMETRI

### -InstanceView
Indica che questo cmdlet ottiene solo la visualizzazione istanza della macchina virtuale.

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse di VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Specie il nome del VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Questo cmdlet non genera alcun output.

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmVmss](./New-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Riavviare-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Start-AzureRmVmss](./Start-AzureRmVmss.md)

[Stop-AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


