---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D903741F-1D22-48FC-BFA5-6876E557EFE5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4284d34ef5151dbcd16d9ed882dcf112abbb8ea5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023450"
---
# Remove-AzureVNetConfig

## Sinossi
Elimina la configurazione di rete dall'abbonamento Azure corrente.

## SINTASSI

```
Remove-AzureVNetConfig [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureVNetConfig** consente di rimuovere tutte le impostazioni di rete virtuale dall'abbonamento Azure corrente.

## ESEMPI

### Esempio 1: rimuovere una configurazione di rete virtuale dall'abbonamento corrente
```
PS C:\> Remove-AzureVNetConfig
```

Questo comando rimuove la configurazione di rete virtuale dall'abbonamento corrente.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureVNetConfig](./Get-AzureVNetConfig.md)

[Get-AzureVNetSite](./Get-AzureVNetSite.md)

[Set-AzureVNetConfig](./Set-AzureVNetConfig.md)


