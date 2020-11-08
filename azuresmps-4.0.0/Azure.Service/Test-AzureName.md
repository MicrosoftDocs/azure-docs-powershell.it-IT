---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023895"
---
# Test-AzureName

## Sinossi
Verifica se un nome del servizio cloud di Microsoft Azure, il nome del servizio di archiviazione o il nome dello spazio dei nomi Service Bus esiste oppure no.

## SINTASSI

### Servizio
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Archiviazione
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServiceBusNamespace
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Sito Web
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Se il nome esiste, il cmdlet restituisce $True.
Se il nome non esiste, restituisce $False.

## ESEMPI

### Esempio 1
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

Questo comando consente di verificare se "MyNameService1" è un nome di servizio cloud di Microsoft Azure esistente.

### Esempio 2
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

Questo comando consente di verificare se "mystorename1" è un nome del servizio di archiviazione di Microsoft Azure esistente.

### Esempio 3
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

Questo comando consente di verificare se "MyNamespace" è un nome dello spazio dei nomi di Microsoft Azure Service Bus esistente.

## PARAMETRI

### -Nome
Specifica il nome dell'account del servizio o dello spazio di archiviazione da testare.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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

### -Servizio
Specifica di testare un account del servizio esistente.

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusNamespace
Specifica di testare uno spazio dei nomi di Service Bus esistente.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Spazio di archiviazione
Specifica di testare un account di archiviazione esistente.

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sito Web
Specifica di testare un sito Web esistente.

```yaml
Type: SwitchParameter
Parameter Sets: Website
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

## OUTPUT

## Note
* node-dev, php-dev, python-dev

## COLLEGAMENTI CORRELATI

