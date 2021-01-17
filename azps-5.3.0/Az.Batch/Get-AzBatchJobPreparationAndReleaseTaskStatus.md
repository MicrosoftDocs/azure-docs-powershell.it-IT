---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478359"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## Sinossi
Ottiene la preparazione del processo batch e lo stato dell'attività di rilascio.

## SINTASSI

### ID (impostazione predefinita)
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzBatchJobPreparationAndReleaseTaskStatus** ottiene la preparazione del processo batch di Azure e lo stato dell'attività di rilascio per un processo batch.
Devi specificare il parametro *ID* o un'istanza di **PSCloudJob** per questo cmdlet.

## ESEMPI

### Esempio 1: ottenere la preparazione del processo e lo stato di rilascio di un processo
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Questo comando consente di ottenere la preparazione del processo e lo stato dell'attività di rilascio per il processo "test".
Usa il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla variabile $Context.

### Esempio 2: ottenere la preparazione del processo e lo stato di rilascio di un processo con filtro e selezionare specificato
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Questo comando ottiene lo stato dell'attività di preparazione e rilascio del processo per il processo "test" nel nodo "TVM-2316545714_1-20170613t201733z" e usa la clausola SELECT per specificare di restituire solo le informazioni di JobPreparationTaskExecutionInformation

## PARAMETRI

### -BatchContext
Istanza di BatchAccountContext da usare per interagire con il servizio batch.
Usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.

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

### -Espandi
Specifica una clausola di espansione OData (Open Data Protocol).
Specifica un valore per questo parametro per ottenere le entità associate dell'entità principale che ottieni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filtro
Specifica una clausola di filtro OData.
Se non specifichi un filtro, questo cmdlet restituisce tutti i processi di preparazione e rilascio dell'attività per il processo.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Specifica l'ID del processo di cui devono essere recuperate le attività di preparazione e rilascio.
Non è possibile specificare caratteri jolly.

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

### -InputObject
Specifica un oggetto **PSCloudJob** che rappresenta il processo per ottenere la preparazione e il rilascio dello stato dell'attività.
Per ottenere un oggetto **PSCloudJob** , usa il cmdlet Get-AzBatchJob.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
Specifica il numero massimo di operazioni di preparazione e rilascio dello stato dell'attività da restituire.
Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.
Il valore predefinito è 1000.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Selezionare
Specifica una clausola di selezione OData.
Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft.Azure.Commands.Batch. Models. PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUT

### Microsoft.Azure.Commands.Batch. Models. PSJobPreparationAndReleaseTaskExecutionInformation

## Note

## COLLEGAMENTI CORRELATI

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Cmdlet batch di Azure](/powershell/module/Az.Batch/)
