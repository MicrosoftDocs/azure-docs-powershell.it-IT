---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 6c890836d8ca22e617fdc88788a6809cbce8581c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687550"
---
# Enable-AzureBatchComputeNodeScheduling

## Sinossi
Consente la pianificazione delle attività nel nodo Compute specificato.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ID (impostazione predefinita)
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Enable-AzureBatchComputeNodeScheduling** Abilita la pianificazione delle attività nel nodo Compute specificato.
Un nodo COMPUTE è una macchina virtuale di Azure dedicata a un carico di lavoro specifico dell'applicazione.

## ESEMPI

### Esempio 1: abilitare la pianificazione delle attività in un nodo Compute
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Questi comandi consentono la pianificazione delle attività nel nodo di calcolo TVM-1783593343_34-20151117t222514z.
A questo scopo, il primo comando nell'esempio crea un riferimento a un oggetto contenente le chiavi dell'account per l'account batch contosobatchaccount.
Questo riferimento oggetto è archiviato in una variabile denominata $context.

Il secondo comando usa quindi questo riferimento di oggetto e il cmdlet **Enable-AzureBatchComputeNodeScheduling** per connettersi al pool e abilitare la pianificazione delle attività in TVM-1783593343_34-20151117t222514z.

### Esempio 2: abilitare la pianificazione delle attività sui nodi di calcolo in un pool
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

Questi comandi consentono la pianificazione delle attività in tutti i nodi di calcolo presenti nel pool Pool06.
Per eseguire questa attività, il primo comando nell'esempio crea un riferimento a un oggetto contenente le chiavi dell'account per l'account batch contosobatchaccount.
Questo riferimento oggetto è archiviato in una variabile denominata $context.

Il secondo comando nell'esempio usa quindi questo riferimento di oggetto e **Get-AzureBatchComputeNode** per restituire una raccolta di tutti i nodi di calcolo trovati in Pool06.
La raccolta viene quindi inviata tramite pipe al cmdlet **Enable-AzureBatchComputeNodeScheduling** , che consente la pianificazione delle attività in ogni nodo COMPUTE della raccolta.

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

### -ComputeNode
Specifica un riferimento a un oggetto al nodo COMPUTE in cui è abilitata la pianificazione delle attività.
Questo riferimento all'oggetto viene creato usando il cmdlet Get-AzureBatchComputeNode e archiviando l'oggetto compute node restituito in una variabile.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ID
Specifica l'ID del nodo COMPUTE in cui è abilitata la pianificazione delle attività.

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Specifica l'ID del pool di batch che contiene il nodo COMPUTE in cui è abilitata la pianificazione delle attività.

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

### PSComputeNode
Il parametro ' ComputeNode ' accetta il valore di tipo ' PSComputeNode ' dalla pipeline

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Disable-AzureBatchComputeNodeScheduling](./Disable-AzureBatchComputeNodeScheduling.md)


