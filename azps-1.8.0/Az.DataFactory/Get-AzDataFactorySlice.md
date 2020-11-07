---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a4f83bf560af1643d2971ed7644089cee26759c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684622"
---
# Get-AzDataFactorySlice

## Sinossi
Ottiene le fette di dati per un DataSet in Azure Data Factory.

## SINTASSI

### ByFactoryName (impostazione predefinita)
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

## Descrizione
Il cmdlet **Get-AzDataFactorySlice** ottiene le fette di dati per un DataSet in Azure Data Factory.
Specificare l'ora di inizio e l'ora di fine per definire un intervallo di sezioni di dati da visualizzare.
Lo stato di una fetta di dati è uno dei valori seguenti: 
- PendingExecution.
L'elaborazione dei dati non è stata avviata. 
- InProgress.
L'elaborazione dei dati è in corso. 
- Pronto.
L'elaborazione dei dati è completata.
La sezione dati è pronta per l'utilizzo delle sezioni dipendenti. 
- Fallito.
L'esecuzione che produce la sezione non è riuscita. 
- Ignorare.
Data Factory ignora l'elaborazione della sezione. 
- Tentativi.
Data Factory ritenta l'esecuzione che produce la sezione. 
- Scaduta. L'elaborazione dei dati è scaduta. 
- PendingValidation.
La data Slice attende la convalida prima che venga elaborata. 
- Ripetere la convalida.
Data Factory ritenta la convalida della sezione. 
- Convalida non riuscita.
La convalida della sezione non è riuscita.
Per ognuna delle sezioni, è possibile visualizzare altre informazioni sull'esecuzione che produce la sezione usando il cmdlet Get-AzDataFactoryRun.

## ESEMPI

### Esempio 1: recuperare le fette di dati per un DataSet
```
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

Questo comando consente di ottenere tutte le fette di dati per il DataSet denominato WikiAggregatedData nella Factory di dati denominata WikiADF.
Il comando ottiene le sezioni prodotte dopo il tempo specificato dal parametro StartDateTime.
Il codice di esempio seguente imposta la disponibilità per questo DataSet ogni ora nel file JSON (JavaScript Object Notation).
disponibilità: {periodo: "hour", periodMultiplier: 1} alcuni dei risultati sono pronti e altri sono PendingExecution.
Le sezioni pronte sono già state eseguite.
Le sezioni in sospeso sono in attesa di esecuzione alla fine di ogni ora nell'intervallo specificato dal cmdlet Set-AzDataFactoryPipelineActivePeriod.
In questo esempio, i periodi di inizio e di fine per la pipeline e la sezione hanno un valore di un giorno (24 ore).

## PARAMETRI

### -DataFactory
Specifica un oggetto **PSDataFactory** .
Questo cmdlet consente di ottenere le sezioni che appartengono alla Factory di dati specificata da questo parametro.

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

### -Datafactoryname
Specifica il nome di una data factory.
Questo cmdlet consente di ottenere le sezioni che appartengono alla Factory di dati specificata da questo parametro.

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

### -DataSetName
Specifica il nome del DataSet per cui questo cmdlet ottiene le sezioni.

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
Specifica la fine di un periodo di tempo come oggetto **DateTime** .
Questo cmdlet ottiene le sezioni prodotte prima del tempo specificato da questo parametro.
Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .
*EndDateTime* deve essere specificato nel formato ISO8601, come negli esempi seguenti: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (ora solare Pacifico) l'identificatore del fuso orario predefinito è UTC.

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
Specifica il nome di un gruppo di risorse Azure.
Questo cmdlet ottiene le sezioni che appartengono al gruppo specificato da questo parametro.

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
Specifica l'inizio di un periodo di tempo come oggetto **DateTime** .
Questo cmdlet ottiene le sezioni prodotte dopo il tempo specificato da questo parametro.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## OUTPUT

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## Note
* Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory

## COLLEGAMENTI CORRELATI

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


