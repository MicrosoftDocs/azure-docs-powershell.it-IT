---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
ms.openlocfilehash: a86e5346078bd1a8c9be924cdeac3b94fab907dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513208"
---
# <span data-ttu-id="2aca7-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2aca7-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="2aca7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2aca7-102">SYNOPSIS</span></span>
<span data-ttu-id="2aca7-103">Imposta lo stato dell'obiettivo per una route.</span><span class="sxs-lookup"><span data-stu-id="2aca7-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aca7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2aca7-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2aca7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2aca7-105">DESCRIPTION</span></span>
<span data-ttu-id="2aca7-106">Il cmdlet **set-AzureRmRouteConfig** imposta lo stato dell'obiettivo per una route di Azure.</span><span class="sxs-lookup"><span data-stu-id="2aca7-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="2aca7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2aca7-107">EXAMPLES</span></span>

### <span data-ttu-id="2aca7-108">Esempio 1: modificare una route</span><span class="sxs-lookup"><span data-stu-id="2aca7-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
Name              : Routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"58c2922e-9efe-4554-a457-956ef44bc718"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/Routetable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.4.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="2aca7-109">Questo comando consente di ottenere la tabella route denominata RouteTable01 usando il cmdlet Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="2aca7-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="2aca7-110">Il comando passa la tabella al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="2aca7-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2aca7-111">Il cmdlet Current modifica la route denominata Route02 e quindi passa il risultato al cmdlet **set-AzureRmRouteTable** , che aggiorna la tabella in base alle modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="2aca7-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="2aca7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2aca7-112">PARAMETERS</span></span>

### <span data-ttu-id="2aca7-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2aca7-113">-AddressPrefix</span></span>
<span data-ttu-id="2aca7-114">Specifica la destinazione, in formato CIDR (classe Interdomain Routing) a cui si applica la route.</span><span class="sxs-lookup"><span data-stu-id="2aca7-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="2aca7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2aca7-115">-Name</span></span>
<span data-ttu-id="2aca7-116">Specifica il nome della route che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="2aca7-116">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2aca7-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="2aca7-117">-NextHopIpAddress</span></span>
<span data-ttu-id="2aca7-118">Specifica l'indirizzo IP di un'appliance virtuale che si aggiunge alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="2aca7-118">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="2aca7-119">Questa route inoltra i pacchetti a quell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="2aca7-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="2aca7-120">Specifica questo parametro solo se specifichi un valore di VirtualAppliance per il parametro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="2aca7-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="2aca7-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="2aca7-121">-NextHopType</span></span>
<span data-ttu-id="2aca7-122">Specifica il modo in cui questa route inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="2aca7-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="2aca7-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2aca7-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2aca7-124">Internet.</span><span class="sxs-lookup"><span data-stu-id="2aca7-124">Internet.</span></span>
<span data-ttu-id="2aca7-125">Il gateway Internet predefinito fornito da Azure.</span><span class="sxs-lookup"><span data-stu-id="2aca7-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="2aca7-126">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="2aca7-126">None.</span></span>
<span data-ttu-id="2aca7-127">Se specifichi questo valore, la route non inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="2aca7-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="2aca7-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="2aca7-128">VirtualAppliance.</span></span>
<span data-ttu-id="2aca7-129">Un'appliance virtuale aggiunta alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="2aca7-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="2aca7-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="2aca7-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="2aca7-131">Un gateway di rete privata virtuale Azureserver-to-server.</span><span class="sxs-lookup"><span data-stu-id="2aca7-131">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="2aca7-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="2aca7-132">VnetLocal.</span></span>
<span data-ttu-id="2aca7-133">Rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="2aca7-133">The local virtual network.</span></span>
<span data-ttu-id="2aca7-134">Se sono presenti due subnet, 10.1.0.0/16 e 10.2.0.0/16 nella stessa rete virtuale, selezionare un valore di VnetLocal per ogni subnet da inoltrare all'altra subnet.</span><span class="sxs-lookup"><span data-stu-id="2aca7-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="2aca7-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2aca7-135">-RouteTable</span></span>
<span data-ttu-id="2aca7-136">Specifica la tabella route a cui è associata questa route.</span><span class="sxs-lookup"><span data-stu-id="2aca7-136">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aca7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aca7-137">-DefaultProfile</span></span>
<span data-ttu-id="2aca7-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2aca7-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aca7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aca7-139">CommonParameters</span></span>
<span data-ttu-id="2aca7-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aca7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aca7-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aca7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aca7-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2aca7-142">INPUTS</span></span>

### <span data-ttu-id="2aca7-143">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2aca7-143">PSRouteTable</span></span>
<span data-ttu-id="2aca7-144">Il parametro ' RouteTable ' accetta il valore di tipo ' PSRouteTable ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2aca7-144">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="2aca7-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2aca7-145">OUTPUTS</span></span>

### <span data-ttu-id="2aca7-146">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2aca7-146">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="2aca7-147">Note</span><span class="sxs-lookup"><span data-stu-id="2aca7-147">NOTES</span></span>

## <span data-ttu-id="2aca7-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2aca7-148">RELATED LINKS</span></span>

[<span data-ttu-id="2aca7-149">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2aca7-149">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="2aca7-150">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2aca7-150">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="2aca7-151">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2aca7-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="2aca7-152">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2aca7-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)


