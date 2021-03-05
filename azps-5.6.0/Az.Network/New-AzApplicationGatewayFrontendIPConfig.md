---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 214f408a5120982a903ed0d0d934c44073c32df8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986760"
---
# <span data-ttu-id="c98ee-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c98ee-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="c98ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c98ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c98ee-103">Crea una configurazione IP front-end per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c98ee-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="c98ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c98ee-104">SYNTAX</span></span>

### <span data-ttu-id="c98ee-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c98ee-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c98ee-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c98ee-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c98ee-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c98ee-107">DESCRIPTION</span></span>
<span data-ttu-id="c98ee-108">Il cmdlet **New-AzApplicationGatewayFrontendIPConfig crea** una configurazione IP front-end per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c98ee-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="c98ee-109">Un gateway applicazione supporta due tipi di configurazione IP front-end:</span><span class="sxs-lookup"><span data-stu-id="c98ee-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="c98ee-110">Indirizzi IP pubblici: indirizzi IP privati che usano il bilanciamento del carico interno (ILB, Internal Load Balancing).</span><span class="sxs-lookup"><span data-stu-id="c98ee-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="c98ee-111">Un gateway applicazione può avere al massimo un indirizzo IP pubblico e uno privato.</span><span class="sxs-lookup"><span data-stu-id="c98ee-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="c98ee-112">L'indirizzo IP pubblico e l'indirizzo IP privato devono essere aggiunti separatamente come indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="c98ee-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="c98ee-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c98ee-113">EXAMPLES</span></span>

### <span data-ttu-id="c98ee-114">Esempio 1: Creare una configurazione IP front-end usando un oggetto risorsa IP pubblico</span><span class="sxs-lookup"><span data-stu-id="c98ee-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="c98ee-115">Il primo comando crea un oggetto risorsa IP pubblica e lo archivia nella $PublicIP variabile.</span><span class="sxs-lookup"><span data-stu-id="c98ee-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="c98ee-116">Il secondo comando usa $PublicIP per creare una nuova configurazione IP front-end denominata FrontEndIP01 e la archivia nella variabile $FrontEnd iniziale.</span><span class="sxs-lookup"><span data-stu-id="c98ee-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="c98ee-117">Esempio 2: Creare un IP privato statico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="c98ee-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="c98ee-118">Il primo comando ottiene una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e la archivia nella $VNet variabile.</span><span class="sxs-lookup"><span data-stu-id="c98ee-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="c98ee-119">Il secondo comando ottiene una configurazione subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet locale.</span><span class="sxs-lookup"><span data-stu-id="c98ee-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="c98ee-120">Il terzo comando crea una configurazione IP front-end denominata FrontEndIP02 usando $Subnet dal secondo comando e l'indirizzo IP privato 10.0.1.1, quindi la archivia nella variabile $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="c98ee-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="c98ee-121">Esempio 3: Creare un IP privato dinamico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="c98ee-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="c98ee-122">Il primo comando ottiene una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e la archivia nella $VNet variabile.</span><span class="sxs-lookup"><span data-stu-id="c98ee-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="c98ee-123">Il secondo comando ottiene una configurazione subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet locale.</span><span class="sxs-lookup"><span data-stu-id="c98ee-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="c98ee-124">Il terzo comando crea una configurazione IP front-end denominata FrontEndIP03 usando $Subnet dal secondo comando e la archivia nella $FrontEnd variabile.</span><span class="sxs-lookup"><span data-stu-id="c98ee-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="c98ee-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c98ee-125">PARAMETERS</span></span>

### <span data-ttu-id="c98ee-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98ee-126">-DefaultProfile</span></span>
<span data-ttu-id="c98ee-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c98ee-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c98ee-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c98ee-128">-Name</span></span>
<span data-ttu-id="c98ee-129">Specifica il nome della configurazione IP front-end creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c98ee-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c98ee-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="c98ee-130">-PrivateIPAddress</span></span>
<span data-ttu-id="c98ee-131">Specifica l'indirizzo IP privato che questo cmdlet associa all'indirizzo IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c98ee-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="c98ee-132">Può essere specificato solo se è specificata una subnet.</span><span class="sxs-lookup"><span data-stu-id="c98ee-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="c98ee-133">Questo INDIRIZZO IP è allocato staticamente dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="c98ee-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="c98ee-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c98ee-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="c98ee-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c98ee-135">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="c98ee-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c98ee-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="c98ee-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c98ee-137">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="c98ee-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="c98ee-138">-PublicIPAddress</span></span>
<span data-ttu-id="c98ee-139">Specifica l'oggetto indirizzo IP pubblico che questo cmdlet associa all'indirizzo IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c98ee-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c98ee-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="c98ee-140">-PublicIPAddressId</span></span>
<span data-ttu-id="c98ee-141">Specifica l'ID dell'indirizzo IP pubblico che questo cmdlet associa all'INDIRIZZO IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c98ee-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="c98ee-142">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c98ee-142">-Subnet</span></span>
<span data-ttu-id="c98ee-143">Specifica l'oggetto subnet associato dal cmdlet all'indirizzo IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c98ee-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="c98ee-144">Se si specifica questo parametro, il gateway usa un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="c98ee-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="c98ee-145">Se è specificato il parametro *PrivateIPAddress,* deve appartenere alla subnet specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c98ee-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="c98ee-146">Se *privateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene scelto dinamicamente come indirizzo IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c98ee-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c98ee-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c98ee-147">-SubnetId</span></span>
<span data-ttu-id="c98ee-148">Specifica l'ID subnet a cui questo cmdlet associa la configurazione IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c98ee-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="c98ee-149">Se si specifica il *parametro Subnet,* significa che il gateway usa un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="c98ee-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="c98ee-150">Se si *specifica il parametro PrivateIPAddress,* deve appartenere alla subnet specificata da *Subnet.*</span><span class="sxs-lookup"><span data-stu-id="c98ee-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="c98ee-151">Se *privateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene scelto dinamicamente come indirizzo IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c98ee-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c98ee-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98ee-152">CommonParameters</span></span>
<span data-ttu-id="c98ee-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98ee-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98ee-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c98ee-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98ee-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="c98ee-155">INPUTS</span></span>

### <span data-ttu-id="c98ee-156">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c98ee-156">None</span></span>

## <span data-ttu-id="c98ee-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c98ee-157">OUTPUTS</span></span>

### <span data-ttu-id="c98ee-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c98ee-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="c98ee-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="c98ee-159">NOTES</span></span>

## <span data-ttu-id="c98ee-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c98ee-160">RELATED LINKS</span></span>

[<span data-ttu-id="c98ee-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c98ee-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c98ee-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c98ee-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c98ee-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c98ee-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c98ee-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c98ee-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


