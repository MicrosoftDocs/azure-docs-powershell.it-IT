---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023777"
---
# Set-AzureServiceProject

## Sinossi
Imposta la posizione, l'abbonamento, lo slot e l'account di archiviazione predefiniti per il servizio corrente.

## SINTASSI

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureServiceProject** imposta il percorso di distribuzione, lo slot, l'account di archiviazione e l'abbonamento per il servizio corrente.
Questi valori vengono usati ogni volta che il servizio viene pubblicato nel cloud.

## ESEMPI

### Esempio 1: impostazioni di base
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

Imposta il percorso di distribuzione per il servizio nell'area Nord America centrale.
Imposta lo slot di distribuzione su Production. Imposta l'account di archiviazione che verrà usato per organizzare la definizione del servizio in myStorageAccount.
Imposta la sottoscrizione che consentirà di ospitare il servizio in abbonamento.
Ogni volta che il servizio viene pubblicato nel cloud, sarà ospitato in un centro dati nell'area nord-centrale degli Stati Uniti, che aggiornerà lo slot di distribuzione e userà l'account di sottoscrizione e archiviazione specificato.

## PARAMETRI

### -Posizione
Area geografica in cui verrà ospitato il servizio.
Questo valore viene usato ogni volta che il servizio viene pubblicato nel cloud.
I valori possibili sono: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.

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

### -PassThru
Indica che questo cmdlet restituisce un oggetto che rappresenta l'elemento in cui opera.
Per impostazione predefinita, questo cmdlet non genera alcun output.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

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

### -Slot
Slot (produzione o staging) in cui verrà ospitato il servizio.
Questo valore viene usato ogni volta che il servizio viene pubblicato nel cloud.
I valori possibili sono: produzione, staging.

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

### -Spazio di archiviazione
Account di archiviazione da usare quando si carica il pacchetto del servizio nel cloud.
Se l'account di archiviazione non esiste, verrà creato quando il servizio viene pubblicato nel cloud.

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
* node-dev, php-dev, python-dev

## COLLEGAMENTI CORRELATI

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Publish-AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


