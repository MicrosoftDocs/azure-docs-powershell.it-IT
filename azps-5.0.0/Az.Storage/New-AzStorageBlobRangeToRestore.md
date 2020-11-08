---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200637"
---
# New-AzStorageBlobRangeToRestore

## Sinossi
Crea un oggetto Range BLOB per ripristinare un account di archiviazione.

## SINTASSI

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzStorageBlobRangeToRestore** crea un oggetto Range BLOB, che può essere usato in Restore-AzStorageBlobRange.

## ESEMPI

### Esempio 1: crea un intervallo di BLOB da ripristinare
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Questo comando crea un intervallo di BLOB da ripristinare, che inizia in container1/blob1 (include), e termina in container2/blob2 (Escludi).

### Esempio 2: crea un intervallo di BLOB che verrà ripristinato dal primo BLOB in ordine alfabetico a un blob specifico (Escludi)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Questo comando crea un intervallo di BLOB che ripristinerà dal primo BLOB di ordine alfabetico a un blob specifico container2/blob2 (Escludi)

### Esempio 3: crea un intervallo di BLOB che verrà ripristinato da un blob specifico (include), all'ultimo BLOB in ordine alfabetico
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Questo comando crea un intervallo di BLOB che verrà ripristinato da un blob specifico container1/blob1 (include), all'ultimo BLOB in ordine alfabetico.

### Esempio 4: crea un intervallo di BLOB che ripristinerà tutti i BLOB
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Questo comando crea un intervallo di BLOB che ripristinerà tutti i BLOB.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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
Specificare l'intervallo di fine ripristino BLOB.
L'intervallo di fine verrà escluso in ripristini BLOB.
Impostarlo come strng vuoto da ripristinare alla fine.

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
Specificare l'intervallo di inizio ripristino BLOB.
L'intervallo di inizio verrà incluso nei BLOB di ripristino.
Impostarla come stringa vuota per il ripristino dall'inizio.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Management. storage. Models. PSBlobRestoreRange

## Note

## COLLEGAMENTI CORRELATI
