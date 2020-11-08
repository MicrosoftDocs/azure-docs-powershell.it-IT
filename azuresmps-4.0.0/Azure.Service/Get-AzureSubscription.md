---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023495"
---
# Get-AzureSubscription

## Sinossi
Ottiene abbonamenti Azure in account Azure.

## SINTASSI

### ByName (impostazione predefinita)
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ById
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Predefinita
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Corrente
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureSubscription** ottiene le sottoscrizioni nell'account di Azure.
Puoi usare questo cmdlet per ottenere informazioni sull'abbonamento e per reindirizzare l'abbonamento ad altri cmdlet.

**Get-AzureSubscription** richiede l'accesso agli account di Azure.
Prima di eseguire **Get-AzureSubscription** , è necessario eseguire il cmdlet **Add-AzureAccount** o i cmdlet che scaricano e installano un file di impostazioni di pubblicazione ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.

Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

## ESEMPI

### Esempio 1: ottenere tutte le sottoscrizioni
```
C:\PS>Get-AzureSubscription
```

Questo comando consente di ottenere tutte le sottoscrizioni nell'account.

### Esempio 2: ottenere un abbonamento per nome
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

Questo comando ottiene solo l'abbonamento "MyProdSubsciption".

### Esempio 3: ottenere l'abbonamento predefinito
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

Questo comando ottiene solo il nome dell'abbonamento predefinito.
Il comando ottiene prima di tutto l'abbonamento e quindi usa il metodo dot per ottenere la proprietà **subscriptionname** dell'abbonamento.

### Esempio 4: ottenere le proprietà di sottoscrizione selezionate
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

Questo comando restituisce un elenco con il nome e il certificato della sottoscrizione corrente.
Usa un comando **Get-AzureSubscription** per ottenere l'abbonamento corrente.
Quindi convoglia l'abbonamento a un comando **Format-List** che visualizza le proprietà selezionate in un elenco.

### Esempio 5: usare un file di dati alternativo per l'abbonamento
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

Questo comando ottiene gli abbonamenti dal file di dati dell'abbonamento C:\Temp\MySubscriptions.xml.
Usa il parametro **SubscriptionDataFile** se hai specificato un file di dati di sottoscrizione alternativo quando hai eseguito i cmdlet **Add-AzureAccount** o **Import-PublishSettingsFile** .

## PARAMETRI

### -Current
Ottiene solo l'abbonamento corrente, ovvero l'abbonamento designato come "corrente". Per impostazione predefinita, **Get-AzureSubscription** ottiene tutte le sottoscrizioni degli account di Azure.
Per designare un abbonamento come "corrente", usa il parametro **Current** del cmdlet **Select-AzureSubscription** .

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Impostazione predefinita
Ottiene solo l'abbonamento predefinito, ovvero l'abbonamento designato come "predefinito". Per impostazione predefinita, **Get-AzureSubscription** ottiene tutte le sottoscrizioni degli account di Azure.
Per designare un abbonamento come "predefinito", usare il parametro **predefinito** del cmdlet **Select-AzureSubscription** .

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtendedDetails
Restituisce le informazioni sulle quote per l'abbonamento, oltre alle impostazioni standard.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet. Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

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

### -SubscriptionId
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subscriptionname
Ottiene solo l'abbonamento specificato.
Immettere il nome dell'abbonamento.
Il valore fa distinzione tra maiuscole e minuscole.
I caratteri jolly non sono supportati.
Per impostazione predefinita, **Get-AzureSubscription** ottiene tutte le sottoscrizioni degli account di Azure.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
È possibile reindirizzare l'input alla proprietà **subscriptionname** per nome, ma non per valore.

## OUTPUT

### Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureSubscription

## Note
* Get-AzureSubscription ottiene i dati dal file di dati dell'abbonamento creato dai cmdlet **Add-AzureAccount** e **Import-PublishSettingsFile** .

## COLLEGAMENTI CORRELATI

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Set-AzureSubscription](./Set-AzureSubscription.md)


