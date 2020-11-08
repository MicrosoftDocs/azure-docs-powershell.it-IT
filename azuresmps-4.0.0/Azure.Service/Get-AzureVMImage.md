---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029994"
---
# Get-AzureVMImage

## Sinossi
Ottiene le proprietà in uno o un elenco di sistemi operativi o un'immagine della macchina virtuale nel repository di immagini.

## SINTASSI

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureVMImage** ottiene le proprietà in uno o un elenco di sistemi operativi o un'immagine della macchina virtuale nel repository di immagini.
Il cmdlet restituisce informazioni per tutte le immagini del repository o su un'immagine specifica se è disponibile il nome dell'immagine.

## ESEMPI

### Esempio 1: ottenere un oggetto immagine specifico dal repository di immagini corrente.
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

Questo comando ottiene l'oggetto Image denominato Image001 dal repository di immagini corrente.

### Esempio 2: ottenere tutte le immagini dal repository di immagini corrente
```
PS C:\> Get-AzureVMImage
```

Questo comando recupera tutte le immagini dal repository di immagini corrente.

### Esempio 3: impostare il contesto dell'abbonamento e quindi ottenere tutte le immagini
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

Questo comando imposta il contesto di sottoscrizione e recupera tutte le immagini dal repository di immagini.

## PARAMETRI

### -ImageName
Specifica il nome del sistema operativo o dell'immagine della macchina virtuale nel repository di immagini.
Se non specifichi questo parametro, vengono restituite tutte le immagini.

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

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Remove-AzureVMImage](./Remove-AzureVMImage.md)

[Salva-AzureVMImage](./Save-AzureVMImage.md)

[Update-AzureVMImage](./Update-AzureVMImage.md)


