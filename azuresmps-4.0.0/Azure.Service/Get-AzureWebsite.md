---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029736"
---
# Get-AzureWebsite

## Sinossi
Ottiene i siti Web di Azure nell'abbonamento corrente.

## SINTASSI

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureWebsite** ottiene le informazioni sui siti Web di Azure nell'abbonamento corrente.

Per impostazione predefinita, **Get-AzureWebsite** ottiene tutti i siti Web di Azure nell'abbonamento corrente e restituisce un oggetto che fornisce informazioni di base sui siti.
Quando si usa il parametro *Name* , **Get-AzureWebsite** restituisce un oggetto con informazioni estese, inclusi i dettagli della configurazione.

L'abbonamento corrente è l'abbonamento designato come "Current". Per trovare l'abbonamento corrente, usa il parametro *Current* del cmdlet [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) .
Per cambiare l'abbonamento corrente, usare il cmdlet [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) .

Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

## ESEMPI

### Esempio 1: ottenere tutti i siti Web nell'abbonamento
```
PS C:\> Get-AzureWebsite
```

Questo comando consente di ottenere tutti i siti Web di Azure nell'abbonamento corrente.

### Esempio 2: ottenere un sito Web per nome
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

Questo comando consente di ottenere informazioni dettagliate sul sito Web di ContosoWeb Azure, incluse le informazioni di configurazione.
Quando usi il parametro *Name* , **Get-AzureWebsite** restituisce un oggetto **SiteWithConfig** con informazioni estese sul sito Web.

### Esempio 3: ottenere informazioni dettagliate su tutti i siti Web
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

Questo comando consente di ottenere informazioni dettagliate su tutti i siti Web nell'abbonamento.
Usa un comando **Get-AzureWebsite** per ottenere tutti i siti Web e quindi usa il cmdlet **foreach-Object** per ottenere ogni sito Web per nome.

### Esempio 4: ottenere informazioni su uno slot di distribuzione
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

Questo comando ottiene lo slot di distribuzione della gestione temporanea del sito Web ContosoWeb.
Gli slot di distribuzione consentono di testare versioni diverse del sito Web di Azure senza rilasciarle al pubblico.

### Esempio 5: ottenere istanze del sito Web
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

I comandi in questo esempio usano la proprietà instances di un sito Web di Azure per ottenere informazioni sulle istanze del sito Web attualmente in uso.
La proprietà **instances** è stata aggiunta all'oggetto **SiteWithConfig** nella versione 0.8.3 del modulo Azure.

Il primo comando consente di ottenere gli ID di istanza di tutte le istanze attualmente in uso di un sito Web.
Il secondo comando consente di ottenere il numero di istanze in uso del sito Web.
Puoi usare la proprietà **count** in qualsiasi matrice.

## PARAMETRI

### -Nome
Ottiene informazioni dettagliate sulla configurazione del sito Web specificato.
Immettere il nome di un sito Web nell'abbonamento.
Per impostazione predefinita, **Get-AzureWebsite** ottiene tutti i siti Web nell'abbonamento corrente.
Il valore *Name* non supporta i caratteri jolly.

```yaml
Type: String
Parameter Sets: (All)
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

### -Slot
Ottiene lo slot di distribuzione specificato del sito Web.
Immettere il nome dello slot, ad esempio "Staging" o "Production".
Per altre informazioni sugli slot di distribuzione, vedere distribuzione a fasi nei siti Web di Microsoft Azure https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .
Per aggiungere uno slot di distribuzione a un sito Web Azure esistente, usare il cmdlet Set-AzureWebsite.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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
È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.

## OUTPUT

### Microsoft. WindowsAzure. Commands. Utilities. Web. Services. webentities. site
Per impostazione predefinita, **Get-AzureWebsite** restituisce una matrice di oggetti **sito** .

### Microsoft. WindowsAzure. Commands. Utilities. Web. Services. webentities. SiteWithConfig
Quando usi il parametro *Name* , **Get-AzureWebsite** restituisce un oggetto **SiteWithConfig** .

## Note

## COLLEGAMENTI CORRELATI

[New-AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start-AzureWebsite](./Start-AzureWebsite.md)

[Stop-AzureWebsite](./Stop-AzureWebsite.md)

[Mostra-AzureWebsite](./Show-AzureWebsite.md)


