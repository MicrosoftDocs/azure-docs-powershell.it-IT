---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: 497899400c05697fb9b273a89743172b672e4892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975310"
---
# Get-AzDataFactorySlice

## SYNOPSIS
Recupera le sezioni di dati per un set di dati in Data factory di Azure.

## SINTASSI

### ByFactoryName (Default)
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzDataFactorySlice** ottiene le sezioni di dati per un set di dati in Data factory di Azure.
Specificare un'ora di inizio e un'ora di fine per definire un intervallo di sezioni di dati da visualizzare.
Lo stato di una sezione dati è uno dei valori seguenti: 
- PendingExecution.
L'elaborazione dati non è stata avviata. 
- InProgress.
L'elaborazione dei dati è in corso. 
- Pronto.
L'elaborazione dei dati è stata completata.
La sezione dati è pronta per essere utilizzata dalle sezioni dipendenti. 
- Operazione non riuscita.
L'esecuzione che genera la sezione non è riuscita. 
- Ignora.
Data factory ignora l'elaborazione della sezione. 
- Riprova.
Data factory esegue nuovamente l'esecuzione che genera la sezione. 
- Timeout. Timeout dell'elaborazione dati. 
- PendingValido.
La sezione dati è in attesa di convalida prima dell'elaborazione. 
- Riprova convalida.
Data factory riprova la convalida della sezione. 
- Convalida non riuscita.
Convalida della sezione non riuscita.
Per ognuna delle sezioni, è possibile visualizzare altre informazioni sull'esecuzione che genera la sezione usando il cmdlet Get-AzDataFactoryRun.

## ESEMPI

### Esempio 1: Recuperare sezioni di dati per un set di dati
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

Questo comando recupera tutte le sezioni di dati per il set di dati denominato WikiAggregatedData nel data factory denominato WikiADF.
Il comando ottiene le sezioni prodotti dopo l'ora specificata dal parametro StartDateTime.
Il codice di esempio seguente imposta la disponibilità di questo set di dati ogni ora nel file JSON (JavaScript Object Notation).
disponibilità: { periodo: "Ora", periodMultiplier: 1 } Alcuni dei risultati sono pronti e altri sono in attesa di esecuzione.
Le sezioni pronte sono già state eseguite.
Le sezioni in sospeso sono in attesa di essere eseguite alla fine di ogni ora nell'intervallo specificato dal cmdlet Set-AzDataFactoryPipelineActivePeriod in sospeso.
In questo esempio, sia i periodi di inizio che di fine per la pipeline e la sezione hanno un valore di un giorno (24 ore).

### Esempio 2

Recupera le sezioni di dati per un set di dati in Data factory di Azure. (autogenerati)

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## PARAMETERS

### -DataFactory
Specifica un **oggetto PSDataFactory.**
Questo cmdlet ottiene le sezioni che appartengono al data factory specificato da questo parametro.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Specifica il nome di un data factory.
Questo cmdlet ottiene le sezioni che appartengono al data factory specificato da questo parametro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatasetName
Specifica il nome del set di dati per cui il cmdlet ottiene le sezioni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -EndDateTime
Specifica la fine di un periodo di tempo come **oggetto DateTime.**
Questo cmdlet ottiene le sezioni prodotti prima dell'ora specificata da questo parametro.
Per altre informazioni sugli **oggetti DateTime,** digitare `Get-Help Get-Date` .
*EndDateTime* deve essere specificato nel formato ISO8601 come negli esempi seguenti: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (ora standard del Pacifico) Il fuso orario predefinito è UTC.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse azure.
Questo cmdlet recupera le sezioni che appartengono al gruppo specificato da questo parametro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDateTime
Specifica l'inizio di un periodo di tempo come **oggetto DateTime.**
Questo cmdlet ottiene le sezioni prodotti dopo il tempo specificato da questo parametro.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## OUTPUT

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## NOTE
* Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori

## COLLEGAMENTI CORRELATI

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


