---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: e85976b4d4b5de508e1a4f25338b21abdb0c097f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983469"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## SYNOPSIS
Recupera lo stato delle attività di preparazione e rilascio dei processi batch.

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

## DESCRIZIONE
Il cmdlet **Get-AzBatchJobPreparationAndReleaseTaskStatus** ottiene il cmdlet Azure Batch job preparation and release task status for a Batch job.
È necessario specificare il *parametro ID* o un'istanza **PSCloudJob** per questo cmdlet.

## ESEMPI

### Esempio 1: Ottenere lo stato di preparazione e rilascio di un processo
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Questo comando recupera lo stato delle attività di preparazione e rilascio per il processo "Test".
Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.

### Esempio 2: Ottenere lo stato di preparazione e rilascio di un processo con filtro e selezione specificati
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Questo comando recupera lo stato delle attività di preparazione e rilascio per il processo "Test" nel nodo "tvm-2316545714_1-20170613t201733z" e usa la clausola Select per specificare di restituire solo le informazioni su JobPreparationTaskExecutionInformation

## PARAMETERS

### -BatchContext
Istanza BatchAccountContext da usare quando si interagisce con il servizio batch.
Usare il cmdlet Get-AzBatchAccountKey batch per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.

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

### -Expand
Specifica una clausola di espansione OData (Open Data Protocol).
Specificare un valore per questo parametro per ottenere entità associate dell'entità principale da ottenere.

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

### -Filter
Specifica una clausola del filtro OData.
Se non si specifica un filtro, questo cmdlet restituisce tutti gli stati delle attività di preparazione e rilascio per il processo.

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

### -Id
Specifica l'ID del processo di cui recuperare le attività di preparazione e rilascio.
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
Specifica un oggetto **PSCloudJob** che rappresenta il processo da cui recuperare lo stato di preparazione e rilascio dell'attività.
Per ottenere un **oggetto PSCloudJob,** usare il cmdlet Get-AzBatchJob.

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
Specifica il numero massimo di processi di preparazione e stato delle attività di rilascio da restituire.
Se si specifica un valore uguale o inferiore a zero (0), il cmdlet non usa un limite superiore.
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

### -Select
Specifica una clausola di selezione OData.
Specificare un valore per questo parametro per ottenere proprietà specifiche invece di tutte le proprietà dell'oggetto.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Batch. Models.PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUT

### Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Cmdlet batch di Azure](/powershell/module/Az.Batch/)
