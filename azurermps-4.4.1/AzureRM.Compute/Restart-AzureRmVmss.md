---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 479aaf61169cb09d8561e9f09b05a5852c93b58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508655"
---
# Restart-AzureRmVmss

## Sinossi
Riavvia VMSS o una macchina virtuale all'interno di VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Restart-AzureRmVmss riavvia** il set di scale della macchina virtuale (VMSS).
Questo cmdlet può essere usato anche per riavviare una specifica macchina virtuale all'interno di VMSS usando il parametro *InstanceID* .

## ESEMPI

### Esempio 1: riavviare il VMSS
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

Questo comando Riavvia il VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.

### Esempio 2: riavviare una specifica macchina virtuale all'interno di VMSS
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

Questo comando Riavvia una macchina virtuale con l'ID istanza di 1 nella VMSS denominata VMSS001 che appartiene al gruppo di risorse denominato Group001.

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

### -InstanceId
Specifica, come matrice di stringhe, l'ID delle istanze che devono essere riavviate.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse di VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Specie il nome del VMSS riavviato da questo cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## OUTPUT

###  
Questo cmdlet non genera alcun output.

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[New-AzureRmVmss](./New-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Start-AzureRmVmss](./Start-AzureRmVmss.md)

[Stop-AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


