---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205379"
---
# Enable-AzBatchComputeNodeScheduling

## SYNOPSIS
Abilita la programmazione delle attività nel nodo di elaborazione specificato.

## SINTASSI

### ID (impostazione predefinita)
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Enable-AzBatchComputeNodeScheduling** abilita la pianificazione delle attività nel nodo di calcolo specificato.
Un nodo di elaborazione è una macchina virtuale di Azure dedicata a un carico di lavoro specifico dell'applicazione.

## ESEMPI

### Esempio 1: Abilitare la programmazione delle attività in un nodo di calcolo
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Questi comandi abilitano la pianificazione delle attività nel nodo di calcolo tvm-1783593343_34-20151117t222514z.
A questo scopo, il primo comando dell'esempio crea un riferimento a un oggetto contenente le chiavi dell'account batch contosobatchaccount.
Questo riferimento all'oggetto è archiviato in una variabile denominata $context.
Il secondo comando usa quindi questo riferimento all'oggetto e il cmdlet **Enable-AzBatchComputeNodeScheduling** per connettersi al pool myPool e abilitare la pianificazione delle attività in tvm-1783593343_34-20151117t222514z.

### Esempio 2: Abilitare la pianificazione delle attività nei nodi di calcolo in un pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

Questi comandi abilitano la pianificazione delle attività in tutti i nodi di calcolo trovati nel pool Pool06.
Per eseguire questa attività, il primo comando dell'esempio crea un riferimento a un oggetto contenente le chiavi dell'account batch contosobatchaccount.
Questo riferimento all'oggetto è archiviato in una variabile denominata $context.
Il secondo comando dell'esempio usa quindi questo riferimento all'oggetto e **Get-AzBatchComputeNode** per restituire una raccolta di tutti i nodi di calcolo trovati in Pool06.
Questa raccolta viene quindi reindirizzata al cmdlet **Enable-AzBatchComputeNodeScheduling,** che consente la pianificazione delle attività in ogni nodo di calcolo della raccolta.

## PARAMETERS

### -BatchContext
Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.
Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch. Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate. Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario. Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.

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
Specifica un riferimento a un oggetto al nodo di calcolo in cui è abilitata la programmazione delle attività.
Questo riferimento all'oggetto viene creato usando il cmdlet Get-AzBatchComputeNode e archiviando l'oggetto nodo di calcolo restituito in una variabile.

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

### -Id
Specifica l'ID del nodo di calcolo in cui è abilitata la programmazione delle attività.

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
Specifica l'ID del pool batch che contiene il nodo di calcolo in cui è abilitata la programmazione delle attività.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Batch. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUT

### System.Void

## NOTE

## COLLEGAMENTI CORRELATI

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


