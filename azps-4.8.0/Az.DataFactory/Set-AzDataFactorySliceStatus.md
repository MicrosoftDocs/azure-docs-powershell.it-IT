---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 8b2c55a069463120b861f1ea928ac0163a4c37df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189111"
---
# Set-AzDataFactorySliceStatus

## Sinossi
Imposta lo stato delle sezioni per un DataSet in Azure Data Factory.

## SINTASSI

### ByFactoryName (impostazione predefinita)
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzDataFactorySliceStatus** imposta lo stato delle sezioni per un DataSet in Azure Data Factory.

## ESEMPI

### Esempio 1: impostare lo stato di tutte le sezioni
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

Questo comando imposta lo stato di tutte le sezioni per il DataSet denominato DAWikiAggregatedData in attesa nella data factory denominata WikiADF.
Il parametro *UpdateType* ha un valore di UpstreamInPipeline e quindi il comando imposta lo stato di ogni sezione per DataSet e tutti i set di dati dipendenti.
I DataSet dipendenti vengono usati come set di dati di input per le attività della pipeline.
Questo comando restituisce un valore di $True.

## PARAMETRI

### -DataFactory
Specifica un oggetto **PSDataFactory** .
Questo cmdlet modifica lo stato delle sezioni che appartengono alla data factory specificata da questo parametro.

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
Questo cmdlet modifica lo stato delle sezioni che appartengono alla data factory specificata da questo parametro.

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
Specifica il nome del DataSet per cui questo cmdlet modifica le sezioni.

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
Questa volta è la fine di una sezione di dati.
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
Questo cmdlet modifica lo stato delle sezioni che appartengono al gruppo specificato da questo parametro.

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
Questa volta è l'inizio di una sezione di dati.

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

### -Stato
Specifica uno stato da assegnare alla sezione dati.
I valori accettabili per questo parametro sono i seguenti:
- In attesa.
La sezione dati attende la convalida per i criteri di convalida prima dell'elaborazione. 
- Pronto.
L'elaborazione dei dati è stata completata e la sezione dati è pronta.
- InProgress.
L'elaborazione dei dati è in corso. 
- Fallito.
L'elaborazione dei dati non è riuscita.
- Ignorato.
Ignorato l'elaborazione della sezione dati.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateType
Specifica il tipo di aggiornamento alla sezione.
I valori accettabili per questo parametro sono i seguenti:
- Singoli.
Imposta lo stato di ogni sezione per il DataSet nell'intervallo di tempo specificato. 
- UpstreamInPipeline.
Imposta lo stato di ogni sezione per il DataSet e tutti i set di dati dipendenti, che vengono usati come set di dati di input per le attività della pipeline.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## OUTPUT

### System. Boolean

## Note
* Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory

## COLLEGAMENTI CORRELATI

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


