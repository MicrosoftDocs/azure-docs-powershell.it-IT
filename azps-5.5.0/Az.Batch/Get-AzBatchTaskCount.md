---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205226"
---
# Get-AzBatchTaskCount

## SYNOPSIS
Ottiene il conteggio delle attività per il processo specificato.

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

## DESCRIZIONE
Il **cmdlet Get-AzBatchTaskCount** ottiene il numero di attività batch di Azure per un processo batch.
Specificare un processo usando il *parametro JobId* o *Job.*
Il numero di attività fornisce un conteggio delle attività per stato di attività attive, in esecuzione o completate e un numero di attività che ha avuto esito positivo o negativo. Le attività in stato di preparazione vengono conteggiate come in esecuzione. Se validationStatus non è convalidato, il servizio batch non è stato in grado di controllare il conteggio dello stato rispetto agli stati dell'attività, come riportato nell'API Attività elenco. Lo stato di convalida potrebbe non essere convalidato se il processo contiene più di 200.000 attività.

## ESEMPI

### Esempio 1: Ottenere il conteggio delle attività per ID
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Questo comando recupera il conteggio delle attività per il processo Job01.
Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.

## PARAMETERS

### -BatchContext
Istanza BatchAccountContext da usare quando si interagisce con il servizio batch.
Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.
Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.
Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.
Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.

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

### -Job
Specifica il processo che contiene le attività recuperate da questo cmdlet.
Per ottenere un **oggetto PSCloudJob,** usare il cmdlet Get-AzBatchJob.

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
ID del processo per cui ottenere il conteggio delle attività.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### Microsoft.Azure.Commands.Batch. Models.PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUT

### Microsoft.Azure.Commands.Batch. Models.PSTaskCounts

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Cmdlet batch di Azure](/powershell/module/Az.Batch/)
