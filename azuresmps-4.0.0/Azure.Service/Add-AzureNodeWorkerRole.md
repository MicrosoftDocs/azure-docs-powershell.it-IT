---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029851"
---
# Add-AzureNodeWorkerRole

## Sinossi
Crea i file e le cartelle necessari per un'applicazione di Node.js ospitata nel cloud tramite node.exe

## SINTASSI

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **Add-AzureNodeWorkerRole** crea i file e le cartelle necessari, a volte definiti come ponteggi, perché un'applicazione Node.js sia ospitata nel cloud tramite node.exe.

## ESEMPI

### Esempio 1: ruolo di lavoratore a istanza singola
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

Questo esempio aggiunge le impalcature per un singolo ruolo di lavoro denominato **MyWorkerRole** all'applicazione corrente.

### Esempio 2: ruolo di lavoro più istanze
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

Questo esempio aggiunge le impalcature per un singolo ruolo di lavoro denominato **MyWorkerRole** all'applicazione corrente, con un conteggio delle istanze del ruolo di 2.

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
Il valore determina il nome della cartella che contiene le impalcature per il servizio di node.js ospitate nel ruolo di lavoro.
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

[Add-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


