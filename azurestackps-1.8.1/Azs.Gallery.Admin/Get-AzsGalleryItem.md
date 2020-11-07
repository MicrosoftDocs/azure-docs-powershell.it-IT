---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93860030"
---
# Get-AzsGalleryItem

## Sinossi
Elenca gli elementi della raccolta.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzsGalleryItem [<CommonParameters>]
```

### Ottieni
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## Descrizione
Ottenere un elenco di elementi della raccolta disponibili in Azure stack Marketplace

## ESEMPI

### ESEMPIO 1
```
Get-AzsGalleryItem
```

Elementi della raccolta elenchi.

### ESEMPIO 2
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

Ottenere un elemento della raccolta in base al nome.

## PARAMETRI

### -Nome
Identità dell'elemento della raccolta.
Include il nome dell'autore, il nome dell'elemento e può includere la versione separata per carattere periodo.

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. gallery. admin. Models. GalleryItem

## Note

## COLLEGAMENTI CORRELATI
