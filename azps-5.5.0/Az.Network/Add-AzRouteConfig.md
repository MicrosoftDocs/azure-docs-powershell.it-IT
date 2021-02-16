---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 326baa91b8da8f9bae67cf47dcc69246549d7c06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203178"
---
# <span data-ttu-id="6096a-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6096a-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="6096a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6096a-102">SYNOPSIS</span></span>
<span data-ttu-id="6096a-103">Aggiunge un percorso a una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="6096a-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="6096a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6096a-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6096a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6096a-105">DESCRIPTION</span></span>
<span data-ttu-id="6096a-106">Il cmdlet **Add-AzRouteConfig** aggiunge una route a una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="6096a-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="6096a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6096a-107">EXAMPLES</span></span>

### <span data-ttu-id="6096a-108">Esempio 1: Aggiungere un percorso a una tabella di route</span><span class="sxs-lookup"><span data-stu-id="6096a-108">Example 1: Add a route to a route table</span></span>
```powershell
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="6096a-109">Il primo comando ottiene una tabella di route denominata RouteTable01 usando il cmdlet Get-AzRouteTable route.</span><span class="sxs-lookup"><span data-stu-id="6096a-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="6096a-110">Il comando archivia la tabella nella $RouteTable variabile.</span><span class="sxs-lookup"><span data-stu-id="6096a-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="6096a-111">Il secondo comando aggiunge una route denominata Route13 alla tabella di route archiviata in $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="6096a-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="6096a-112">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="6096a-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="6096a-113">Esempio 2: Aggiungere una route a una tabella di route usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="6096a-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```powershell
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="6096a-114">Questo comando recupera la tabella di route denominata RouteTable01 **usando Get-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="6096a-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="6096a-115">Il comando passa la tabella al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="6096a-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6096a-116">Il cmdlet corrente aggiunge la route denominata Route02 e quindi passa il risultato al cmdlet **Set-AzRouteTable,** che aggiorna la tabella per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="6096a-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="6096a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6096a-117">PARAMETERS</span></span>

### <span data-ttu-id="6096a-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6096a-118">-AddressPrefix</span></span>
<span data-ttu-id="6096a-119">Specifica la destinazione, in Classless Interdomain Routing (CIDR), a cui si applica la route.</span><span class="sxs-lookup"><span data-stu-id="6096a-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="6096a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6096a-120">-DefaultProfile</span></span>
<span data-ttu-id="6096a-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6096a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6096a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6096a-122">-Name</span></span>
<span data-ttu-id="6096a-123">Specifica un nome della route da aggiungere alla tabella di route.</span><span class="sxs-lookup"><span data-stu-id="6096a-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="6096a-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="6096a-124">-NextHopIpAddress</span></span>
<span data-ttu-id="6096a-125">Specifica l'indirizzo IP di un'appliance virtuale che si aggiunge alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="6096a-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="6096a-126">Questa route inoltra i pacchetti a tale indirizzo.</span><span class="sxs-lookup"><span data-stu-id="6096a-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="6096a-127">Specificare questo parametro solo se si specifica un valore di VirtualAppliance per il *parametro NextHopType.*</span><span class="sxs-lookup"><span data-stu-id="6096a-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="6096a-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="6096a-128">-NextHopType</span></span>
<span data-ttu-id="6096a-129">Specifica in che modo questa route inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="6096a-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="6096a-130">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="6096a-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6096a-131">Internet.</span><span class="sxs-lookup"><span data-stu-id="6096a-131">Internet.</span></span>
<span data-ttu-id="6096a-132">Gateway Internet predefinito fornito da Azure.</span><span class="sxs-lookup"><span data-stu-id="6096a-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="6096a-133">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="6096a-133">None.</span></span>
<span data-ttu-id="6096a-134">Se si specifica questo valore, la route non inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="6096a-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="6096a-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="6096a-135">VirtualAppliance.</span></span>
<span data-ttu-id="6096a-136">Un'appliance virtuale aggiunta alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="6096a-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="6096a-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="6096a-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="6096a-138">Gateway di rete privata virtuale da server a server di Azure.</span><span class="sxs-lookup"><span data-stu-id="6096a-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="6096a-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="6096a-139">VnetLocal.</span></span>
<span data-ttu-id="6096a-140">La rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="6096a-140">The local virtual network.</span></span>
<span data-ttu-id="6096a-141">Se si hanno due subnet, 10.1.0.0/16 e 10.2.0.0/16 nella stessa rete virtuale, selezionare un valore VnetLocal per ogni subnet da inoltrare all'altra subnet.</span><span class="sxs-lookup"><span data-stu-id="6096a-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="6096a-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="6096a-142">-RouteTable</span></span>
<span data-ttu-id="6096a-143">Specifica la tabella di route a cui questo cmdlet aggiunge una route.</span><span class="sxs-lookup"><span data-stu-id="6096a-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="6096a-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6096a-144">-Confirm</span></span>
<span data-ttu-id="6096a-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6096a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6096a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6096a-146">-WhatIf</span></span>
<span data-ttu-id="6096a-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6096a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6096a-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6096a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6096a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6096a-149">CommonParameters</span></span>
<span data-ttu-id="6096a-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6096a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6096a-151">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6096a-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6096a-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="6096a-152">INPUTS</span></span>

### <span data-ttu-id="6096a-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="6096a-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="6096a-154">System.String</span><span class="sxs-lookup"><span data-stu-id="6096a-154">System.String</span></span>

## <span data-ttu-id="6096a-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6096a-155">OUTPUTS</span></span>

### <span data-ttu-id="6096a-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="6096a-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="6096a-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="6096a-157">NOTES</span></span>

## <span data-ttu-id="6096a-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6096a-158">RELATED LINKS</span></span>

[<span data-ttu-id="6096a-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6096a-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="6096a-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="6096a-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="6096a-161">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6096a-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="6096a-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6096a-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="6096a-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6096a-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="6096a-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="6096a-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


