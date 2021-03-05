---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 1e7438195b0749dabc5206238a32bc00be03ea31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994515"
---
# Disable-AzBatchComputeNodeScheduling

## SYNOPSIS
Disabilita la programmazione delle attività nel nodo di elaborazione specificato.

## SINTASSI

### ID (impostazione predefinita)
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Disable-AzBatchComputeNodeScheduling** disabilita la pianificazione delle attività nel nodo di elaborazione specificato.
Un nodo di elaborazione è una macchina virtuale di Azure dedicata a un carico di lavoro specifico dell'applicazione.
Quando si disabilita la programmazione delle attività in un nodo di elaborazione, si avrà anche la possibilità di determinare cosa fare sui processi attualmente nella coda di attività del nodo.
**Disable-AzBatchComputeNodeScheduling** consente di eseguire le operazioni seguenti: 
- Terminare le attività e rimessarle nella coda di processi.
In questo modo queste attività possono essere riprogrammate in un altro nodo di calcolo. 
- Terminare le attività e rimuoverle dalla coda di processi.
Le attività arrestate in questo modo non verranno ripianificate. 
- Attendere il completamento di tutte le attività attualmente in esecuzione e quindi disabilitare la programmazione delle attività nel nodo di calcolo. 
- Attendere il completamento di tutte le attività in esecuzione e la scadenza di tutti i periodi di conservazione dei dati, quindi disabilitare la programmazione delle attività nel nodo di calcolo.

## ESEMPI

### Esempio 1: Disabilitare la programmazione delle attività in un nodo di calcolo
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Questi comandi disabilitano la pianificazione delle attività nel nodo di elaborazione tvm-1783593343_34-20151117t222514z.
A questo scopo, il primo comando dell'esempio crea un riferimento a un oggetto alle chiavi dell'account batch contosobatchaccount.
Questo riferimento all'oggetto è archiviato in una variabile denominata $context.
Il secondo comando usa quindi questo riferimento all'oggetto e il cmdlet **Disable-AzBatchComputeNodeScheduling** per connettersi al pool myPool e disabilitare la pianificazione delle attività nel nodo tvm-1783593343_34-20151117t222514z.
Poiché il *parametro DisableComputeNodeSchedulingOptions* non è stato incluso, le attività attualmente in esecuzione nel nodo di calcolo verranno di nuovo in coda.

### Esempio 2: Disabilitare la pianificazione delle attività in tutti i nodi di calcolo in un pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

Questi comandi disabilitano la pianificazione delle attività in tutti i nodi del computer nel pool batch06.
Per eseguire questa attività, il primo comando dell'esempio crea un riferimento a un oggetto alle chiavi dell'account batch contosobatchaccount.
Questo riferimento all'oggetto è archiviato in una variabile denominata $context.
Il secondo comando nell'esempio usa quindi questo riferimento all'oggetto e **Get-AzBatchComputeNode** per restituire una raccolta di tutti i nodi di calcolo trovati in Pool06.
Viene quindi eseguito il piping di questa raccolta al cmdlet **Disable-AzBatchComputeNodeScheduling** per disabilitare la pianificazione delle attività in ogni nodo di calcolo nella raccolta.
Poiché il *parametro DisableComputeNodeSchedulingOptions* non è stato incluso, le attività attualmente in esecuzione nei nodi di calcolo verranno di nuovo in coda.

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
Specifica un riferimento a un oggetto al nodo di calcolo in cui la programmazione delle attività è disabilitata.
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

### -DisableSchedulingOption
Specifica in che modo questo cmdlet gestisce le attività attualmente in esecuzione nel nodo del computer in cui la pianificazione è disabilitata.
I valori accettabili per questo parametro sono:
- In coda.
Le attività vengono arrestate immediatamente e restituite alla coda di processi.
In questo modo le attività possono essere riprogrammate in un altro nodo di calcolo.
Questo è il valore predefinito. 
- Termina.
Le attività vengono arrestate immediatamente e rimosse dalla coda di processi.
Queste attività non verranno ripianificate. 
- TaskCompletion.
Le attività attualmente in esecuzione possono essere completate prima che la programmazione delle attività venga disabilitata nel nodo di calcolo.
Non verranno programmate nuove attività in questo nodo. 
- RetainedData.
Le attività attualmente in esecuzione potranno essere completate e i periodi di conservazione dei dati scadranno prima che la programmazione delle attività venga disabilitata nel nodo di elaborazione.
Non verranno programmate nuove attività in questo nodo.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifica l'ID del nodo di calcolo in cui la programmazione delle attività è disabilitata.

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
Specifica l'ID del pool batch che contiene il nodo di calcolo in cui la programmazione delle attività è disabilitata.
Se si usa il *parametro PoolId,* non usare il parametro *ComputeNode* nello stesso comando.

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

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


