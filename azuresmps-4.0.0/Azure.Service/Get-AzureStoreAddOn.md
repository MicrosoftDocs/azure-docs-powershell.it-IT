---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023505"
---
# Get-AzureStoreAddOn

## Sinossi
Ottiene i componenti aggiuntivi di Azure Store disponibili.

## SINTASSI

### ListAvailable
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Getaddon
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Ottiene tutti i componenti aggiuntivi disponibili per l'acquisto da Azure Store oppure ottiene le istanze del componente aggiuntivo esistenti per l'abbonamento corrente.

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzureStoreAddOn
```

Questo esempio consente di ottenere tutte le istanze del componente aggiuntivo acquistate per la sottoscrizione corrente.

### Esempio 2
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

Questo esempio consente di ottenere tutti i componenti aggiuntivi disponibili per l'acquisto in Stati Uniti da Azure Store.

### Esempio 3
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

Questo esempio ottiene un componente aggiuntivo denominato AddOn dall'istanza del componente aggiuntivo acquistata nell'abbonamento corrente.

## PARAMETRI

### -Paese
Se specificato, restituisce solo le istanze del componente aggiuntivo Azure Store disponibili nel paese specificato.
Il valore predefinito è "US".

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ListAvailable
Se specificato, ottiene i componenti aggiuntivi disponibili per l'acquisto da Azure Store.

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Restituisce il componente aggiuntivo che corrisponde al nome specificato.

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
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

[New-AzureStoreAddOn](./New-AzureStoreAddOn.md)

[Remove-AzureStoreAddOn](./Remove-AzureStoreAddOn.md)

[Set-AzureStoreAddOn](./Set-AzureStoreAddOn.md)


