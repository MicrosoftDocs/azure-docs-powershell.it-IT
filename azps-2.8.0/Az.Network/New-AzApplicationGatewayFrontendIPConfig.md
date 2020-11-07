---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 2ffd1d0a0ab3542636a2deec134d5bd233fd8ffa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853034"
---
# New-AzApplicationGatewayFrontendIPConfig

## Sinossi
Crea una configurazione IP front-end per un gateway dell'applicazione.

## SINTASSI

### SetByResourceId
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzApplicationGatewayFrontendIPConfig** crea una configurazione IP front-end per un gateway dell'applicazione Azure.
Un gateway applicazione supporta due tipi di configurazione IP front-end: 
- Indirizzi IP pubblici--indirizzi IP privati con il bilanciamento del carico interno (ILB).
 Un gateway applicazione può avere al massimo un indirizzo IP pubblico e un indirizzo IP privato.
L'indirizzo IP pubblico e l'indirizzo IP privato devono essere aggiunti separatamente come indirizzi IP front-end.

## ESEMPI

### Esempio 1: creare una configurazione IP front-end usando un oggetto risorsa IP pubblico
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

Il primo comando crea un oggetto risorsa IP pubblico e lo archivia nella variabile $PublicIP.
Il secondo comando USA $PublicIP per creare una nuova configurazione IP front-end denominata FrontEndIP01 e la archivia nella variabile $FrontEnd.

### Esempio 2: creare un IP privato statico come indirizzo IP front-end
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.
Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.
Il terzo comando crea una configurazione IP front-end denominata FrontEndIP02 usando $Subnet dal secondo comando e dall'indirizzo IP privato 10.0.1.1, quindi lo archivia nella variabile $FrontEnd.

### Esempio 3: creare un IP privato dinamico come indirizzo IP front-end
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.
Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.
Il terzo comando crea una configurazione IP front-end denominata FrontEndIP03 usando $Subnet dal secondo comando e la archivia nella variabile $FrontEnd.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome della configurazione IP front-end creata da questo cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIPAddress
Specifica l'indirizzo IP privato che questo cmdlet associa all'indirizzo IP front-end del gateway dell'applicazione.
Questa operazione può essere specificata solo se è specificata una subnet.
Questo IP viene allocato in modo statico dalla subnet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddress
Specifica l'oggetto indirizzo IP pubblico che questo cmdlet associa all'indirizzo IP front-end del gateway dell'applicazione.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
Specifica l'ID indirizzo IP pubblico che questo cmdlet associa all'IP front-end del gateway dell'applicazione.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
Specifica l'oggetto subnet che questo cmdlet associa all'indirizzo IP front-end del gateway dell'applicazione.
Se specifichi questo parametro, significa che il gateway usa un indirizzo IP privato.
Se il parametro *PrivateIPAddress* è specificato, deve appartenere alla subnet specificata da questo parametro.
Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene selezionato in modo dinamico come indirizzo IP front-end del gateway dell'applicazione.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Specifica l'ID subnet che questo cmdlet associa alla configurazione IP front-end del gateway dell'applicazione.
Se specifichi il parametro *subnet* , significa che il gateway usa un indirizzo IP privato.
Se il parametro *PrivateIPAddress* è specificato, deve appartenere alla subnet specificata dalla *Subnet*.
Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene selezionato in modo dinamico come indirizzo IP front-end del gateway dell'applicazione.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
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

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration

## Note

## COLLEGAMENTI CORRELATI

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


