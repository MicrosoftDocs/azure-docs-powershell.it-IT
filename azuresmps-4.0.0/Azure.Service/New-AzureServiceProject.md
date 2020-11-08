---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029680"
---
# New-AzureServiceProject

## Sinossi
Crea i file e la configurazione necessari per un nuovo servizio.

## SINTASSI

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **New-AzureServiceProject** crea i file e la configurazione necessari per un nuovo servizio Azure nella directory corrente.

## ESEMPI

### Esempio 1: creare ponteggi per un servizio
```
PS C:\> New-AzureServiceProject MyService1
```

Questo esempio crea ponteggi per un nuovo servizio Azure denominato MyService1 nella directory corrente.

## PARAMETRI

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

### -ServiceName
Specifica il nome del servizio.
Determina la prima sezione del nome host per il servizio (ad esempio, name.cloudapp.net) e la directory che conterrà il servizio.
Il nome può contenere solo lettere, cifre e il carattere di trattino (-).

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[Add-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[Publish-AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


