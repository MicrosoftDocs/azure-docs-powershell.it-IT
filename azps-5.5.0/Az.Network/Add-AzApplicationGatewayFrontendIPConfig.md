---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194006"
---
# <span data-ttu-id="6a8c8-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6a8c8-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="6a8c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8c8-103">Aggiunge una configurazione IP front-end a un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="6a8c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a8c8-104">SYNTAX</span></span>

### <span data-ttu-id="6a8c8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a8c8-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a8c8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6a8c8-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a8c8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6a8c8-107">DESCRIPTION</span></span>
<span data-ttu-id="6a8c8-108">Il cmdlet **Add-AzApplicationGatewayFrontendIPConfig aggiunge** una configurazione IP front-end a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="6a8c8-109">Un gateway applicazione supporta due tipi di configurazioni IP front-end:</span><span class="sxs-lookup"><span data-stu-id="6a8c8-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="6a8c8-110">Indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="6a8c8-110">Public IP addresses</span></span>
- <span data-ttu-id="6a8c8-111">Indirizzi IP privati che usano il bilanciamento del carico interno (ILB, Internal Load-Balancing) Un gateway di applicazione può avere al massimo un IP pubblico e uno privato.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="6a8c8-112">Aggiungere l'indirizzo IP pubblico e l'indirizzo IP privato come IP front-end distinti.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="6a8c8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a8c8-113">EXAMPLES</span></span>

### <span data-ttu-id="6a8c8-114">Esempio 1: Aggiungere un indirizzo IP pubblico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="6a8c8-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="6a8c8-115">Il primo comando crea un oggetto indirizzo IP pubblico e lo archivia nella $PublicIp variabile.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="6a8c8-116">Il secondo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6a8c8-117">Il terzo comando aggiunge la configurazione IP front-end denominata FrontEndIp01 per il gateway in $AppGw, usando l'indirizzo archiviato in $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="6a8c8-118">Esempio 2: Aggiungere un IP privato statico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="6a8c8-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="6a8c8-119">Il primo comando ottiene una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e la archivia nella $VNet variabile.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="6a8c8-120">Il secondo comando ottiene una configurazione subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet locale.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="6a8c8-121">Il terzo comando recupera il gateway applicazione denominato ApplicationGateway01, che appartiene al gruppo di risorse denominato ResourceGroup01, e lo archivia nella variabile $AppGw risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6a8c8-122">Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet del secondo comando e l'indirizzo IP privato 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="6a8c8-123">Esempio 3: Aggiungere un IP privato dinamico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="6a8c8-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="6a8c8-124">Il primo comando ottiene una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e la archivia nella $VNet variabile.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="6a8c8-125">Il secondo comando ottiene una configurazione subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet locale.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="6a8c8-126">Il terzo comando recupera il gateway applicazione denominato ApplicationGateway01, che appartiene al gruppo di risorse denominato ResourceGroup01, e lo archivia nella variabile $AppGw risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6a8c8-127">Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet dal secondo comando.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="6a8c8-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a8c8-128">PARAMETERS</span></span>

### <span data-ttu-id="6a8c8-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a8c8-129">-ApplicationGateway</span></span>
<span data-ttu-id="6a8c8-130">Specifica il gateway applicazione a cui questo cmdlet aggiunge una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="6a8c8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8c8-131">-DefaultProfile</span></span>
<span data-ttu-id="6a8c8-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a8c8-133">-Name</span><span class="sxs-lookup"><span data-stu-id="6a8c8-133">-Name</span></span>
<span data-ttu-id="6a8c8-134">Specifica il nome della configurazione IP front-end da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="6a8c8-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="6a8c8-135">-PrivateIPAddress</span></span>
<span data-ttu-id="6a8c8-136">Specifica l'indirizzo IP privato da aggiungere come indirizzo IP front-end per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="6a8c8-137">Se specificato, l'indirizzo IP viene allocato staticamente dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="6a8c8-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a8c8-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="6a8c8-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a8c8-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="6a8c8-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6a8c8-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="6a8c8-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6a8c8-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="6a8c8-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="6a8c8-142">-PublicIPAddress</span></span>
<span data-ttu-id="6a8c8-143">Specifica l'indirizzo IP pubblico aggiunto dal cmdlet come indirizzo IP front-end per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="6a8c8-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="6a8c8-144">-PublicIPAddressId</span></span>
<span data-ttu-id="6a8c8-145">Specifica l'ID dell'indirizzo IP pubblico che il cmdlet aggiunge come indirizzo IP front-end per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="6a8c8-146">-Subnet</span><span class="sxs-lookup"><span data-stu-id="6a8c8-146">-Subnet</span></span>
<span data-ttu-id="6a8c8-147">Specifica la subnet a cui questo cmdlet aggiunge come configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="6a8c8-148">Se si specifica questo parametro, il gateway applicazione supporta una configurazione privata basata su IP.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="6a8c8-149">Se si specifica il parametro *PrivateIPAddress,* questo deve appartenere alla subnet.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="6a8c8-150">Se *privateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene scelto dinamicamente come indirizzo IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="6a8c8-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6a8c8-151">-SubnetId</span></span>
<span data-ttu-id="6a8c8-152">Specifica l'ID subnet aggiunto da questo cmdlet come configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="6a8c8-153">Il passaggio della subnet implica l'ip privato.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="6a8c8-154">Se si specifica il parametro *PrivateIPAddress,* questo deve appartenere alla subnet.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="6a8c8-155">In caso contrario, uno degli indirizzi IP di questa subnet viene scelto dinamicamente come IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="6a8c8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8c8-156">CommonParameters</span></span>
<span data-ttu-id="6a8c8-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8c8-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a8c8-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8c8-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="6a8c8-159">INPUTS</span></span>

### <span data-ttu-id="6a8c8-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a8c8-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a8c8-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a8c8-161">OUTPUTS</span></span>

### <span data-ttu-id="6a8c8-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a8c8-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a8c8-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="6a8c8-163">NOTES</span></span>

## <span data-ttu-id="6a8c8-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a8c8-164">RELATED LINKS</span></span>

[<span data-ttu-id="6a8c8-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6a8c8-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6a8c8-166">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6a8c8-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6a8c8-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6a8c8-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6a8c8-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6a8c8-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


