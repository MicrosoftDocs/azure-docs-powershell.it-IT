---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030014"
---
# Get-AzureStorSimpleAccessControlRecord

## Sinossi
Ottiene i record di controllo di accesso in una configurazione di servizio.

## SINTASSI

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorSimpleAccessControlRecord** ottiene i record di controllo di accesso nella configurazione del servizio di gestione di StorSimple.
Questo cmdlet consente di ottenere tutti i record o un record denominato.

I record di controllo di Access sono contenitori di parametri dell'iniziatore iSCSI.
Questi parametri specificano quali iniziatori possono accedere a un volume.
Quando un iniziatore iSCSI cerca di connettersi a un volume, l'appliance controlla i record di controllo di accesso assegnati al volume.
Se i parametri degli iniziatori iSCSI corrispondono a una delle voci di un record di controllo di Access mappato a tale volume, l'iniziatore iSCSI può connettersi.

## ESEMPI

### Esempio 1: ottenere tutti i record di controllo di accesso
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

Questo comando consente di ottenere tutti i record di controllo di Access.

### Esempio 2: ottenere un record di controllo di accesso specifico
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

Questo comando ottiene il record di controllo di accesso denominato Acr11.

## PARAMETRI

### -ACRName
Specifica il nome di un record di controllo di Access da ottenere.

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

### AccessControlRecord, IList\<AccessControlRecord\>
Questo cmdlet restituisce un oggetto **AccessControlRecord** o un **oggetto \<AccessControlRecord\> IList** .
Un oggetto **AccessControlRecord** contiene i campi seguenti: 

- **GlobalId** ( **stringa** ) 
- **Initiatorname** ( **String** ) 
- **InstanceID** ( **String** ) 
- **Nome** ( **stringa** ) 
- **OperationInProgress** ( **OperationInProgress** ) 
- **VolumeCount** ( **int** )

## Note

## COLLEGAMENTI CORRELATI

[New-AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Remove-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)


