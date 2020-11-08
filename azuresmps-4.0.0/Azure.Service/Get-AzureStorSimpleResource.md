---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023512"
---
# Get-AzureStorSimpleResource

## Sinossi
Ottiene tutte le risorse create.

## SINTASSI

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorSimpleResource** ottiene tutte le risorse create con Azure Portal.
Il cmdlet ottiene i dettagli che è possibile usare per connettersi alle risorse.

## ESEMPI

### Esempio 1: ottenere tutte le risorse
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

Questo comando consente di ottenere tutte le risorse create.
In questo esempio sono disponibili tre risorse.

### Esempio 2: ottenere una risorsa usando il relativo nome
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

Questo comando consente di ottenere la risorsa denominata Contoso63-Tsqa.

### Esempio 3: tentativo di ottenere una risorsa inesistente
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

Questo comando tenta di ottenere la risorsa denominata Contoso64-Tsqa.
Non esiste una risorsa con questo nome.
Questo esempio non restituisce alcuna risorsa.

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

### -ResourceName
Specifica il nome della risorsa ottenuta da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### IEnumerable \<ResourceCredentials\> , ResourceCredentials
Questo cmdlet restituisce gli oggetti **ResourceCredentials** che contengono le proprietà seguenti: 

- **ResourceName**
- **ResouceId**
- **ResourceState**

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)

[Selezionare-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


