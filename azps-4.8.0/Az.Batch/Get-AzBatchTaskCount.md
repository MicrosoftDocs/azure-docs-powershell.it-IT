---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191663"
---
# Get-AzBatchTaskCount

## Sinossi
Ottiene i conteggi delle attività per il processo specificato.

## SINTASSI

### ID
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzBatchTaskCount** ottiene il conteggio delle attività batch di Azure per un processo batch.
Specificare un processo per il parametro *JobID* o per il parametro *Job* .
I conteggi delle attività offrono un conteggio delle attività tramite lo stato dell'attività attivo, in corso o completato e un conteggio delle attività che hanno avuto esito positivo o negativo. Le attività nello stato di preparazione vengono conteggiate come in corso. Se validationStatus non è convalidato, il servizio batch non è stato in grado di controllare i conteggi degli Stati in base agli Stati delle attività riportati nell'API elenco attività. ValidationStatus potrebbe non essere convalidato se il processo contiene più di 200.000 attività.

## ESEMPI

### Esempio 1: ottenere i conteggi delle attività in base all'ID
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Questo comando consente di ottenere i conteggi delle attività per Job Job01.
Usa il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla variabile $Context.

## PARAMETRI

### -BatchContext
Istanza di BatchAccountContext da usare per interagire con il servizio batch.
Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.
Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.
Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.
Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.

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

### -Job
Specifica il processo che contiene le attività ottenute da questo cmdlet.
Per ottenere un oggetto **PSCloudJob** , usa il cmdlet Get-AzBatchJob.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
ID del processo per cui viene conteggiato l'attività.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### Microsoft.Azure.Commands.Batch. Models. PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUT

### Microsoft.Azure.Commands.Batch. Models. PSTaskCounts

## Note

## COLLEGAMENTI CORRELATI

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Cmdlet batch di Azure](/powershell/module/Az.Batch/)
