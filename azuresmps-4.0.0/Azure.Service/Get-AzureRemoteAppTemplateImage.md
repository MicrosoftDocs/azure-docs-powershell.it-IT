---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030041"
---
# Get-AzureRemoteAppTemplateImage

## Sinossi
Recupera informazioni sulle immagini di modelli RemoteApp di Azure.

## SINTASSI

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRemoteAppTemplateImage** recupera informazioni sulle immagini di modelli RemoteApp di Azure in Microsoft Azure.
Questo cmdlet restituisce un oggetto che contiene informazioni su un'immagine del modello specificata.
Se non viene specificata un'immagine del modello, vengono recuperate le informazioni relative a tutte le immagini del modello nell'abbonamento corrente.

## ESEMPI

### Esempio 1: ottenere un elenco di tutte le immagini dei modelli
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

Questo comando restituisce l'elenco di tutte le immagini modello.

### Esempio 2: recuperare informazioni su un'immagine del modello specificata
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

Questo comando recupera le informazioni sull'immagine del modello denominata ContosoApps.

## PARAMETRI

### -ImageName
Specifica il nome di un'immagine del modello RemoteApp di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
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

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppStartMenuProgram](./Get-AzureRemoteAppStartMenuProgram.md)


