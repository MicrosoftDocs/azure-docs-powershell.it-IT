---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030033"
---
# Get-AzureRemoteAppVM

## Sinossi
Ottiene le macchine virtuali in una raccolta RemoteApp di Azure.

## SINTASSI

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRemoteAppVM** ottiene le macchine virtuali create in una raccolta RemoteApp di Azure per l'hosting della sessione.

## ESEMPI

### Esempio 1: visualizzare le macchine virtuali in una raccolta
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

Questo comando Visualizza le macchine virtuali usate per l'hosting della sessione in una raccolta RemoteApp di Azure denominata Contoso.

## PARAMETRI

### -CollectionName
Specifica il nome della raccolta RemoteApp di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
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

[Riavviare-AzureRemoteAppVM](./Restart-AzureRemoteAppVM.md)


