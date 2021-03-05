---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 84b5389c4f9b404b4b74783184143af310bf1ba5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002318"
---
# New-AzStorageTable

## SYNOPSIS
Crea una tabella di archiviazione.

## SINTASSI

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzStorageTable** crea una tabella di archiviazione associata all'account di archiviazione in Azure.

## ESEMPI

### Esempio 1: Creare una tabella di archiviazione di Azure
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

Questo comando crea una tabella di archiviazione con il nome tableabc.

### Esempio 2: Creare più tabelle di archiviazione di Azure
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

Questo comando crea più tabelle.
Usa il **metodo Split** della classe **stringa** .NET e quindi passa i nomi alla pipeline.

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
Specifica un nome per la nuova tabella.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

[Get-AzStorageTable](./Get-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


