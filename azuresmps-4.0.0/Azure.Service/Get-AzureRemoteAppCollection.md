---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029791"
---
# Get-AzureRemoteAppCollection

## Sinossi
Recupera informazioni su una raccolta RemoteApp di Azure.

## SINTASSI

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRemoteAppCollection** recupera informazioni sulle raccolte RemoteApp di Azure in Microsoft Azure.
Restituisce un oggetto con informazioni su una raccolta specifica o se non è specificata alcuna raccolta, per tutte le raccolte della sottoscrizione corrente.

## ESEMPI

### Esempio 1: ottenere un elenco di tutte le raccolte
```
PS C:\> Get-AzureRemoteAppCollection
```

Questo comando restituisce un elenco di tutte le raccolte RemoteApp di Azure nell'abbonamento.

### Esempio 2: ottenere informazioni su una raccolta specificata
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

Questo comando restituisce informazioni sulla raccolta RemoteApp di Azure denominata ContosoApps.

### Esempio 3: ottenere un elenco di raccolte usando un carattere jolly
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

Questo comando restituisce un elenco di tutte le raccolte RemoteApp di Azure che corrispondono a Finance *.

## PARAMETRI

### -CollectionName
Specifica il nome della raccolta RemoteApp di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

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

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


