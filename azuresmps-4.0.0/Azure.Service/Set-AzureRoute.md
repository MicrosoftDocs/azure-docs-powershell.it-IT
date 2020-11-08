---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023781"
---
# Set-AzureRoute

## Sinossi
Crea una route in una tabella di route.

## SINTASSI

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRoute** crea una route in una tabella di route.
La nuova route ha effetto quasi immediatamente sulle macchine virtuali associate alla tabella route.

## ESEMPI

### Esempio 1: aggiungere una route hop Next appliance virtuale
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

Questo comando crea una tabella di route denominata ApplianceRouteTable nella posizione specificata.
Il comando passa la tabella route al cmdlet Current.
Il cmdlet corrente aggiunge una route denominata ApplianceRoute03, che è un tipo di hop successivo di VirtualAppliance.
Il comando specifica l'indirizzo IP dell'hop successivo e il prefisso dell'indirizzo per la route.

### Esempio 2: aggiungere una route hop Next Internet
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

Questo comando consente di ottenere una tabella di route denominata ApplianceRouteTable.
Il comando passa la tabella route al cmdlet Current.
Il cmdlet corrente aggiunge una route denominata InternetRoute, che è un tipo di hop successivo Internet.
Il comando specifica il prefisso dell'indirizzo per la route.

## PARAMETRI

### -AddressPrefix
Specifica un prefisso di indirizzo per la nuova route.

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

### -NextHopIpAddress
Specifica l'indirizzo IP dell'appliance che rappresenta l'hop successivo per il traffico che usa questa route.
Specificare questo valore solo se si specifica un valore di VirtualAppliance per il parametro *NextHopType* .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NextHopType
Specifica il tipo di hop successivo per il traffico che usa questa route.
I valori validi sono: 

- VPNGateway
- VNETLocal
- Internet
- VirtualAppliance
- Null

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

### -RouteName
Specifica un nome per la nuova route aggiunta da questo cmdlet.

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

### -RouteTable
Specifica la tabella di route a cui questo cmdlet aggiunge la nuova route.

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Remove-AzureRoute](./Remove-AzureRoute.md)


