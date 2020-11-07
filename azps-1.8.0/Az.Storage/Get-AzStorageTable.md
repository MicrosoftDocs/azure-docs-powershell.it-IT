---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: 5c575ace97687ca6906a73e8e79d93343f369f45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676601"
---
# Get-AzStorageTable

## Sinossi
Elenca le tabelle di archiviazione.

## SINTASSI

### TableName (impostazione predefinita)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzStorageTable** elenca le tabelle di archiviazione associate all'account di archiviazione in Azure.

## ESEMPI

### Esempio 1: elencare tutte le tabelle di archiviazione di Azure
```
PS C:\>Get-AzStorageTable
```

Questo comando consente di ottenere tutte le tabelle di archiviazione per un account di archiviazione.

### Esempio 2: elencare le tabelle di archiviazione di Azure usando un carattere jolly
```
PS C:\>Get-AzStorageTable -Name table*
```

Questo comando usa un carattere jolly per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.

### Esempio 3: elenca tabelle di archiviazione di Azure con prefisso di nome di tabella
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

Questo comando usa il parametro *Prefix* per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.

## PARAMETRI

### -Contesto
Specifica il contesto di archiviazione.
Per crearlo, puoi usare il cmdlet New-AzStorageContext.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome della tabella.
Se il nome della tabella è vuoto, il cmdlet elenca tutte le tabelle.
In caso contrario, elenca tutte le tabelle che corrispondono al nome specificato o al modello di nome normale.

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefisso
Specifica un prefisso usato nel nome della tabella o delle tabelle che vuoi ottenere.
Puoi usare questa procedura per trovare tutte le tabelle che iniziano con la stessa stringa, ad esempio tabella.

```yaml
Type: System.String
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

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext

## OUTPUT

### Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageTable

## Note

## COLLEGAMENTI CORRELATI

[New-AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


