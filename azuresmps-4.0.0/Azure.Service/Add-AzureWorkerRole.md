---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023668"
---
# Add-AzureWorkerRole

## Sinossi
Crea i file e la configurazione necessari per un ruolo di lavoro personalizzato.

## SINTASSI

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **Add-AzureWorkerRole** crea i file e la configurazione necessari, a volte definiti come ponteggi, per un ruolo di lavoro personalizzato.

## ESEMPI

### Esempio 1: creare un singolo ruolo di lavoro istanza
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

Questo esempio aggiunge le impalcature per un singolo ruolo di lavoro denominato MyWorkerRole all'applicazione corrente.

### Esempio 2: creare un ruolo di lavoro a più istanze
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

Questo esempio aggiunge le impalcature per un nuovo ruolo di lavoro denominato MyWorkerRole all'applicazione corrente, con un conteggio delle istanze del ruolo di 2.

### Esempio 3: creare un ruolo di lavoro con le impalcature personalizzate
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

Questo esempio crea un ruolo di lavoro con un'impalcatura personalizzata.

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
Questo valore determina il nome della cartella che contiene le impalcature per l'applicazione personalizzata che verranno ospitate nel ruolo di lavoro.
Il valore predefinito è WorkerRolenumber, dove numero è il numero di ruoli di lavoro nel servizio.

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

### -TemplateFolder
Specifica la cartella del modello di ponteggi da usare per creare il ruolo di lavoro.

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

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureWebRole](./Add-AzureWebRole.md)

[New-AzureRoleTemplate](./New-AzureRoleTemplate.md)


