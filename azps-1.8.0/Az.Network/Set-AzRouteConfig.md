---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: ea0346ccae552a4167c545e36995ba4e8bca05fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677933"
---
# <span data-ttu-id="57b41-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="57b41-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="57b41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57b41-102">SYNOPSIS</span></span>
<span data-ttu-id="57b41-103">Aggiorna una configurazione della route per una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="57b41-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="57b41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57b41-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57b41-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57b41-105">DESCRIPTION</span></span>
<span data-ttu-id="57b41-106">Il cmdlet **set-AzRouteConfig** aggiorna una configurazione della route per una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="57b41-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="57b41-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57b41-107">EXAMPLES</span></span>

### <span data-ttu-id="57b41-108">Esempio 1: modificare una route</span><span class="sxs-lookup"><span data-stu-id="57b41-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
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

<span data-ttu-id="57b41-109">Questo comando consente di ottenere la tabella route denominata RouteTable01 usando il cmdlet Get-AzRouteTable.</span><span class="sxs-lookup"><span data-stu-id="57b41-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="57b41-110">Il comando passa la tabella al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="57b41-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="57b41-111">Il cmdlet Current modifica la route denominata Route02 e quindi passa il risultato al cmdlet **set-AzRouteTable** , che aggiorna la tabella in base alle modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="57b41-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="57b41-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57b41-112">PARAMETERS</span></span>

### <span data-ttu-id="57b41-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="57b41-113">-AddressPrefix</span></span>
<span data-ttu-id="57b41-114">Specifica la destinazione, in formato CIDR (classe Interdomain Routing) a cui si applica la route.</span><span class="sxs-lookup"><span data-stu-id="57b41-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57b41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b41-115">-DefaultProfile</span></span>
<span data-ttu-id="57b41-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57b41-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57b41-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="57b41-117">-Name</span></span>
<span data-ttu-id="57b41-118">Specifica il nome della route che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="57b41-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="57b41-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="57b41-119">-NextHopIpAddress</span></span>
<span data-ttu-id="57b41-120">Specifica l'indirizzo IP di un'appliance virtuale che si aggiunge alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="57b41-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="57b41-121">Questa route inoltra i pacchetti a quell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="57b41-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="57b41-122">Specifica questo parametro solo se specifichi un valore di VirtualAppliance per il parametro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="57b41-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57b41-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="57b41-123">-NextHopType</span></span>
<span data-ttu-id="57b41-124">Specifica il modo in cui questa route inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="57b41-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="57b41-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="57b41-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="57b41-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="57b41-126">Internet.</span></span>
<span data-ttu-id="57b41-127">Il gateway Internet predefinito fornito da Azure.</span><span class="sxs-lookup"><span data-stu-id="57b41-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="57b41-128">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="57b41-128">None.</span></span>
<span data-ttu-id="57b41-129">Se specifichi questo valore, la route non inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="57b41-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="57b41-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="57b41-130">VirtualAppliance.</span></span>
<span data-ttu-id="57b41-131">Un'appliance virtuale aggiunta alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="57b41-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="57b41-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="57b41-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="57b41-133">Un gateway di rete privata virtuale Azureserver-to-server.</span><span class="sxs-lookup"><span data-stu-id="57b41-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="57b41-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="57b41-134">VnetLocal.</span></span>
<span data-ttu-id="57b41-135">Rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="57b41-135">The local virtual network.</span></span>
<span data-ttu-id="57b41-136">Se sono presenti due subnet, 10.1.0.0/16 e 10.2.0.0/16 nella stessa rete virtuale, selezionare un valore di VnetLocal per ogni subnet da inoltrare all'altra subnet.</span><span class="sxs-lookup"><span data-stu-id="57b41-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57b41-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="57b41-137">-RouteTable</span></span>
<span data-ttu-id="57b41-138">Specifica la tabella route a cui è associata questa route.</span><span class="sxs-lookup"><span data-stu-id="57b41-138">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57b41-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="57b41-139">-Confirm</span></span>
<span data-ttu-id="57b41-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57b41-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b41-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57b41-141">-WhatIf</span></span>
<span data-ttu-id="57b41-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57b41-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57b41-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57b41-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b41-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b41-144">CommonParameters</span></span>
<span data-ttu-id="57b41-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57b41-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b41-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57b41-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b41-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57b41-147">INPUTS</span></span>

### <span data-ttu-id="57b41-148">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="57b41-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="57b41-149">System. String</span><span class="sxs-lookup"><span data-stu-id="57b41-149">System.String</span></span>

## <span data-ttu-id="57b41-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57b41-150">OUTPUTS</span></span>

### <span data-ttu-id="57b41-151">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="57b41-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="57b41-152">Note</span><span class="sxs-lookup"><span data-stu-id="57b41-152">NOTES</span></span>

## <span data-ttu-id="57b41-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57b41-153">RELATED LINKS</span></span>

[<span data-ttu-id="57b41-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="57b41-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="57b41-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="57b41-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="57b41-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="57b41-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="57b41-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="57b41-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


