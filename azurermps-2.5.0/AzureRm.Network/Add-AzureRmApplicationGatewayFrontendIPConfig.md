---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 646aaa2ec5d39089627caa97e74990ac3ce43b5c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866501"
---
# <span data-ttu-id="48d8a-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="48d8a-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="48d8a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="48d8a-103">Aggiunge una configurazione IP front-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48d8a-103">Adds a front-end IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48d8a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48d8a-104">SYNTAX</span></span>

### <span data-ttu-id="48d8a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="48d8a-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d8a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="48d8a-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48d8a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48d8a-107">DESCRIPTION</span></span>
<span data-ttu-id="48d8a-108">Il cmdlet **Add-AzureRmApplicationGatewayFrontendIPConfig** aggiunge una configurazione IP front-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48d8a-108">The **Add-AzureRmApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="48d8a-109">Un gateway applicazione supporta due tipi di configurazioni IP front-end:</span><span class="sxs-lookup"><span data-stu-id="48d8a-109">An application gateway supports two types of front-end IP configurations:</span></span> 

- <span data-ttu-id="48d8a-110">Indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="48d8a-110">Public IP addresses</span></span>
- <span data-ttu-id="48d8a-111">Indirizzi IP privati con il bilanciamento del carico interno (ILB)</span><span class="sxs-lookup"><span data-stu-id="48d8a-111">Private IP addresses using internal load-balancing (ILB)</span></span>

<span data-ttu-id="48d8a-112">Un gateway applicazione può avere al massimo un IP pubblico e un IP privato.</span><span class="sxs-lookup"><span data-stu-id="48d8a-112">An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="48d8a-113">Aggiungere l'indirizzo IP pubblico e l'indirizzo IP privato come IPs front-end separato.</span><span class="sxs-lookup"><span data-stu-id="48d8a-113">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="48d8a-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48d8a-114">EXAMPLES</span></span>

### <span data-ttu-id="48d8a-115">Esempio 1: aggiungere un IP pubblico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="48d8a-115">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="48d8a-116">Il primo comando crea un oggetto indirizzo IP pubblico e lo archivia nella variabile $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="48d8a-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="48d8a-117">Il secondo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="48d8a-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="48d8a-118">Il terzo comando aggiunge la configurazione IP front-end denominata FrontEndIp01, per il gateway in $AppGw, usando l'indirizzo archiviato in $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="48d8a-118">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="48d8a-119">Esempio 2: aggiungere un IP privato statico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="48d8a-119">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="48d8a-120">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="48d8a-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="48d8a-121">Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="48d8a-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="48d8a-122">Il terzo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="48d8a-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="48d8a-123">Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet dal secondo comando e dall'indirizzo IP privato 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="48d8a-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="48d8a-124">Esempio 3: aggiungere un IP privato dinamico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="48d8a-124">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="48d8a-125">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="48d8a-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="48d8a-126">Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="48d8a-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="48d8a-127">Il terzo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="48d8a-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="48d8a-128">Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet dal secondo comando.</span><span class="sxs-lookup"><span data-stu-id="48d8a-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="48d8a-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48d8a-129">PARAMETERS</span></span>

### <span data-ttu-id="48d8a-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48d8a-130">-ApplicationGateway</span></span>
<span data-ttu-id="48d8a-131">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="48d8a-131">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="48d8a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d8a-132">-DefaultProfile</span></span>
<span data-ttu-id="48d8a-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48d8a-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d8a-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="48d8a-134">-Name</span></span>
<span data-ttu-id="48d8a-135">Specifica il nome della configurazione IP front-end da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="48d8a-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="48d8a-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="48d8a-136">-PrivateIPAddress</span></span>
<span data-ttu-id="48d8a-137">Specifica l'indirizzo IP privato da aggiungere come IP front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48d8a-137">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="48d8a-138">Se specificato, questo IP viene allocato in modo statico dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="48d8a-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="48d8a-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="48d8a-139">-PublicIPAddress</span></span>
<span data-ttu-id="48d8a-140">Specifica l'indirizzo IP pubblico che questo cmdlet aggiunge come indirizzo IP front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48d8a-140">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="48d8a-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="48d8a-141">-PublicIPAddressId</span></span>
<span data-ttu-id="48d8a-142">Specifica l'ID dell'indirizzo IP pubblico che questo cmdlet aggiunge come indirizzo IP front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48d8a-142">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="48d8a-143">-Subnet</span><span class="sxs-lookup"><span data-stu-id="48d8a-143">-Subnet</span></span>
<span data-ttu-id="48d8a-144">Specifica la subnet aggiunta da questo cmdlet come configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="48d8a-144">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="48d8a-145">Se specifichi questo parametro, significa che il gateway dell'applicazione supporta una configurazione privata basata su IP.</span><span class="sxs-lookup"><span data-stu-id="48d8a-145">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="48d8a-146">Se il parametro *PrivateIPAddress* è specificato, deve appartenere a questa subnet.</span><span class="sxs-lookup"><span data-stu-id="48d8a-146">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="48d8a-147">Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene selezionato in modo dinamico come indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48d8a-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="48d8a-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="48d8a-148">-SubnetId</span></span>
<span data-ttu-id="48d8a-149">Specifica l'ID subnet che questo cmdlet aggiunge come configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="48d8a-149">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="48d8a-150">Il passaggio di subnet implica un IP privato.</span><span class="sxs-lookup"><span data-stu-id="48d8a-150">Passing subnet implies private IP.</span></span>
<span data-ttu-id="48d8a-151">Se il parametro *PrivateIPAddresss* è specificato, deve appartenere a questa subnet.</span><span class="sxs-lookup"><span data-stu-id="48d8a-151">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="48d8a-152">In caso contrario, uno degli IP di questa subnet viene selezionato in modo dinamico come IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48d8a-152">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="48d8a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d8a-153">CommonParameters</span></span>
<span data-ttu-id="48d8a-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48d8a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d8a-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d8a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d8a-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48d8a-156">INPUTS</span></span>

### <span data-ttu-id="48d8a-157">System. String</span><span class="sxs-lookup"><span data-stu-id="48d8a-157">System.String</span></span>

## <span data-ttu-id="48d8a-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48d8a-158">OUTPUTS</span></span>

### <span data-ttu-id="48d8a-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48d8a-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="48d8a-160">Note</span><span class="sxs-lookup"><span data-stu-id="48d8a-160">NOTES</span></span>

## <span data-ttu-id="48d8a-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48d8a-161">RELATED LINKS</span></span>

[<span data-ttu-id="48d8a-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="48d8a-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="48d8a-163">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="48d8a-163">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="48d8a-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="48d8a-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="48d8a-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="48d8a-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


