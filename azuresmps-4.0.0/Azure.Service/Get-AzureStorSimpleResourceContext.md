---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030011"
---
# Get-AzureStorSimpleResourceContext

## Sinossi
Ottiene il contesto della risorsa corrente.

## SINTASSI

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorSimpleResourceContext** ottiene il contesto della risorsa corrente.

## ESEMPI

### Esempio 1: ottenere il contesto corrente
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

Il primo comando imposta il contesto corrente come la risorsa denominata Contoso63-Tsqa usando il cmdlet **Select-AzureStorSimpleResource** .

Il secondo comando ottiene il contesto della risorsa corrente.

### Esempio 2: tentativo di ottenere il contesto corrente
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

Questo comando ottiene il contesto corrente.
In questo esempio non è stato impostato alcun contesto.
Il comando restituisce un messaggio che spiega il problema.

## PARAMETRI

### -Profile
Specifica un profilo Azure.

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

### Nessuno

## OUTPUT

### StorSimpleResourceContext
Questo cmdlet restituisce un oggetto **ResourceContext** .

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Selezionare-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


