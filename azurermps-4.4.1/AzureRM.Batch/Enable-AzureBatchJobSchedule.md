---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: c012fe266bc25752729b14192c4d9c0a42cd8961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521791"
---
# Enable-AzureBatchJobSchedule

## Sinossi
Abilita una pianificazione processo batch.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Enable-AzureBatchJobSchedule** Abilita una pianificazione del processo batch di Azure.
Dopo l'abilitazione di una pianificazione processo, i processi possono essere creati in base a tale programmazione.

## ESEMPI

### Esempio 1: abilitare una pianificazione del processo
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

Questo comando Abilita la pianificazione del processo con ID JobSchedule17.
Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.

## PARAMETRI

### -BatchContext
Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.
Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ID
Specifica l'ID della pianificazione del processo abilitata da questo cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### BatchAccountContext
Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline

### Stringa
Il parametro "ID" accetta il valore di tipo "String" dalla pipeline

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Disable-AzureBatchJobSchedule](./Disable-AzureBatchJobSchedule.md)

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJobSchedule](./Get-AzureBatchJobSchedule.md)

[New-AzureBatchJobSchedule](./New-AzureBatchJobSchedule.md)

[Remove-AzureBatchJobSchedule](./Remove-AzureBatchJobSchedule.md)

[Stop-AzureBatchJobSchedule](./Stop-AzureBatchJobSchedule.md)

[Cmdlet batch di Azure](./AzureRM.Batch.md)


