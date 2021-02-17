---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206851"
---
# New-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Crea una configurazione IP front-end per un gateway applicazioni.

## SINTASSI

### SetByResourceId
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzApplicationGatewayFrontendIPConfig crea** una configurazione IP front-end per un gateway applicazione di Azure.
Un gateway applicazione supporta due tipi di configurazione IP front-end: 
- Indirizzi IP pubblici: indirizzi IP privati che usano il bilanciamento del carico interno.
 Un gateway applicazione può avere al massimo un indirizzo IP pubblico e uno privato.
L'indirizzo IP pubblico e l'indirizzo IP privato devono essere aggiunti separatamente come indirizzi IP front-end.

## ESEMPI

### Esempio 1: Creare una configurazione IP front-end usando un oggetto risorsa IP pubblico
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

Il primo comando crea un oggetto risorsa IP pubblica e lo archivia nella $PublicIP variabile.
Il secondo comando usa $PublicIP per creare una nuova configurazione IP front-end denominata FrontEndIP01 e la archivia nella variabile $FrontEnd front-end.

### Esempio 2: Creare un IP privato statico come indirizzo IP front-end
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Il primo comando ottiene una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e la archivia nella $VNet variabile.
Il secondo comando ottiene una configurazione subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet locale.
Il terzo comando crea una configurazione IP front-end denominata FrontEndIP02 usando $Subnet dal secondo comando e l'indirizzo IP privato 10.0.1.1, quindi la archivia nella variabile $FrontEnd.

### Esempio 3: Creare un IP privato dinamico come indirizzo IP front-end
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

Il primo comando ottiene una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e la archivia nella $VNet variabile.
Il secondo comando ottiene una configurazione subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet locale.
Il terzo comando crea una configurazione IP front-end denominata FrontEndIP03 usando $Subnet dal secondo comando e la archivia nella $FrontEnd variabile.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifica il nome della configurazione IP front-end creata da questo cmdlet.

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

### -PrivateIPAddress
Specifica l'indirizzo IP privato che questo cmdlet associa all'indirizzo IP front-end del gateway applicazione.
Può essere specificato solo se è specificata una subnet.
Questo INDIRIZZO IP è allocato staticamente dalla subnet.

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

### -PrivateLinkConfiguration
PrivateLinkConfiguration

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfigurationId
PrivateLinkConfigurationId

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddress
Specifica l'oggetto indirizzo IP pubblico che questo cmdlet associa all'indirizzo IP front-end del gateway applicazione.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
Specifica l'ID dell'indirizzo IP pubblico che questo cmdlet associa all'INDIRIZZO IP front-end del gateway applicazione.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
Specifica l'oggetto subnet associato dal cmdlet all'indirizzo IP front-end del gateway applicazione.
Se si specifica questo parametro, il gateway usa un indirizzo IP privato.
Se è specificato il parametro *PrivateIPAddress,* deve appartenere alla subnet specificata da questo parametro.
Se *privateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene scelto dinamicamente come indirizzo IP front-end del gateway applicazione.

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Specifica l'ID subnet a cui questo cmdlet associa la configurazione IP front-end del gateway applicazione.
Se si specifica il *parametro Subnet,* il gateway usa un indirizzo IP privato.
Se si *specifica il parametro PrivateIPAddress,* deve appartenere alla subnet specificata da *Subnet.*
Se *privateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene scelto dinamicamente come indirizzo IP front-end del gateway applicazione.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


