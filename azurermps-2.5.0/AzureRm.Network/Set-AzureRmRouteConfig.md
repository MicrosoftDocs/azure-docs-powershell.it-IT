---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: 5aa84098c19595ac1c7d6b33c56dca20d08a475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866216"
---
# <span data-ttu-id="f13d3-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f13d3-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="f13d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f13d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f13d3-103">Imposta lo stato dell'obiettivo per una route.</span><span class="sxs-lookup"><span data-stu-id="f13d3-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f13d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f13d3-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f13d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f13d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f13d3-106">Il cmdlet **set-AzureRmRouteConfig** imposta lo stato dell'obiettivo per una route di Azure.</span><span class="sxs-lookup"><span data-stu-id="f13d3-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="f13d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f13d3-107">EXAMPLES</span></span>

### <span data-ttu-id="f13d3-108">Esempio 1: modificare una route</span><span class="sxs-lookup"><span data-stu-id="f13d3-108">Example 1: Modify a route</span></span>
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

<span data-ttu-id="f13d3-109">Questo comando consente di ottenere la tabella route denominata RouteTable01 usando il cmdlet Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="f13d3-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="f13d3-110">Il comando passa la tabella al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f13d3-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f13d3-111">Il cmdlet Current modifica la route denominata Route02 e quindi passa il risultato al cmdlet **set-AzureRmRouteTable** , che aggiorna la tabella in base alle modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="f13d3-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="f13d3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f13d3-112">PARAMETERS</span></span>

### <span data-ttu-id="f13d3-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f13d3-113">-AddressPrefix</span></span>
<span data-ttu-id="f13d3-114">Specifica la destinazione, in formato CIDR (classe Interdomain Routing) a cui si applica la route.</span><span class="sxs-lookup"><span data-stu-id="f13d3-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="f13d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f13d3-115">-DefaultProfile</span></span>
<span data-ttu-id="f13d3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f13d3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f13d3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f13d3-117">-Name</span></span>
<span data-ttu-id="f13d3-118">Specifica il nome della route che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="f13d3-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f13d3-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="f13d3-119">-NextHopIpAddress</span></span>
<span data-ttu-id="f13d3-120">Specifica l'indirizzo IP di un'appliance virtuale che si aggiunge alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f13d3-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="f13d3-121">Questa route inoltra i pacchetti a quell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="f13d3-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="f13d3-122">Specifica questo parametro solo se specifichi un valore di VirtualAppliance per il parametro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="f13d3-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="f13d3-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="f13d3-123">-NextHopType</span></span>
<span data-ttu-id="f13d3-124">Specifica il modo in cui questa route inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f13d3-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="f13d3-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f13d3-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f13d3-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="f13d3-126">Internet.</span></span>
<span data-ttu-id="f13d3-127">Il gateway Internet predefinito fornito da Azure.</span><span class="sxs-lookup"><span data-stu-id="f13d3-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="f13d3-128">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="f13d3-128">None.</span></span>
<span data-ttu-id="f13d3-129">Se specifichi questo valore, la route non inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f13d3-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="f13d3-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="f13d3-130">VirtualAppliance.</span></span>
<span data-ttu-id="f13d3-131">Un'appliance virtuale aggiunta alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f13d3-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="f13d3-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="f13d3-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="f13d3-133">Un gateway di rete privata virtuale Azureserver-to-server.</span><span class="sxs-lookup"><span data-stu-id="f13d3-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="f13d3-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="f13d3-134">VnetLocal.</span></span>
<span data-ttu-id="f13d3-135">Rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="f13d3-135">The local virtual network.</span></span>
<span data-ttu-id="f13d3-136">Se sono presenti due subnet, 10.1.0.0/16 e 10.2.0.0/16 nella stessa rete virtuale, selezionare un valore di VnetLocal per ogni subnet da inoltrare all'altra subnet.</span><span class="sxs-lookup"><span data-stu-id="f13d3-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="f13d3-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="f13d3-137">-RouteTable</span></span>
<span data-ttu-id="f13d3-138">Specifica la tabella route a cui è associata questa route.</span><span class="sxs-lookup"><span data-stu-id="f13d3-138">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f13d3-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f13d3-139">-Confirm</span></span>
<span data-ttu-id="f13d3-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f13d3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f13d3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f13d3-141">-WhatIf</span></span>
<span data-ttu-id="f13d3-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f13d3-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f13d3-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f13d3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f13d3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f13d3-144">CommonParameters</span></span>
<span data-ttu-id="f13d3-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f13d3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f13d3-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f13d3-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f13d3-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f13d3-147">INPUTS</span></span>

### <span data-ttu-id="f13d3-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f13d3-148">PSRouteTable</span></span>
<span data-ttu-id="f13d3-149">Il parametro ' RouteTable ' accetta il valore di tipo ' PSRouteTable ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f13d3-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="f13d3-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f13d3-150">OUTPUTS</span></span>

### <span data-ttu-id="f13d3-151">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f13d3-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="f13d3-152">Note</span><span class="sxs-lookup"><span data-stu-id="f13d3-152">NOTES</span></span>

## <span data-ttu-id="f13d3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f13d3-153">RELATED LINKS</span></span>

[<span data-ttu-id="f13d3-154">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f13d3-154">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="f13d3-155">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f13d3-155">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="f13d3-156">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f13d3-156">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="f13d3-157">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f13d3-157">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)


