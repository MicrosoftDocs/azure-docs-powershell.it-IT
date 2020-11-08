---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029852"
---
# Add-AzurePHPWebRole

## Sinossi
Crea i file e la configurazione necessari per un'applicazione PHP.

## SINTASSI

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **Add-AzurePHPWebRole** crea i file e la configurazione, a volte definiti ponteggi, per un'applicazione php che verrà ospitata in Azure tramite IIS.

## ESEMPI

### Esempio 1: aggiungere un ruolo Web usando i valori predefiniti
```
PS C:\> Add-AzurePHPWebRole
```

Questo esempio aggiunge i file e la configurazione necessari per il nuovo ruolo Web usando i valori predefiniti di un servizio denominato "WebRole1" con 1 istanza.

### Esempio 2: aggiungere un ruolo Web con più istanze
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

Questo esempio aggiunge i file e la configurazione necessari per un nuovo ruolo Web all'applicazione corrente, usando il nome "MyWebRole" e un conteggio delle istanze del ruolo di 2.

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
Il nome determina il nome della directory che contiene i file e la configurazione necessari per l'applicazione PHP.
Il valore predefinito è WebRole #, dove # rappresenta il numero di ruoli Web nel servizio.

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

[Add-AzurePHPWorkerRole](./Add-AzurePHPWorkerRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


