---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d4296acd16b29640fa8925d8482cca012be27b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994795"
---
# Get-AzStorageTable

## SYNOPSIS
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

## DESCRIZIONE
Il cmdlet **Get-AzStorageTable elenca** le tabelle di archiviazione associate all'account di archiviazione in Azure.

## ESEMPI

### Esempio 1: Elencare tutte le tabelle di Archiviazione di Azure
```
PS C:\>Get-AzStorageTable
```

Questo comando recupera tutte le tabelle di archiviazione per un account di archiviazione.

### Esempio 2: Elencare le tabelle di Archiviazione di Azure usando un carattere jolly
```
PS C:\>Get-AzStorageTable -Name table*
```

Questo comando usa un carattere jolly per ottenere le tabelle di archiviazione il cui nome inizia con tabella.

### Esempio 3: Elencare le tabelle di Archiviazione di Azure usando il prefisso del nome della tabella
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

Questo comando usa il parametro *Prefix* per ottenere le tabelle di archiviazione il cui nome inizia con table.

## PARAMETERS

### -Context
Specifica il contesto di archiviazione.
Per crearlo, è possibile usare il cmdlet New-AzStorageContext.

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
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -Name
Specifica il nome della tabella.
Se il nome della tabella è vuoto, il cmdlet elenca tutte le tabelle.
In caso contrario, elenca tutte le tabelle che corrispondono al nome specificato o al criterio del nome normale.

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

### -Prefix
Specifica un prefisso usato nel nome della tabella o delle tabelle da ottenere.
È possibile usarla per trovare tutte le tabelle che iniziano con la stessa stringa, ad esempio tabella.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUT

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


