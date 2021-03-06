---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 30e6a3ec6d3cd9cba978ed51d6545b3f68375779
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508563"
---
# Set-AzureRmDataFactorySliceStatus

## Sinossi
Imposta lo stato delle sezioni per un DataSet in Azure Data Factory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ByFactoryName (impostazione predefinita)
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmDataFactorySliceStatus** imposta lo stato delle sezioni per un DataSet in Azure Data Factory.

## ESEMPI

### Esempio 1: impostare lo stato di tutte le sezioni
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
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

### -EndDateTime
Specifica la fine di un periodo di tempo come oggetto **DateTime** .
Questa volta è la fine di una sezione di dati.
Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .

*EndDateTime* deve essere specificato nel formato ISO8601 come negli esempi seguenti: 

2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (ora solare Pacifico)

L'indicatore di fuso orario predefinito è UTC.

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

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### System. Boolean

## Note
* Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory

## COLLEGAMENTI CORRELATI

[Get-AzureRmDataFactorySlice](./Get-AzureRmDataFactorySlice.md)


