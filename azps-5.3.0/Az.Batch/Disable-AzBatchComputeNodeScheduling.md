---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478424"
---
# Disable-AzBatchComputeNodeScheduling

## Sinossi
Disabilita la pianificazione delle attività nel nodo Compute specificato.

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

## Descrizione
Il cmdlet **Disable-AzBatchComputeNodeScheduling Disabilita** la pianificazione delle attività nel nodo Compute specificato.
Un nodo COMPUTE è una macchina virtuale di Azure dedicata a un carico di lavoro specifico dell'applicazione.
Quando si disattiva la programmazione delle attività in un nodo di calcolo, si avrà anche la possibilità di determinare le operazioni da eseguire sui processi attualmente presenti nella coda delle attività del nodo.
**Disable-AzBatchComputeNodeScheduling** consente di eseguire le operazioni seguenti: 
- Terminare le attività e riportarle nella coda processi.
Ciò consente di ripianificare le attività in un altro nodo COMPUTE. 
- Terminare le attività e rimuoverle dalla coda processi.
Le attività interrotte in questo modo non verranno riprogrammate. 
- Attendere che tutte le attività attualmente in esecuzione vengano completate e quindi disabilitare la programmazione delle attività nel nodo COMPUTE. 
- Attendere che tutte le attività in esecuzione vengano completate e tutti i periodi di conservazione dei dati scadano e quindi disabilitare la programmazione delle attività nel nodo COMPUTE.

## ESEMPI

### Esempio 1: disabilitare la pianificazione delle attività in un nodo Compute
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Questi comandi disabilitano la programmazione delle attività nel nodo di calcolo TVM-1783593343_34-20151117t222514z.
A questo scopo, il primo comando nell'esempio crea un riferimento a un oggetto alle chiavi dell'account per l'account batch contosobatchaccount.
Questo riferimento oggetto è archiviato in una variabile denominata $context.
Il secondo comando usa quindi questo riferimento di oggetto e il cmdlet **Disable-AzBatchComputeNodeScheduling** per connettersi al pool e disabilitare la programmazione delle attività nel nodo TVM-1783593343_34-20151117t222514z.
Dato che il parametro *DisableComputeNodeSchedulingOptions* non è stato incluso, le attività attualmente in uso nel nodo COMPUTE verranno accodate.

### Esempio 2: disabilitare la programmazione delle attività in tutti i nodi di calcolo in un pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

Questi comandi disabilitano la programmazione delle attività in tutti i nodi del computer nel pool di Pool06.
Per eseguire questa attività, il primo comando nell'esempio crea un riferimento a un oggetto alle chiavi dell'account per l'account batch contosobatchaccount.
Questo riferimento oggetto è archiviato in una variabile denominata $context.
Il secondo comando nell'esempio usa quindi questo riferimento di oggetto e **Get-AzBatchComputeNode** per restituire una raccolta di tutti i nodi di calcolo trovati in Pool06.
La raccolta viene quindi inviata tramite pipe al cmdlet **Disable-AzBatchComputeNodeScheduling** per disabilitare la pianificazione delle attività in ogni nodo COMPUTE della raccolta.
Dato che il parametro *DisableComputeNodeSchedulingOptions* non è stato incluso, le attività in corso sui nodi COMPUTE verranno accodate.

## PARAMETRI

### -BatchContext
Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.
Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch. Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati. Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita. Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.

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
Specifica un riferimento a un oggetto al nodo COMPUTE in cui la pianificazione delle attività è disabilitata.
Questo riferimento all'oggetto viene creato usando il cmdlet Get-AzBatchComputeNode e archiviando l'oggetto compute node restituito in una variabile.

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

### -DisableSchedulingOption
Specifica il modo in cui questo cmdlet tratta le attività attualmente in uso nel nodo del computer in cui viene disabilitata la pianificazione.
I valori accettabili per questo parametro sono i seguenti:
- Riaccodare.
Le attività vengono interrotte immediatamente e restituite alla coda processi.
Ciò consente di ripianificare le attività in un altro nodo COMPUTE.
Questo è il valore predefinito. 
- Terminare.
Le attività vengono arrestate immediatamente e rimosse dalla coda processi.
Queste attività non verranno riprogrammate. 
- TaskCompletion.
Le attività in esecuzione saranno in grado di completare prima della disattivazione della pianificazione delle attività nel nodo COMPUTE.
In questo nodo non verranno pianificate nuove attività. 
- RetainedData.
Le attività in esecuzione saranno in grado di completare e i periodi di conservazione dei dati potranno scadere prima che la pianificazione delle attività sia disabilitata nel nodo COMPUTE.
In questo nodo non verranno pianificate nuove attività.

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

### -ID
Specifica l'ID del nodo COMPUTE in cui la pianificazione delle attività è disabilitata.

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
Specifica l'ID del pool di batch che contiene il nodo COMPUTE in cui la pianificazione delle attività è disabilitata.
Se usi il parametro *PoolId* , non usare il parametro *ComputeNode* nello stesso comando.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft.Azure.Commands.Batch. Models. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUT

### System. void

## Note

## COLLEGAMENTI CORRELATI

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


