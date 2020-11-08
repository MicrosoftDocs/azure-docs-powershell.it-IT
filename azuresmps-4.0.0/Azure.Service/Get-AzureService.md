---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029771"
---
# Get-AzureService

## Sinossi
Restituisce un oggetto con le informazioni sui servizi cloud per l'abbonamento corrente.

## SINTASSI

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureService** restituisce un oggetto List con tutti i servizi cloud di Azure associati alla sottoscrizione corrente.
Se specifichi il parametro *ServiceName* , **Get-AzureService** restituirà informazioni solo sul servizio corrispondente.

## ESEMPI

### Esempio 1: ottenere informazioni su tutti i servizi
```
PS C:\> Get-AzureService
```

Questo comando restituisce un oggetto che contiene informazioni su tutti i servizi di Azure associati alla sottoscrizione corrente.

### Esempio 2: ottenere informazioni su un servizio specificato
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

Questo comando restituisce informazioni sul servizio $MySvc.

### Esempio 3: visualizzare i metodi e le proprietà disponibili
```
PS C:\> Get-AzureService | Get-Member
```

Questo comando Visualizza le proprietà e i metodi disponibili nel cmdlet **Get-AzureService** .

## PARAMETRI

### -InformationAction
Specifica il modo in cui questo cmdlet risponde a un evento informativo.

I valori accettabili per questo parametro sono i seguenti:

- Continuare
- Ignora
- Informarsi
- SilentlyContinue
- Stop
- Sospensione

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifica una variabile di informazioni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

### -ServiceName
Specifica il nome di un servizio in cui restituire le informazioni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### HostedServiceContext

## Note

## COLLEGAMENTI CORRELATI

[New-AzureService](./New-AzureService.md)

[Set-AzureService](./Set-AzureService.md)


