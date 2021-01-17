---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: d9c7b4895d05b4f55ef91705062db7c200d702cf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474487"
---
# <span data-ttu-id="eb7da-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb7da-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="eb7da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb7da-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7da-103">Crea una risorsa della tabella route Hub associata a un VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="eb7da-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="eb7da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb7da-104">SYNTAX</span></span>

### <span data-ttu-id="eb7da-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb7da-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb7da-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="eb7da-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb7da-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="eb7da-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb7da-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb7da-108">DESCRIPTION</span></span>
<span data-ttu-id="eb7da-109">Crea la tabella di route specificata associata all'hub virtuale specificato con le route e le etichette fornite.</span><span class="sxs-lookup"><span data-stu-id="eb7da-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="eb7da-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb7da-110">EXAMPLES</span></span>

### <span data-ttu-id="eb7da-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eb7da-111">Example 1</span></span>

```powershell
PS C:\> New-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan" -Location "westcentralus" -VirtualWANType "Standard" -AllowVnetToVnetTraffic -AllowBranchToBranchTraffic
PS C:\> $virtualWan = Get-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan"

PS C:\> New-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub" -Location "westcentralus" -AddressPrefix "10.0.0.0/16" -VirtualWan $virtualWan
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub"

PS C:\> $fwIp = New-AzFirewallHubPublicIpAddress -Count 1
PS C:\> $hubIpAddresses = New-AzFirewallHubIpAddress -PublicIP $fwIp
PS C:\> New-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg" -Location "westcentralus" -Sku AZFW_Hub -VirtualHubId $virtualHub.Id -HubIPAddress $hubIpAddresses
PS C:\> $firewall = Get-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg"

PS C:\> $route1 = New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> New-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route1) -Label @("testLabel")

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "private-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "10.30.0.0/16",
                               "10.40.0.0/16"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="eb7da-112">Questo comando crea una tabella di route Hub dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb7da-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="eb7da-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb7da-113">PARAMETERS</span></span>

### <span data-ttu-id="eb7da-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb7da-114">-AsJob</span></span>
<span data-ttu-id="eb7da-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="eb7da-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7da-116">-DefaultProfile</span></span>
<span data-ttu-id="eb7da-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb7da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7da-118">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="eb7da-118">-Label</span></span>
<span data-ttu-id="eb7da-119">Elenco di etichette.</span><span class="sxs-lookup"><span data-stu-id="eb7da-119">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7da-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb7da-120">-Name</span></span>
<span data-ttu-id="eb7da-121">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb7da-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7da-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="eb7da-122">-ParentObject</span></span>
<span data-ttu-id="eb7da-123">L'oggetto hub virtuale padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb7da-123">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7da-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="eb7da-124">-ParentResourceName</span></span>
<span data-ttu-id="eb7da-125">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="eb7da-125">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7da-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb7da-126">-ResourceGroupName</span></span>
<span data-ttu-id="eb7da-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eb7da-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7da-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="eb7da-128">-ParentResourceId</span></span>
<span data-ttu-id="eb7da-129">ID risorsa della risorsa hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb7da-129">The resource id of the virtual hub resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7da-130">-Route</span><span class="sxs-lookup"><span data-stu-id="eb7da-130">-Route</span></span>
<span data-ttu-id="eb7da-131">Elenco di route per questa tabella di route.</span><span class="sxs-lookup"><span data-stu-id="eb7da-131">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7da-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eb7da-132">-Confirm</span></span>
<span data-ttu-id="eb7da-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb7da-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb7da-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb7da-134">-WhatIf</span></span>
<span data-ttu-id="eb7da-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb7da-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb7da-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb7da-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb7da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7da-137">CommonParameters</span></span>
<span data-ttu-id="eb7da-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb7da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7da-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb7da-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7da-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb7da-140">INPUTS</span></span>

### <span data-ttu-id="eb7da-141">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="eb7da-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="eb7da-142">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb7da-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="eb7da-143">System. String</span><span class="sxs-lookup"><span data-stu-id="eb7da-143">System.String</span></span>

## <span data-ttu-id="eb7da-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb7da-144">OUTPUTS</span></span>

### <span data-ttu-id="eb7da-145">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb7da-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="eb7da-146">Note</span><span class="sxs-lookup"><span data-stu-id="eb7da-146">NOTES</span></span>

## <span data-ttu-id="eb7da-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb7da-147">RELATED LINKS</span></span>

[<span data-ttu-id="eb7da-148">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb7da-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="eb7da-149">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="eb7da-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="eb7da-150">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb7da-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="eb7da-151">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb7da-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
