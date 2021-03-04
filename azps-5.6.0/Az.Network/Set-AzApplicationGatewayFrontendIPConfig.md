---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 17ef06c6f91f650da95ddcbfb87b09a60c1948d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956782"
---
# <span data-ttu-id="93fe4-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="93fe4-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="93fe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="93fe4-103">Modifica una configurazione dell'indirizzo IP front-end.</span><span class="sxs-lookup"><span data-stu-id="93fe4-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="93fe4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93fe4-104">SYNTAX</span></span>

### <span data-ttu-id="93fe4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="93fe4-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93fe4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="93fe4-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93fe4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93fe4-107">DESCRIPTION</span></span>
<span data-ttu-id="93fe4-108">Il cmdlet **Set-AzApplicationGatewayFrontendIPConfig** aggiorna una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="93fe4-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="93fe4-109">Un gateway applicazione supporta due tipi di indirizzi IP front-end:</span><span class="sxs-lookup"><span data-stu-id="93fe4-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="93fe4-110">Indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="93fe4-110">Public IP addresses</span></span>
- <span data-ttu-id="93fe4-111">Indirizzi IP privati per i quali la configurazione usa il bilanciamento del carico interno (ILB, Internal Load Balancing) Un gateway di applicazione può avere al massimo un indirizzo IP pubblico e un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="93fe4-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="93fe4-112">Un indirizzo IP pubblico e un indirizzo IP privato devono essere aggiunti separatamente come indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="93fe4-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="93fe4-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93fe4-113">EXAMPLES</span></span>

### <span data-ttu-id="93fe4-114">Esempio 1: Impostare un INDIRIZZO IP pubblico come IP front-end di un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="93fe4-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="93fe4-115">Il primo comando crea un oggetto indirizzo IP pubblico e lo archivia nella $PublicIp variabile.</span><span class="sxs-lookup"><span data-stu-id="93fe4-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="93fe4-116">Il secondo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="93fe4-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="93fe4-117">Il terzo comando aggiorna la configurazione IP front-end denominata FrontEndIp01 per il gateway in $AppGw, usando l'indirizzo archiviato in $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="93fe4-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="93fe4-118">Esempio 2: Impostare un IP privato statico come indirizzo IP front-end di un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="93fe4-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="93fe4-119">Il primo comando ottiene una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e la archivia nella $VNet variabile.</span><span class="sxs-lookup"><span data-stu-id="93fe4-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="93fe4-120">Il secondo comando ottiene una configurazione subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet locale.</span><span class="sxs-lookup"><span data-stu-id="93fe4-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="93fe4-121">Il terzo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw risorsa.</span><span class="sxs-lookup"><span data-stu-id="93fe4-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="93fe4-122">Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet del secondo comando e l'indirizzo IP privato 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="93fe4-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="93fe4-123">Esempio 3: Impostare un IP privato dinamico come indirizzo IP front-end di un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="93fe4-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="93fe4-124">Il primo comando ottiene una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e la archivia nella $VNet variabile.</span><span class="sxs-lookup"><span data-stu-id="93fe4-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="93fe4-125">Il secondo comando ottiene una configurazione subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet locale.</span><span class="sxs-lookup"><span data-stu-id="93fe4-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="93fe4-126">Il terzo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw risorsa.</span><span class="sxs-lookup"><span data-stu-id="93fe4-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="93fe4-127">Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet dal secondo comando.</span><span class="sxs-lookup"><span data-stu-id="93fe4-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="93fe4-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93fe4-128">PARAMETERS</span></span>

### <span data-ttu-id="93fe4-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93fe4-129">-ApplicationGateway</span></span>
<span data-ttu-id="93fe4-130">Specifica un oggetto gateway applicazione in cui modificare la configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="93fe4-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="93fe4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93fe4-131">-DefaultProfile</span></span>
<span data-ttu-id="93fe4-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93fe4-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93fe4-133">-Name</span><span class="sxs-lookup"><span data-stu-id="93fe4-133">-Name</span></span>
<span data-ttu-id="93fe4-134">Specifica il nome della configurazione IP front-end modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93fe4-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="93fe4-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="93fe4-135">-PrivateIPAddress</span></span>
<span data-ttu-id="93fe4-136">Specifica l'indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="93fe4-136">Specifies the private IP address.</span></span>
<span data-ttu-id="93fe4-137">Se specificato, l'indirizzo IP viene allocato staticamente dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="93fe4-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="93fe4-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="93fe4-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="93fe4-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="93fe4-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="93fe4-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="93fe4-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="93fe4-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="93fe4-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="93fe4-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="93fe4-142">-PublicIPAddress</span></span>
<span data-ttu-id="93fe4-143">Specifica l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="93fe4-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="93fe4-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="93fe4-144">-PublicIPAddressId</span></span>
<span data-ttu-id="93fe4-145">Specifica l'ID dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="93fe4-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="93fe4-146">-Subnet</span><span class="sxs-lookup"><span data-stu-id="93fe4-146">-Subnet</span></span>
<span data-ttu-id="93fe4-147">Specifica la subnet utilizzata dal gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="93fe4-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="93fe4-148">Specificare questo parametro se il gateway usa un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="93fe4-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="93fe4-149">Se è *specificato l'indirizzo PrivateIPAddress,* dovrebbe appartenere alla subnet.</span><span class="sxs-lookup"><span data-stu-id="93fe4-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="93fe4-150">Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene scelto dinamicamente come indirizzo IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="93fe4-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="93fe4-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="93fe4-151">-SubnetId</span></span>
<span data-ttu-id="93fe4-152">Specifica l'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="93fe4-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="93fe4-153">Specificare questo parametro se il gateway usa un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="93fe4-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="93fe4-154">Se si specifica il parametro *PrivateIPAddress,* questo deve appartenere alla subnet.</span><span class="sxs-lookup"><span data-stu-id="93fe4-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="93fe4-155">Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene scelto dinamicamente come indirizzo IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="93fe4-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="93fe4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93fe4-156">CommonParameters</span></span>
<span data-ttu-id="93fe4-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93fe4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93fe4-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93fe4-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93fe4-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="93fe4-159">INPUTS</span></span>

### <span data-ttu-id="93fe4-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93fe4-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93fe4-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93fe4-161">OUTPUTS</span></span>

### <span data-ttu-id="93fe4-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93fe4-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93fe4-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="93fe4-163">NOTES</span></span>

## <span data-ttu-id="93fe4-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93fe4-164">RELATED LINKS</span></span>

[<span data-ttu-id="93fe4-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="93fe4-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="93fe4-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="93fe4-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="93fe4-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="93fe4-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="93fe4-168">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="93fe4-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="93fe4-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="93fe4-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


