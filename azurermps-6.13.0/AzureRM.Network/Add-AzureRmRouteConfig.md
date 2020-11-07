---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: 10018ad3a58de005ecf5798aafaa610c4899d4d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688403"
---
# <span data-ttu-id="4b078-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4b078-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="4b078-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b078-102">SYNOPSIS</span></span>
<span data-ttu-id="4b078-103">Aggiunge una route a una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="4b078-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b078-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b078-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>]
 [-NextHopType <String>] [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b078-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b078-105">DESCRIPTION</span></span>
<span data-ttu-id="4b078-106">Il cmdlet **Add-AzureRmRouteConfig** aggiunge una route a una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b078-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="4b078-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b078-107">EXAMPLES</span></span>

### <span data-ttu-id="4b078-108">Esempio 1: aggiungere una route a una tabella di route</span><span class="sxs-lookup"><span data-stu-id="4b078-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="4b078-109">Il primo comando consente di ottenere una tabella di route denominata RouteTable01 usando il cmdlet Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="4b078-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="4b078-110">Il comando Archivia la tabella nella variabile $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="4b078-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="4b078-111">Il secondo comando aggiunge una route denominata Route13 alla tabella route archiviata in $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="4b078-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="4b078-112">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="4b078-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="4b078-113">Esempio 2: aggiungere una route a una tabella di route tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="4b078-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="4b078-114">Questo comando ottiene la tabella route denominata RouteTable01 utilizzando **Get-AzureRmRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="4b078-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="4b078-115">Il comando passa la tabella al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="4b078-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4b078-116">Il cmdlet corrente aggiunge la route denominata Route02 e quindi passa il risultato al cmdlet **set-AzureRmRouteTable** , che aggiorna la tabella per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="4b078-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="4b078-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b078-117">PARAMETERS</span></span>

### <span data-ttu-id="4b078-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4b078-118">-AddressPrefix</span></span>
<span data-ttu-id="4b078-119">Specifica la destinazione, in formato CIDR (classe Interdomain Routing) a cui si applica la route.</span><span class="sxs-lookup"><span data-stu-id="4b078-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="4b078-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b078-120">-DefaultProfile</span></span>
<span data-ttu-id="4b078-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b078-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b078-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b078-122">-Name</span></span>
<span data-ttu-id="4b078-123">Specifica un nome della route da aggiungere alla tabella di route.</span><span class="sxs-lookup"><span data-stu-id="4b078-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="4b078-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="4b078-124">-NextHopIpAddress</span></span>
<span data-ttu-id="4b078-125">Specifica l'indirizzo IP di un'appliance virtuale che si aggiunge alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b078-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="4b078-126">Questa route inoltra i pacchetti a quell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="4b078-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="4b078-127">Specifica questo parametro solo se specifichi un valore di VirtualAppliance per il parametro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="4b078-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="4b078-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="4b078-128">-NextHopType</span></span>
<span data-ttu-id="4b078-129">Specifica il modo in cui questa route inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="4b078-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="4b078-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b078-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4b078-131">Internet.</span><span class="sxs-lookup"><span data-stu-id="4b078-131">Internet.</span></span>
<span data-ttu-id="4b078-132">Il gateway Internet predefinito fornito da Azure.</span><span class="sxs-lookup"><span data-stu-id="4b078-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="4b078-133">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="4b078-133">None.</span></span>
<span data-ttu-id="4b078-134">Se specifichi questo valore, la route non inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="4b078-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="4b078-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="4b078-135">VirtualAppliance.</span></span>
<span data-ttu-id="4b078-136">Un'appliance virtuale aggiunta alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b078-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="4b078-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="4b078-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="4b078-138">Un gateway di rete privata virtuale di Azure da server a server.</span><span class="sxs-lookup"><span data-stu-id="4b078-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="4b078-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="4b078-139">VnetLocal.</span></span>
<span data-ttu-id="4b078-140">Rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="4b078-140">The local virtual network.</span></span>
<span data-ttu-id="4b078-141">Se sono presenti due subnet, 10.1.0.0/16 e 10.2.0.0/16 nella stessa rete virtuale, selezionare un valore di VnetLocal per ogni subnet da inoltrare all'altra subnet.</span><span class="sxs-lookup"><span data-stu-id="4b078-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="4b078-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4b078-142">-RouteTable</span></span>
<span data-ttu-id="4b078-143">Specifica la tabella di route a cui questo cmdlet aggiunge una route.</span><span class="sxs-lookup"><span data-stu-id="4b078-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="4b078-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b078-144">-Confirm</span></span>
<span data-ttu-id="4b078-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b078-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b078-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b078-146">-WhatIf</span></span>
<span data-ttu-id="4b078-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b078-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b078-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b078-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b078-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b078-149">CommonParameters</span></span>
<span data-ttu-id="4b078-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b078-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b078-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b078-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b078-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b078-152">INPUTS</span></span>

### <span data-ttu-id="4b078-153">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4b078-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="4b078-154">System. String</span><span class="sxs-lookup"><span data-stu-id="4b078-154">System.String</span></span>

## <span data-ttu-id="4b078-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b078-155">OUTPUTS</span></span>

### <span data-ttu-id="4b078-156">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4b078-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4b078-157">Note</span><span class="sxs-lookup"><span data-stu-id="4b078-157">NOTES</span></span>

## <span data-ttu-id="4b078-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b078-158">RELATED LINKS</span></span>

[<span data-ttu-id="4b078-159">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4b078-159">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="4b078-160">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4b078-160">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="4b078-161">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4b078-161">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="4b078-162">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4b078-162">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="4b078-163">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4b078-163">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="4b078-164">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4b078-164">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)

