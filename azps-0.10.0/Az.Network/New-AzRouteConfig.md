---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 1311c229b670af3ffd049f3f13b3460fb0631628
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860437"
---
# <span data-ttu-id="06df8-101">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="06df8-101">New-AzRouteConfig</span></span>

## <span data-ttu-id="06df8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06df8-102">SYNOPSIS</span></span>
<span data-ttu-id="06df8-103">Crea una route per una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="06df8-103">Creates a route for a route table.</span></span>

## <span data-ttu-id="06df8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06df8-104">SYNTAX</span></span>

```
New-AzRouteConfig [-AddressPrefix <String>] [-NextHopType <String>] [-NextHopIpAddress <String>]
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06df8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06df8-105">DESCRIPTION</span></span>
<span data-ttu-id="06df8-106">Il cmdlet **New-AzRouteConfig** crea una route per una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="06df8-106">The **New-AzRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="06df8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06df8-107">EXAMPLES</span></span>

### <span data-ttu-id="06df8-108">Esempio 1: creare una route</span><span class="sxs-lookup"><span data-stu-id="06df8-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="06df8-109">Il primo comando crea una route denominata Route07 e la archivia nella variabile $Route.</span><span class="sxs-lookup"><span data-stu-id="06df8-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="06df8-110">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="06df8-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="06df8-111">Il secondo comando Visualizza le proprietà della route.</span><span class="sxs-lookup"><span data-stu-id="06df8-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="06df8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06df8-112">PARAMETERS</span></span>

### <span data-ttu-id="06df8-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="06df8-113">-AddressPrefix</span></span>
<span data-ttu-id="06df8-114">Specifica la destinazione, in formato CIDR (classe Interdomain Routing) a cui si applica la route.</span><span class="sxs-lookup"><span data-stu-id="06df8-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06df8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06df8-115">-DefaultProfile</span></span>
<span data-ttu-id="06df8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06df8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06df8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="06df8-117">-Name</span></span>
<span data-ttu-id="06df8-118">Specifica un nome per la route.</span><span class="sxs-lookup"><span data-stu-id="06df8-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="06df8-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="06df8-119">-NextHopIpAddress</span></span>
<span data-ttu-id="06df8-120">Specifica l'indirizzo IP di un'appliance virtuale aggiunta alla rete Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="06df8-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="06df8-121">Questa route inoltra i pacchetti a quell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="06df8-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="06df8-122">Specifica questo parametro solo se specifichi un valore di VirtualAppliance per il parametro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="06df8-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06df8-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="06df8-123">-NextHopType</span></span>
<span data-ttu-id="06df8-124">Specifica il modo in cui questa route inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="06df8-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="06df8-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="06df8-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06df8-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="06df8-126">Internet.</span></span>
<span data-ttu-id="06df8-127">Il gateway Internet predefinito fornito da Azure.</span><span class="sxs-lookup"><span data-stu-id="06df8-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="06df8-128">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="06df8-128">None.</span></span>
<span data-ttu-id="06df8-129">Se specifichi questo valore, la route non inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="06df8-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="06df8-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="06df8-130">VirtualAppliance.</span></span>
<span data-ttu-id="06df8-131">Un'appliance virtuale aggiunta alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="06df8-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="06df8-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="06df8-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="06df8-133">Un gateway di rete privata virtuale di Azure da server a server.</span><span class="sxs-lookup"><span data-stu-id="06df8-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="06df8-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="06df8-134">VnetLocal.</span></span>
<span data-ttu-id="06df8-135">Rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="06df8-135">The local virtual network.</span></span>
<span data-ttu-id="06df8-136">Se sono presenti due subnet, 10.1.0.0/16 e 10.2.0.0/16 nella stessa rete virtuale, selezionare un valore di VnetLocal per ogni subnet da inoltrare all'altra subnet.</span><span class="sxs-lookup"><span data-stu-id="06df8-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06df8-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06df8-137">-Confirm</span></span>
<span data-ttu-id="06df8-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06df8-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06df8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06df8-139">-WhatIf</span></span>
<span data-ttu-id="06df8-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06df8-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06df8-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06df8-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06df8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06df8-142">CommonParameters</span></span>
<span data-ttu-id="06df8-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06df8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06df8-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06df8-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06df8-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06df8-145">INPUTS</span></span>

## <span data-ttu-id="06df8-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06df8-146">OUTPUTS</span></span>

### <span data-ttu-id="06df8-147">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="06df8-147">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="06df8-148">Note</span><span class="sxs-lookup"><span data-stu-id="06df8-148">NOTES</span></span>

## <span data-ttu-id="06df8-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06df8-149">RELATED LINKS</span></span>

[<span data-ttu-id="06df8-150">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="06df8-150">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="06df8-151">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="06df8-151">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="06df8-152">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="06df8-152">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="06df8-153">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="06df8-153">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


