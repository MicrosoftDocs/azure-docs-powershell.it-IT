---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029797"
---
# Get-AzureMediaServicesAccount

## Sinossi
Ottiene gli account di servizi di Azure Media disponibili.

**Nota:** Questa versione è deprecata, vedere la [versione più recente](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).

## SINTASSI

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Per elencare tutti gli account, usare il `Get-AzureMediaServicesAccount` cmdlet.
Per ottenere informazioni più dettagliate su un account specifico, usare il `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.

## ESEMPI

### Esempio 1: elencare tutti gli account di servizi multimediali
```
PS C:\> Get-AzureMediaServicesAccount
```

Questo comando elenca tutti gli account di servizi multimediali disponibili.

### Esempio 2: ottenere informazioni dettagliate su un account di servizi multimediali
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

Questo comando Visualizza le proprietà di un account di servizi multimediali.

## PARAMETRI

### -Nome
Nome dell'account dei servizi multimediali.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Come usare Azure PowerShell per i servizi multimediali](https://go.microsoft.com/fwlink/?LinkId=324179)


