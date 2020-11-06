---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3ba13fb1ee18f5dcc35b81ff70ebd7c5a61d1e4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508892"
---
# Get-AzureStorageTable

## Sinossi
Elenca le tabelle di archiviazione.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### TableName (impostazione predefinita)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorageTable** elenca le tabelle di archiviazione associate all'account di archiviazione in Azure.

## ESEMPI

### Esempio 1: elencare tutte le tabelle di archiviazione di Azure
```
PS C:\>Get-AzureStorageTable
```

Questo comando consente di ottenere tutte le tabelle di archiviazione per un account di archiviazione.

### Esempio 2: elencare le tabelle di archiviazione di Azure usando un carattere jolly
```
PS C:\>Get-AzureStorageTable -Name table*
```

Questo comando usa un carattere jolly per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.

### Esempio 3: elenca tabelle di archiviazione di Azure con prefisso di nome di tabella
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

Questo comando usa il parametro *Prefix* per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.

## PARAMETRI

### -Contesto
Specifica il contesto di archiviazione.
Per crearlo, puoi usare il cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Nome
Specifica il nome della tabella.
Se il nome della tabella è vuoto, il cmdlet elenca tutte le tabelle.
In caso contrario, elenca tutte le tabelle che corrispondono al nome specificato o al modello di nome normale.

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### -Prefisso
Specifica un prefisso usato nel nome della tabella o delle tabelle che vuoi ottenere.
Puoi usare questa procedura per trovare tutte le tabelle che iniziano con la stessa stringa, ad esempio tabella.

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### IStorageContext

Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline

### Stringa

Il parametro "Name" accetta il valore di tipo "String" dalla pipeline

## OUTPUT

### Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageTable

## Note

## COLLEGAMENTI CORRELATI

[New-AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


