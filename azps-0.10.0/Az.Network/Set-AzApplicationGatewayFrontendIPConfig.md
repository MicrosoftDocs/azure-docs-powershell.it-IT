---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: e85976f77ece9af89ecd532ff0a3236039abb9fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862846"
---
# <span data-ttu-id="3c58b-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c58b-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="3c58b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c58b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c58b-103">Modifica la configurazione di un indirizzo IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3c58b-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="3c58b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c58b-104">SYNTAX</span></span>

### <span data-ttu-id="3c58b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c58b-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c58b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3c58b-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c58b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c58b-107">DESCRIPTION</span></span>
<span data-ttu-id="3c58b-108">Il cmdlet **set-AzApplicationGatewayFrontendIPConfig** aggiorna una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3c58b-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="3c58b-109">Un gateway applicazione supporta due tipi di indirizzi IP front-end:</span><span class="sxs-lookup"><span data-stu-id="3c58b-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="3c58b-110">Indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="3c58b-110">Public IP addresses</span></span>
- <span data-ttu-id="3c58b-111">Indirizzi IP privati per cui la configurazione usa il bilanciamento del carico interno (ILB)</span><span class="sxs-lookup"><span data-stu-id="3c58b-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="3c58b-112">Un gateway applicazione può avere al massimo un indirizzo IP pubblico e un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="3c58b-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="3c58b-113">Un indirizzo IP pubblico e un indirizzo IP privato devono essere aggiunti separatamente come indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3c58b-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="3c58b-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c58b-114">EXAMPLES</span></span>

### <span data-ttu-id="3c58b-115">Esempio 1: impostare un IP pubblico come IP front-end di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="3c58b-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="3c58b-116">Il primo comando crea un oggetto indirizzo IP pubblico e lo archivia nella variabile $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="3c58b-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="3c58b-117">Il secondo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3c58b-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="3c58b-118">Il terzo comando Aggiorna la configurazione IP front-end denominata FrontEndIp01, per il gateway in $AppGw, usando l'indirizzo archiviato in $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="3c58b-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="3c58b-119">Esempio 2: impostare un IP privato statico come IP front-end di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="3c58b-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="3c58b-120">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="3c58b-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="3c58b-121">Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3c58b-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="3c58b-122">Il terzo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3c58b-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="3c58b-123">Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet dal secondo comando e dall'indirizzo IP privato 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="3c58b-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="3c58b-124">Esempio 3: impostare un IP privato dinamico come IP front-end di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="3c58b-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="3c58b-125">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="3c58b-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="3c58b-126">Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3c58b-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="3c58b-127">Il terzo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3c58b-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="3c58b-128">Il quarto comando aggiunge una configurazione IP front-end denominata FrontendIP02 usando $Subnet dal secondo comando.</span><span class="sxs-lookup"><span data-stu-id="3c58b-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="3c58b-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c58b-129">PARAMETERS</span></span>

### <span data-ttu-id="3c58b-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c58b-130">-ApplicationGateway</span></span>
<span data-ttu-id="3c58b-131">Specifica un oggetto gateway dell'applicazione in cui modificare la configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3c58b-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="3c58b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c58b-132">-DefaultProfile</span></span>
<span data-ttu-id="3c58b-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c58b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c58b-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c58b-134">-Name</span></span>
<span data-ttu-id="3c58b-135">Specifica il nome della configurazione IP front-end che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3c58b-135">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3c58b-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="3c58b-136">-PrivateIPAddress</span></span>
<span data-ttu-id="3c58b-137">Specifica l'indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="3c58b-137">Specifies the private IP address.</span></span>
<span data-ttu-id="3c58b-138">Se specificato, questo IP viene allocato in modo statico dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="3c58b-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="3c58b-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="3c58b-139">-PublicIPAddress</span></span>
<span data-ttu-id="3c58b-140">Specifica l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="3c58b-140">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="3c58b-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="3c58b-141">-PublicIPAddressId</span></span>
<span data-ttu-id="3c58b-142">Specifica l'ID dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="3c58b-142">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="3c58b-143">-Subnet</span><span class="sxs-lookup"><span data-stu-id="3c58b-143">-Subnet</span></span>
<span data-ttu-id="3c58b-144">Specifica la subnet utilizzata dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c58b-144">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="3c58b-145">Specificare questo parametro se il gateway usa un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="3c58b-145">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="3c58b-146">Se l'indirizzo *PrivateIPAddress* è specificato, deve appartenere a questa subnet.</span><span class="sxs-lookup"><span data-stu-id="3c58b-146">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="3c58b-147">Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene selezionato in modo dinamico come indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c58b-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="3c58b-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3c58b-148">-SubnetId</span></span>
<span data-ttu-id="3c58b-149">Specifica l'ID subnet.</span><span class="sxs-lookup"><span data-stu-id="3c58b-149">Specifies the subnet ID.</span></span>
<span data-ttu-id="3c58b-150">Specificare questo parametro se il gateway usa un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="3c58b-150">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="3c58b-151">Se il parametro *PrivateIPAddress* è specificato, deve appartenere a questa subnet.</span><span class="sxs-lookup"><span data-stu-id="3c58b-151">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="3c58b-152">Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene selezionato in modo dinamico come indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c58b-152">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="3c58b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c58b-153">CommonParameters</span></span>
<span data-ttu-id="3c58b-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c58b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c58b-155">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c58b-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c58b-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c58b-156">INPUTS</span></span>

### <span data-ttu-id="3c58b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="3c58b-157">System.String</span></span>

## <span data-ttu-id="3c58b-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c58b-158">OUTPUTS</span></span>

### <span data-ttu-id="3c58b-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c58b-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3c58b-160">Note</span><span class="sxs-lookup"><span data-stu-id="3c58b-160">NOTES</span></span>

## <span data-ttu-id="3c58b-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c58b-161">RELATED LINKS</span></span>

[<span data-ttu-id="3c58b-162">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c58b-162">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3c58b-163">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c58b-163">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3c58b-164">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c58b-164">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3c58b-165">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c58b-165">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3c58b-166">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c58b-166">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


