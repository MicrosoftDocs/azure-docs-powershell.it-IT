---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029849"
---
# Add-AzurePHPWorkerRole

## Sinossi
Crea i file e la configurazione necessari per un'applicazione PHP che verrà ospitata in Azure tramite php.exe.

## SINTASSI

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Crea i file e la configurazione necessari, a volte definiti come ponteggi, per un'applicazione PHP che verrà ospitata in Azure tramite php.exe.

## ESEMPI

### Esempio 1: creare un ruolo di lavoro con una singola istanza
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

Questo esempio aggiunge i file e la configurazione necessari per un singolo ruolo di lavoro denominato MyWorkerRole all'applicazione corrente.

### Esempio 2: creare un ruolo di lavoro con più istanze
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

Questo esempio aggiunge i file e la configurazione necessari per un nuovo ruolo di lavoro all'applicazione corrente, usando il nome MyWorkerRole con un conteggio delle istanze del ruolo di 2.

## PARAMETRI

### -Istanze
Specifica il numero di istanze di ruolo per il ruolo di lavoro.
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
Specifica il nome del ruolo di lavoro.
Il nome determina il nome della cartella che contiene i file e la configurazione necessari per il servizio PHP ospitato nel ruolo di lavoro.
Il valore predefinito è WorkerRole1.

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

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Add-AzurePHPWebRole](./Add-AzurePHPWebRole.md)


