---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 4b0fd2fd55b255a9734a0c6b0c325f7ac113b4e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861034"
---
# <span data-ttu-id="24933-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="24933-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="24933-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24933-102">SYNOPSIS</span></span>
<span data-ttu-id="24933-103">Aggiunge una configurazione IP front-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24933-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="24933-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24933-104">SYNTAX</span></span>

### <span data-ttu-id="24933-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="24933-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24933-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="24933-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24933-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24933-107">DESCRIPTION</span></span>
<span data-ttu-id="24933-108">Il cmdlet **Add-AzApplicationGatewayFrontendIPConfig** aggiunge una configurazione IP front-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24933-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="24933-109">Un gateway applicazione supporta due tipi di configurazioni IP front-end:</span><span class="sxs-lookup"><span data-stu-id="24933-109">An application gateway supports two types of front-end IP configurations:</span></span> 

- <span data-ttu-id="24933-110">Indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="24933-110">Public IP addresses</span></span>
- <span data-ttu-id="24933-111">Indirizzi IP privati con il bilanciamento del carico interno (ILB)</span><span class="sxs-lookup"><span data-stu-id="24933-111">Private IP addresses using internal load-balancing (ILB)</span></span>

<span data-ttu-id="24933-112">Un gateway applicazione può avere al massimo un IP pubblico e un IP privato.</span><span class="sxs-lookup"><span data-stu-id="24933-112">An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="24933-113">Aggiungere l'indirizzo IP pubblico e l'indirizzo IP privato come IPs front-end separato.</span><span class="sxs-lookup"><span data-stu-id="24933-113">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="24933-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24933-114">EXAMPLES</span></span>

### <span data-ttu-id="24933-115">Esempio 1: aggiungere un IP pubblico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="24933-115">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="24933-116">Il primo comando crea un oggetto indirizzo IP pubblico e lo archivia nella variabile $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="24933-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="24933-117">Il secondo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="24933-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="24933-118">Il terzo comando aggiunge la configurazione IP front-end denominata FrontEndIp01, per il gateway in $AppGw, usando l'indirizzo archiviato in $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="24933-118">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="24933-119">Esempio 2: aggiungere un IP privato statico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="24933-119">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="24933-120">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="24933-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="24933-121">Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="24933-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="24933-122">Il terzo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="24933-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="24933-123">Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet dal secondo comando e dall'indirizzo IP privato 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="24933-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="24933-124">Esempio 3: aggiungere un IP privato dinamico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="24933-124">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="24933-125">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="24933-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="24933-126">Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="24933-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="24933-127">Il terzo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="24933-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="24933-128">Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet dal secondo comando.</span><span class="sxs-lookup"><span data-stu-id="24933-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="24933-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24933-129">PARAMETERS</span></span>

### <span data-ttu-id="24933-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24933-130">-ApplicationGateway</span></span>
<span data-ttu-id="24933-131">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="24933-131">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="24933-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24933-132">-DefaultProfile</span></span>
<span data-ttu-id="24933-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24933-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24933-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="24933-134">-Name</span></span>
<span data-ttu-id="24933-135">Specifica il nome della configurazione IP front-end da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="24933-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="24933-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="24933-136">-PrivateIPAddress</span></span>
<span data-ttu-id="24933-137">Specifica l'indirizzo IP privato da aggiungere come IP front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24933-137">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="24933-138">Se specificato, questo IP viene allocato in modo statico dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="24933-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="24933-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="24933-139">-PublicIPAddress</span></span>
<span data-ttu-id="24933-140">Specifica l'indirizzo IP pubblico che questo cmdlet aggiunge come indirizzo IP front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24933-140">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="24933-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="24933-141">-PublicIPAddressId</span></span>
<span data-ttu-id="24933-142">Specifica l'ID dell'indirizzo IP pubblico che questo cmdlet aggiunge come indirizzo IP front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24933-142">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="24933-143">-Subnet</span><span class="sxs-lookup"><span data-stu-id="24933-143">-Subnet</span></span>
<span data-ttu-id="24933-144">Specifica la subnet aggiunta da questo cmdlet come configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="24933-144">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="24933-145">Se specifichi questo parametro, significa che il gateway dell'applicazione supporta una configurazione privata basata su IP.</span><span class="sxs-lookup"><span data-stu-id="24933-145">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="24933-146">Se il parametro *PrivateIPAddress* è specificato, deve appartenere a questa subnet.</span><span class="sxs-lookup"><span data-stu-id="24933-146">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="24933-147">Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene selezionato in modo dinamico come indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24933-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="24933-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="24933-148">-SubnetId</span></span>
<span data-ttu-id="24933-149">Specifica l'ID subnet che questo cmdlet aggiunge come configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="24933-149">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="24933-150">Il passaggio di subnet implica un IP privato.</span><span class="sxs-lookup"><span data-stu-id="24933-150">Passing subnet implies private IP.</span></span>
<span data-ttu-id="24933-151">Se il parametro *PrivateIPAddresss* è specificato, deve appartenere a questa subnet.</span><span class="sxs-lookup"><span data-stu-id="24933-151">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="24933-152">In caso contrario, uno degli IP di questa subnet viene selezionato in modo dinamico come IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24933-152">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="24933-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24933-153">CommonParameters</span></span>
<span data-ttu-id="24933-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24933-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24933-155">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24933-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24933-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24933-156">INPUTS</span></span>

### <span data-ttu-id="24933-157">System. String</span><span class="sxs-lookup"><span data-stu-id="24933-157">System.String</span></span>

## <span data-ttu-id="24933-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24933-158">OUTPUTS</span></span>

### <span data-ttu-id="24933-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24933-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24933-160">Note</span><span class="sxs-lookup"><span data-stu-id="24933-160">NOTES</span></span>

## <span data-ttu-id="24933-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24933-161">RELATED LINKS</span></span>

[<span data-ttu-id="24933-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="24933-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="24933-163">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="24933-163">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="24933-164">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="24933-164">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="24933-165">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="24933-165">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


