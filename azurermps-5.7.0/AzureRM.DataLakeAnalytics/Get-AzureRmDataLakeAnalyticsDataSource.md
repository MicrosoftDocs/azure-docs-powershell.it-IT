---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 93e64c4a64eecbe66fc3f9b2923ade65405a05a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508191"
---
# Get-AzureRmDataLakeAnalyticsDataSource

## Sinossi
Ottiene un'origine dati di data Lake Analytics.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### GetAllDataSources (impostazione predefinita)
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetDataLakeStoreAccount
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBlobStorageAccount
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmDataLakeAnalyticsDataSource** ottiene un'origine dati di analisi di Azure Data Lake.

## ESEMPI

### Esempio 1: ottenere un'origine dati da un account
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

Questo comando consente di ottenere un'origine dati di data Lake Store denominata ContosoAdls da un account di analisi dei dati sul lago.

### Esempio 2: ottenere l'elenco degli account di data Lake Store in un account di analisi dei dati sul lago
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

Questo comando consente di ottenere tutti gli account dello Store Data Lake da un account di analisi dei dati del lago.

## PARAMETRI

### -Account
Specifica l'account di analisi del lago dati che questo cmdlet ottiene le origini dati.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BLOB
Specifica il nome dell'origine dati di archiviazione BLOB di Azure.

```yaml
Type: String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataLakeStore
Specifica il nome dell'account di data Lake Store.

```yaml
Type: String
Parameter Sets: GetDataLakeStoreAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse che contiene l'origine dati.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### PSStorageAccountInfo
Dettagli dell'account di archiviazione di Azure specificati.

### PSDataLakeStoreAccountInfo
Dettagli dell'account dell'archivio dati specificato del lago

### Elenco<AdlDataSource>
Elenco di account di archiviazione di Azure e di data Lake Store nell'account di analisi dei dati del lago specificato.

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureRmDataLakeAnalyticsDataSource](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[Remove-AzureRmDataLakeAnalyticsDataSource](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[Set-AzureRmDataLakeAnalyticsDataSource](./Set-AzureRmDataLakeAnalyticsDataSource.md)


