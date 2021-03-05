---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: a4cdcbf52dfb20f0282347d5dc1ce9a5aec14da0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990918"
---
# <span data-ttu-id="7650a-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7650a-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="7650a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7650a-102">SYNOPSIS</span></span>
<span data-ttu-id="7650a-103">Aggiorna la configurazione di una route per una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="7650a-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="7650a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7650a-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7650a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7650a-105">DESCRIPTION</span></span>
<span data-ttu-id="7650a-106">Il cmdlet **Set-AzRouteConfig** aggiorna la configurazione di una route per una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="7650a-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="7650a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7650a-107">EXAMPLES</span></span>

### <span data-ttu-id="7650a-108">Esempio 1: Modificare un percorso</span><span class="sxs-lookup"><span data-stu-id="7650a-108">Example 1: Modify a route</span></span>
```powershell
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

<span data-ttu-id="7650a-109">Questo comando recupera la tabella di route denominata RouteTable01 usando il cmdlet Get-AzRouteTable route.</span><span class="sxs-lookup"><span data-stu-id="7650a-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="7650a-110">Il comando passa la tabella al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="7650a-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7650a-111">Il cmdlet corrente modifica la route denominata Route02 e quindi passa il risultato al cmdlet **Set-AzRouteTable,** che aggiorna la tabella per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="7650a-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="7650a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7650a-112">PARAMETERS</span></span>

### <span data-ttu-id="7650a-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7650a-113">-AddressPrefix</span></span>
<span data-ttu-id="7650a-114">Specifica la destinazione, in Classless Interdomain Routing (CIDR), a cui si applica la route.</span><span class="sxs-lookup"><span data-stu-id="7650a-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="7650a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7650a-115">-DefaultProfile</span></span>
<span data-ttu-id="7650a-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7650a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7650a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7650a-117">-Name</span></span>
<span data-ttu-id="7650a-118">Specifica il nome della route modificata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7650a-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7650a-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="7650a-119">-NextHopIpAddress</span></span>
<span data-ttu-id="7650a-120">Specifica l'indirizzo IP di un'appliance virtuale aggiunto alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7650a-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="7650a-121">Questa route inoltra i pacchetti a tale indirizzo.</span><span class="sxs-lookup"><span data-stu-id="7650a-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="7650a-122">Specificare questo parametro solo se si specifica un valore di VirtualAppliance per il *parametro NextHopType.*</span><span class="sxs-lookup"><span data-stu-id="7650a-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="7650a-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="7650a-123">-NextHopType</span></span>
<span data-ttu-id="7650a-124">Specifica in che modo questa route inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="7650a-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="7650a-125">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="7650a-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7650a-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="7650a-126">Internet.</span></span>
<span data-ttu-id="7650a-127">Gateway Internet predefinito fornito da Azure.</span><span class="sxs-lookup"><span data-stu-id="7650a-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="7650a-128">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="7650a-128">None.</span></span>
<span data-ttu-id="7650a-129">Se si specifica questo valore, la route non inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="7650a-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="7650a-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="7650a-130">VirtualAppliance.</span></span>
<span data-ttu-id="7650a-131">Un'appliance virtuale aggiunta alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7650a-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="7650a-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="7650a-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="7650a-133">Gateway di rete privata virtuale Azureserver-to-server.</span><span class="sxs-lookup"><span data-stu-id="7650a-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="7650a-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="7650a-134">VnetLocal.</span></span>
<span data-ttu-id="7650a-135">La rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="7650a-135">The local virtual network.</span></span>
<span data-ttu-id="7650a-136">Se si hanno due subnet, 10.1.0.0/16 e 10.2.0.0/16 nella stessa rete virtuale, selezionare un valore VnetLocal per ogni subnet da inoltrare all'altra subnet.</span><span class="sxs-lookup"><span data-stu-id="7650a-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="7650a-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="7650a-137">-RouteTable</span></span>
<span data-ttu-id="7650a-138">Specifica la tabella di route a cui è associata la route.</span><span class="sxs-lookup"><span data-stu-id="7650a-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="7650a-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7650a-139">-Confirm</span></span>
<span data-ttu-id="7650a-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7650a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7650a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7650a-141">-WhatIf</span></span>
<span data-ttu-id="7650a-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7650a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7650a-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7650a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7650a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7650a-144">CommonParameters</span></span>
<span data-ttu-id="7650a-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7650a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7650a-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7650a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7650a-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="7650a-147">INPUTS</span></span>

### <span data-ttu-id="7650a-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7650a-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="7650a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="7650a-149">System.String</span></span>

## <span data-ttu-id="7650a-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7650a-150">OUTPUTS</span></span>

### <span data-ttu-id="7650a-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7650a-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="7650a-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="7650a-152">NOTES</span></span>

## <span data-ttu-id="7650a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7650a-153">RELATED LINKS</span></span>

[<span data-ttu-id="7650a-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7650a-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="7650a-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7650a-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="7650a-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7650a-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="7650a-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7650a-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


