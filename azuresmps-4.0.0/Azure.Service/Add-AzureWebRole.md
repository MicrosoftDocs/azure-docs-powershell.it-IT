---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023669"
---
# Add-AzureWebRole

## Sinossi
Aggiunge un ruolo di lavoro Web.

## SINTASSI

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **Add-AzureWebRole** aggiunge un ruolo di lavoro Web.

## ESEMPI

### Esempio 1: aggiungere un ruolo predefinito
```
PS C:\> Add-AzureWebRole
```

Questo comando aggiunge il ruolo Web con la configurazione predefinita di Webrole1 come nome e una singola istanza.

### Esempio 2: aggiungere un ruolo con un nome
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

Questo comando aggiunge un singolo ruolo Web denominato MyWebRole all'applicazione corrente.

### Esempio 3: aggiungere un ruolo con un nome e un conteggio delle istanze
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

Questo comando aggiunge un ruolo Web denominato MyWebRole all'applicazione corrente.
Il cmdlet ha un conteggio delle istanze del ruolo di 2.

### Esempio 4: aggiungere un ruolo con un nome e un modello
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

Questo comando aggiunge un singolo ruolo Web denominato MyWebRole all'applicazione corrente.
Il comando specifica una cartella denominata MyWebTemplateFolder come modello di ponteggi.

## PARAMETRI

### -Istanze
Specifica il numero di istanze.

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
Specifica la cartella modello.

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

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)

[New-AzureRoleTemplate](./New-AzureRoleTemplate.md)


