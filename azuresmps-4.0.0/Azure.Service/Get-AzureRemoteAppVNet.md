---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030032"
---
# Get-AzureRemoteAppVNet

## Sinossi
Recupera informazioni sulle reti virtuali di Azure RemoteApp in Azure.

## SINTASSI

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRemoteAppVNet** recupera informazioni sulle reti virtuali di Azure RemoteApp in Microsoft Azure.
Questo cmdlet restituisce un oggetto che contiene informazioni su una rete virtuale specificata.
Se non viene specificata una rete virtuale, questo cmdlet restituisce informazioni su tutte le reti virtuali dell'abbonamento corrente.

## ESEMPI

### Esempio 1: recuperare informazioni su una rete virtuale
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

Questo comando consente di ottenere informazioni sulla rete virtuale denominata ContosoVNet.

## PARAMETRI

### -IncludeSharedKey
Indica che questo cmdlet include il valore della chiave condivisa nelle informazioni recuperate sulla rete virtuale.

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

### -VNetName
Specifica il nome della rete virtuale di Azure RemoteApp.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


