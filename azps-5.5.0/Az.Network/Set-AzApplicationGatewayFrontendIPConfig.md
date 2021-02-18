---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202478"
---
# Set-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Modifica una configurazione dell'indirizzo IP front-end.

## SINTASSI

### SetByResourceId
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzApplicationGatewayFrontendIPConfig** aggiorna una configurazione IP front-end.
Un gateway applicazione supporta due tipi di indirizzi IP front-end: 
- Indirizzi IP pubblici
- Indirizzi IP privati per i quali la configurazione usa il bilanciamento del carico interno (ILB, Internal Load Balancing) Un gateway di applicazione può avere al massimo un indirizzo IP pubblico e un indirizzo IP privato.
Un indirizzo IP pubblico e un indirizzo IP privato devono essere aggiunti separatamente come indirizzi IP front-end.

## ESEMPI

### Esempio 1: Impostare un INDIRIZZO IP pubblico come IP front-end di un gateway applicazioni
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

Il primo comando crea un oggetto indirizzo IP pubblico e lo archivia nella $PublicIp variabile.
Il secondo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw variabile.
Il terzo comando aggiorna la configurazione IP front-end denominata FrontEndIp01 per il gateway in $AppGw, usando l'indirizzo archiviato in $PublicIp.

### Esempio 2: Impostare un IP privato statico come indirizzo IP front-end di un gateway applicazioni
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Il primo comando ottiene una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e la archivia nella $VNet variabile.
Il secondo comando ottiene una configurazione subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet locale.
Il terzo comando recupera il gateway applicazione denominato ApplicationGateway01, che appartiene al gruppo di risorse denominato ResourceGroup01, e lo archivia nella variabile $AppGw risorsa.
Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet del secondo comando e l'indirizzo IP privato 10.0.1.1.

### Esempio 3: Impostare un IP privato dinamico come indirizzo IP front-end di un gateway applicazioni
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

Il primo comando ottiene una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e la archivia nella $VNet variabile.
Il secondo comando ottiene una configurazione subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet locale.
Il terzo comando recupera il gateway applicazione denominato ApplicationGateway01, che appartiene al gruppo di risorse denominato ResourceGroup01, e lo archivia nella variabile $AppGw risorsa.
Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet dal secondo comando.

## PARAMETERS

### -ApplicationGateway
Specifica un oggetto gateway applicazione in cui modificare la configurazione IP front-end.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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
Specifica il nome della configurazione IP front-end modificata da questo cmdlet.

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
Specifica l'indirizzo IP privato.
Se specificato, l'indirizzo IP viene allocato staticamente dalla subnet.

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
Specifica l'indirizzo IP pubblico.

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
Specifica l'ID dell'indirizzo IP pubblico.

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
Specifica la subnet utilizzata dal gateway applicazioni.
Specificare questo parametro se il gateway usa un indirizzo IP privato.
Se è *specificato l'indirizzo PrivateIPAddress,* dovrebbe appartenere alla subnet.
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
Specifica l'ID subnet.
Specificare questo parametro se il gateway usa un indirizzo IP privato.
Se si specifica il parametro *PrivateIPAddress,* questo deve appartenere alla subnet.
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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[New-AzApplicationGatewayFrontendIPConfig](./New-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)


