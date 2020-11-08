---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023758"
---
# Set-AzureNetworkSecurityRule

## Sinossi
Aggiunge o modifica una regola di sicurezza di rete in un gruppo di sicurezza di rete.

## SINTASSI

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureNetworkSecurityRule** aggiunge o modifica una regola di sicurezza della rete Azure in un gruppo di sicurezza di rete.

## ESEMPI

## PARAMETRI

### -Azione
Specifica l'azione per una regola di sicurezza di rete.
I valori validi sono: Allow e Deny.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddressPrefix
Specifica l'indirizzo CIDR (classe Interdomain Routing) dell'intervallo IP di destinazione per la regola di sicurezza della rete.
Un asterisco (*) specifica un indirizzo IP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
Specifica un intervallo di porte di destinazione per la regola di sicurezza della rete.
I valori validi sono costituiti da numeri interi compresi tra 0 e 65535.
Puoi specificare un singolo valore o specificare un intervallo nel formato LowerNumber-HigherNumber.
Un trattino separa i due valori.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome della regola di sicurezza della rete che questo cmdlet aggiunge o modifica.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkSecurityGroup
Specifica il gruppo di sicurezza di rete modificato da questo cmdlet.
Per ottenere un oggetto **INetworkSecurityGroup** , usa il cmdlet Get-AzureNetworkSecurityGroup.

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Priorità
Specifica la priorità per la regola di sicurezza della rete.
I valori validi sono: numeri interi da 100 a 4096.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet. Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

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

### -Protocollo
Specifica il protocollo per la regola di sicurezza della rete.
I valori validi sono: 

- TCP 
- UDP 
- *

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
Specifica l'indirizzo CIDR dell'intervallo IP di origine per la regola di sicurezza della rete.
Un asterisco (*) specifica un indirizzo IP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
Specifica un intervallo della porta di origine per la regola di sicurezza della rete.
I valori validi sono costituiti da numeri interi compresi tra 0 e 65535.
Puoi specificare un singolo valore o specificare un intervallo nel formato LowerNumber-HigherNumber.
Un trattino separa i due valori.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digitare
Specifica il tipo di connessione per la regola di sicurezza della rete.
I valori validi sono: in ingresso e in uscita.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[Remove-AzureNetworkSecurityRule](./Remove-AzureNetworkSecurityRule.md)


