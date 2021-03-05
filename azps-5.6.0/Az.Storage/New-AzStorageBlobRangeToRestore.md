---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: 0f74ad9b146a0c5d2f2c65b7109fb57f56902834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002590"
---
# New-AzStorageBlobRangeToRestore

## SYNOPSIS
Crea un oggetto Intervallo BLOB per ripristinare un account di archiviazione.

## SINTASSI

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzStorageBlobRangeToRestore** crea un oggetto intervallo BLOB, che può essere usato in Restore-AzStorageBlobRange.

## ESEMPI

### Esempio 1: Crea un intervallo BLOB da ripristinare
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Questo comando crea un intervallo BLOB da ripristinare, che inizia in container1/BLOB1 (include) e termina con container2/BLOB2 (exclude).

### Esempio 2: Crea un intervallo BLOB che ripristina dal primo BLOB in ordine alfabetico, a un BLOB specifico (escluso)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Questo comando crea un intervallo BLOB che ripristina dal primo BLOB in ordine alfabetico a uno specifico BLOB container2/BLOB2 (exclude)

### Esempio 3: Crea un intervallo BLOB che ripristina da un BLOB specifico (include) all'ultimo BLOB in ordine alfabetico
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Questo comando crea un intervallo BLOB che ripristina da uno specifico contenitore BLOB1/BLOB1 (include) all'ultimo BLOB in ordine alfabetico.

### Esempio 4: Crea un intervallo BLOB che ripristina tutti i BLOB
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Questo comando crea un intervallo BLOB che ripristina tutti i BLOB.

## PARAMETERS

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

### -EndRange
Specificare l'intervallo finale del ripristino BLOB.
L'intervallo finale verrà escluso nei BLOB di ripristino.
Impostarlo come strng vuoto per ripristinare l'impostazione finale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRange
Specificare l'intervallo iniziale di ripristino BLOB.
L'intervallo iniziale verrà incluso nei BLOB di ripristino.
Impostarla come stringa vuota per ripristinarla dall'inizio.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange

## NOTE

## COLLEGAMENTI CORRELATI
