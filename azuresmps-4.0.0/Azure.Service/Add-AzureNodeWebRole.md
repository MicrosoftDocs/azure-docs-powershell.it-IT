---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029854"
---
# Add-AzureNodeWebRole

## Sinossi
Crea file e cartelle necessari per un'applicazione di Node.js.

## SINTASSI

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il **componente aggiuntivo AzureNodeWebRole** crea file e cartelle necessari, a volte definiti come ponteggi, per un'applicazione Node.js ospitata nel cloud tramite IIS.

## ESEMPI

### Esempio 1: ruolo Web istanza singola
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

Questo esempio aggiunge le impalcature per un singolo ruolo Web denominato **MyWebRole** all'applicazione corrente.

### Esempio 2: ruolo Web istanza multipla
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

Questo esempio aggiunge le impalcature per un nuovo ruolo Web denominato **MyWebRole** all'applicazione corrente, con un conteggio delle istanze del ruolo di 2.

## PARAMETRI

### -Istanze
Specifica il numero di istanze di ruolo per questo ruolo Web.
Il valore predefinito è 1.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del ruolo Web.
Determina anche il nome della directory che contiene le impalcature per l'applicazione node.js che verranno ospitate nel ruolo Web.
Il valore predefinito è WebRole #, dove # indica il numero di ruoli Web nel servizio.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

[Add-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


