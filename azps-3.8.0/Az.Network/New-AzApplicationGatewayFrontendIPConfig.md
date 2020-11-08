---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c36c185ac2fecf1e4584c1bb1b2025ce3b431cf4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022759"
---
# <span data-ttu-id="ab7bd-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab7bd-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="ab7bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab7bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ab7bd-103">Crea una configurazione IP front-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="ab7bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab7bd-104">SYNTAX</span></span>

### <span data-ttu-id="ab7bd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab7bd-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab7bd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ab7bd-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab7bd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab7bd-107">DESCRIPTION</span></span>
<span data-ttu-id="ab7bd-108">Il cmdlet **New-AzApplicationGatewayFrontendIPConfig** crea una configurazione IP front-end per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="ab7bd-109">Un gateway applicazione supporta due tipi di configurazione IP front-end:</span><span class="sxs-lookup"><span data-stu-id="ab7bd-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="ab7bd-110">Indirizzi IP pubblici--indirizzi IP privati con il bilanciamento del carico interno (ILB).</span><span class="sxs-lookup"><span data-stu-id="ab7bd-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="ab7bd-111">Un gateway applicazione può avere al massimo un indirizzo IP pubblico e un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="ab7bd-112">L'indirizzo IP pubblico e l'indirizzo IP privato devono essere aggiunti separatamente come indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="ab7bd-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab7bd-113">EXAMPLES</span></span>

### <span data-ttu-id="ab7bd-114">Esempio 1: creare una configurazione IP front-end usando un oggetto risorsa IP pubblico</span><span class="sxs-lookup"><span data-stu-id="ab7bd-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="ab7bd-115">Il primo comando crea un oggetto risorsa IP pubblico e lo archivia nella variabile $PublicIP.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="ab7bd-116">Il secondo comando USA $PublicIP per creare una nuova configurazione IP front-end denominata FrontEndIP01 e la archivia nella variabile $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="ab7bd-117">Esempio 2: creare un IP privato statico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="ab7bd-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="ab7bd-118">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="ab7bd-119">Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ab7bd-120">Il terzo comando crea una configurazione IP front-end denominata FrontEndIP02 usando $Subnet dal secondo comando e dall'indirizzo IP privato 10.0.1.1, quindi lo archivia nella variabile $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="ab7bd-121">Esempio 3: creare un IP privato dinamico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="ab7bd-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="ab7bd-122">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="ab7bd-123">Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ab7bd-124">Il terzo comando crea una configurazione IP front-end denominata FrontEndIP03 usando $Subnet dal secondo comando e la archivia nella variabile $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="ab7bd-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab7bd-125">PARAMETERS</span></span>

### <span data-ttu-id="ab7bd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab7bd-126">-DefaultProfile</span></span>
<span data-ttu-id="ab7bd-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab7bd-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab7bd-128">-Name</span></span>
<span data-ttu-id="ab7bd-129">Specifica il nome della configurazione IP front-end creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ab7bd-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="ab7bd-130">-PrivateIPAddress</span></span>
<span data-ttu-id="ab7bd-131">Specifica l'indirizzo IP privato che questo cmdlet associa all'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="ab7bd-132">Questa operazione può essere specificata solo se è specificata una subnet.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="ab7bd-133">Questo IP viene allocato in modo statico dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="ab7bd-134">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="ab7bd-134">-PublicIPAddress</span></span>
<span data-ttu-id="ab7bd-135">Specifica l'oggetto indirizzo IP pubblico che questo cmdlet associa all'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-135">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="ab7bd-136">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="ab7bd-136">-PublicIPAddressId</span></span>
<span data-ttu-id="ab7bd-137">Specifica l'ID indirizzo IP pubblico che questo cmdlet associa all'IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-137">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="ab7bd-138">-Subnet</span><span class="sxs-lookup"><span data-stu-id="ab7bd-138">-Subnet</span></span>
<span data-ttu-id="ab7bd-139">Specifica l'oggetto subnet che questo cmdlet associa all'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-139">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="ab7bd-140">Se specifichi questo parametro, significa che il gateway usa un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-140">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="ab7bd-141">Se il parametro *PrivateIPAddress* è specificato, deve appartenere alla subnet specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-141">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="ab7bd-142">Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene selezionato in modo dinamico come indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-142">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="ab7bd-143">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ab7bd-143">-SubnetId</span></span>
<span data-ttu-id="ab7bd-144">Specifica l'ID subnet che questo cmdlet associa alla configurazione IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-144">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="ab7bd-145">Se specifichi il parametro *subnet* , significa che il gateway usa un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-145">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="ab7bd-146">Se il parametro *PrivateIPAddress* è specificato, deve appartenere alla subnet specificata dalla *Subnet*.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-146">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="ab7bd-147">Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene selezionato in modo dinamico come indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="ab7bd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab7bd-148">CommonParameters</span></span>
<span data-ttu-id="ab7bd-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab7bd-150">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab7bd-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab7bd-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab7bd-151">INPUTS</span></span>

### <span data-ttu-id="ab7bd-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ab7bd-152">None</span></span>

## <span data-ttu-id="ab7bd-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab7bd-153">OUTPUTS</span></span>

### <span data-ttu-id="ab7bd-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab7bd-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="ab7bd-155">Note</span><span class="sxs-lookup"><span data-stu-id="ab7bd-155">NOTES</span></span>

## <span data-ttu-id="ab7bd-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab7bd-156">RELATED LINKS</span></span>

[<span data-ttu-id="ab7bd-157">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab7bd-157">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ab7bd-158">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab7bd-158">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ab7bd-159">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab7bd-159">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ab7bd-160">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab7bd-160">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


