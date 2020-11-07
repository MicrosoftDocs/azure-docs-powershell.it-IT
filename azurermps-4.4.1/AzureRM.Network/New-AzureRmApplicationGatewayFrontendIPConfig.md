---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 6f5edd934e7239c8d4bb5083e5b4881fff79f489
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688270"
---
# <span data-ttu-id="c242d-101">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c242d-101">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="c242d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c242d-102">SYNOPSIS</span></span>
<span data-ttu-id="c242d-103">Crea una configurazione IP front-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c242d-103">Creates a front-end IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c242d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c242d-104">SYNTAX</span></span>

### <span data-ttu-id="c242d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c242d-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c242d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c242d-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c242d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c242d-107">DESCRIPTION</span></span>
<span data-ttu-id="c242d-108">Il cmdlet **New-AzureRmApplicationGatewayFrontendIPConfig** crea un configuraton IP front-end per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="c242d-108">The **New-AzureRmApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuraton for an Azure application gateway.</span></span>
<span data-ttu-id="c242d-109">Un gateway applicazione supporta due tipi di configurazione IP front-end:</span><span class="sxs-lookup"><span data-stu-id="c242d-109">An application gateway supports two types of front-end IP configuration:</span></span> 

- <span data-ttu-id="c242d-110">Indirizzi IP pubblici--indirizzi IP privati con il bilanciamento del carico interno (ILB).</span><span class="sxs-lookup"><span data-stu-id="c242d-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>

<span data-ttu-id="c242d-111">Un gateway applicazione può avere al massimo un indirizzo IP pubblico e un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="c242d-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="c242d-112">L'indirizzo IP pubblico e l'indirizzo IP privato devono essere aggiunti separatamente come indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="c242d-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="c242d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c242d-113">EXAMPLES</span></span>

### <span data-ttu-id="c242d-114">Esempio 1: creare una configurazione IP front-end usando un oggetto risorsa IP pubblico</span><span class="sxs-lookup"><span data-stu-id="c242d-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="c242d-115">Il primo comando crea un oggetto risorsa IP pubblico e lo archivia nella variabile $PublicIP.</span><span class="sxs-lookup"><span data-stu-id="c242d-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="c242d-116">Il secondo comando USA $PublicIP per creare una nuova configurazione IP front-end denominata FrontEndIP01 e la archivia nella variabile $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="c242d-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="c242d-117">Esempio 2: creare un IP privato statico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="c242d-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="c242d-118">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="c242d-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="c242d-119">Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c242d-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="c242d-120">Il terzo comando crea una configurazione IP front-end denominata FrontEndIP02 usando $Subnet dal secondo comando e dall'indirizzo IP privato 10.0.1.1, quindi lo archivia nella variabile $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="c242d-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="c242d-121">Esempio 3: creare un IP privato dinamico come indirizzo IP front-end</span><span class="sxs-lookup"><span data-stu-id="c242d-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="c242d-122">Il primo comando consente di ottenere una rete virtuale denominata VNet01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="c242d-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="c242d-123">Il secondo comando ottiene una configurazione della subnet denominata Subnet01 usando $VNet dal primo comando e la archivia nella variabile $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c242d-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="c242d-124">Il terzo comando crea una configurazione IP front-end denominata FrontEndIP03 usando $Subnet dal secondo comando e la archivia nella variabile $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="c242d-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="c242d-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c242d-125">PARAMETERS</span></span>

### <span data-ttu-id="c242d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c242d-126">-Name</span></span>
<span data-ttu-id="c242d-127">Specifica il nome della configurazione IP front-end creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c242d-127">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c242d-128">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="c242d-128">-PrivateIPAddress</span></span>
<span data-ttu-id="c242d-129">Specifica l'indirizzo IP privato che questo cmdlet associa all'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c242d-129">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="c242d-130">Questa operazione può essere specificata solo se è specificata una subnet.</span><span class="sxs-lookup"><span data-stu-id="c242d-130">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="c242d-131">Questo IP viene allocato in modo statico dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="c242d-131">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="c242d-132">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="c242d-132">-PublicIPAddress</span></span>
<span data-ttu-id="c242d-133">Specifica l'oggetto indirizzo IP pubblico che questo cmdlet associa all'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c242d-133">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c242d-134">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="c242d-134">-PublicIPAddressId</span></span>
<span data-ttu-id="c242d-135">Specifica l'ID indirizzo IP pubblico che questo cmdlet associa all'IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c242d-135">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="c242d-136">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c242d-136">-Subnet</span></span>
<span data-ttu-id="c242d-137">Specifica l'oggetto subnet che questo cmdlet associa all'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c242d-137">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="c242d-138">Se specifichi questo parametro, significa che il gateway usa un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="c242d-138">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="c242d-139">Se il parametro *PrivateIPAddresss* è specificato, deve appartenere alla subnet specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c242d-139">If the *PrivateIPAddresss* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="c242d-140">Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene selezionato in modo dinamico come indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c242d-140">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c242d-141">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c242d-141">-SubnetId</span></span>
<span data-ttu-id="c242d-142">Specifica l'ID subnet che questo cmdlet associa alla configurazione IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c242d-142">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="c242d-143">Se specifichi il parametro *subnet* , significa che il gateway usa un indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="c242d-143">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="c242d-144">Se il parametro *PrivateIPAddress* è specificato, deve appartenere alla subnet specificata dalla *Subnet*.</span><span class="sxs-lookup"><span data-stu-id="c242d-144">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="c242d-145">Se *PrivateIPAddress* non è specificato, uno degli indirizzi IP della subnet viene selezionato in modo dinamico come indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c242d-145">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c242d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c242d-146">-DefaultProfile</span></span>
<span data-ttu-id="c242d-147">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c242d-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c242d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c242d-148">CommonParameters</span></span>
<span data-ttu-id="c242d-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c242d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c242d-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c242d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c242d-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c242d-151">INPUTS</span></span>

### <span data-ttu-id="c242d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c242d-152">System.String</span></span>

## <span data-ttu-id="c242d-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c242d-153">OUTPUTS</span></span>

### <span data-ttu-id="c242d-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c242d-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="c242d-155">Note</span><span class="sxs-lookup"><span data-stu-id="c242d-155">NOTES</span></span>

## <span data-ttu-id="c242d-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c242d-156">RELATED LINKS</span></span>

[<span data-ttu-id="c242d-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c242d-157">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c242d-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c242d-158">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c242d-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c242d-159">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c242d-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c242d-160">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


