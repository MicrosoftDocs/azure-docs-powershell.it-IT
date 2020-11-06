---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: bb51d5bfb1ccc81aa10c7aecc4d7a255fc0f60d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513271"
---
# <span data-ttu-id="4bceb-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4bceb-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="4bceb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4bceb-102">SYNOPSIS</span></span>
<span data-ttu-id="4bceb-103">Crea una route per una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="4bceb-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bceb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bceb-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig -Name <String> [-AddressPrefix <String>] -NextHopType <String>
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bceb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bceb-105">DESCRIPTION</span></span>
<span data-ttu-id="4bceb-106">Il cmdlet **New-AzureRmRouteConfig** crea una route per una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="4bceb-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="4bceb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bceb-107">EXAMPLES</span></span>

### <span data-ttu-id="4bceb-108">Esempio 1: creare una route</span><span class="sxs-lookup"><span data-stu-id="4bceb-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="4bceb-109">Il primo comando crea una route denominata Route07 e la archivia nella variabile $Route.</span><span class="sxs-lookup"><span data-stu-id="4bceb-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="4bceb-110">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="4bceb-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="4bceb-111">Il secondo comando Visualizza le proprietà della route.</span><span class="sxs-lookup"><span data-stu-id="4bceb-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="4bceb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4bceb-112">PARAMETERS</span></span>

### <span data-ttu-id="4bceb-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4bceb-113">-AddressPrefix</span></span>
<span data-ttu-id="4bceb-114">Specifica la destinazione, in formato CIDR (classe Interdomain Routing) a cui si applica la route.</span><span class="sxs-lookup"><span data-stu-id="4bceb-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="4bceb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4bceb-115">-Name</span></span>
<span data-ttu-id="4bceb-116">Specifica un nome per la route.</span><span class="sxs-lookup"><span data-stu-id="4bceb-116">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="4bceb-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="4bceb-117">-NextHopIpAddress</span></span>
<span data-ttu-id="4bceb-118">Specifica l'indirizzo IP di un'appliance virtuale aggiunta alla rete Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="4bceb-118">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="4bceb-119">Questa route inoltra i pacchetti a quell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="4bceb-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="4bceb-120">Specifica questo parametro solo se specifichi un valore di VirtualAppliance per il parametro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="4bceb-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="4bceb-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="4bceb-121">-NextHopType</span></span>
<span data-ttu-id="4bceb-122">Specifica il modo in cui questa route inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="4bceb-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="4bceb-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4bceb-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4bceb-124">Internet.</span><span class="sxs-lookup"><span data-stu-id="4bceb-124">Internet.</span></span>
<span data-ttu-id="4bceb-125">Il gateway Internet predefinito fornito da Azure.</span><span class="sxs-lookup"><span data-stu-id="4bceb-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="4bceb-126">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="4bceb-126">None.</span></span>
<span data-ttu-id="4bceb-127">Se specifichi questo valore, la route non inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="4bceb-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="4bceb-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="4bceb-128">VirtualAppliance.</span></span>
<span data-ttu-id="4bceb-129">Un'appliance virtuale aggiunta alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="4bceb-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="4bceb-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="4bceb-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="4bceb-131">Un gateway di rete privata virtuale di Azure da server a server.</span><span class="sxs-lookup"><span data-stu-id="4bceb-131">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="4bceb-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="4bceb-132">VnetLocal.</span></span>
<span data-ttu-id="4bceb-133">Rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="4bceb-133">The local virtual network.</span></span>
<span data-ttu-id="4bceb-134">Se sono presenti due subnet, 10.1.0.0/16 e 10.2.0.0/16 nella stessa rete virtuale, selezionare un valore di VnetLocal per ogni subnet da inoltrare all'altra subnet.</span><span class="sxs-lookup"><span data-stu-id="4bceb-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, None, VirtualAppliance, VirtualNetworkGateway, VnetLocal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bceb-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bceb-135">-DefaultProfile</span></span>
<span data-ttu-id="4bceb-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4bceb-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bceb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bceb-137">CommonParameters</span></span>
<span data-ttu-id="4bceb-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bceb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bceb-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bceb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bceb-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4bceb-140">INPUTS</span></span>

## <span data-ttu-id="4bceb-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bceb-141">OUTPUTS</span></span>

### <span data-ttu-id="4bceb-142">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="4bceb-142">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="4bceb-143">Note</span><span class="sxs-lookup"><span data-stu-id="4bceb-143">NOTES</span></span>

## <span data-ttu-id="4bceb-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bceb-144">RELATED LINKS</span></span>

[<span data-ttu-id="4bceb-145">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4bceb-145">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="4bceb-146">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4bceb-146">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="4bceb-147">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4bceb-147">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="4bceb-148">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4bceb-148">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


