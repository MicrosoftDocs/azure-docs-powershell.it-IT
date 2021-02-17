---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: d330b7e25cc1184a3efaea2c3deb569bf44171b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193286"
---
# <span data-ttu-id="43c9a-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="43c9a-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="43c9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="43c9a-103">Eliminare una risorsa tabella delle route dell'hub associata a un virtualhub.</span><span class="sxs-lookup"><span data-stu-id="43c9a-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="43c9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43c9a-104">SYNTAX</span></span>

### <span data-ttu-id="43c9a-105">ByVHubRouteTableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43c9a-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43c9a-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="43c9a-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43c9a-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="43c9a-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43c9a-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="43c9a-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43c9a-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="43c9a-109">DESCRIPTION</span></span>
<span data-ttu-id="43c9a-110">Aggiorna la tabella di route specificata associata all'hub virtuale specificato con le route o le etichette specificate.</span><span class="sxs-lookup"><span data-stu-id="43c9a-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="43c9a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43c9a-111">EXAMPLES</span></span>

### <span data-ttu-id="43c9a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="43c9a-112">Example 1</span></span>
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
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

PS C:\> $route2 = New-AzVHubRoute -Name "internet-traffic" -Destination @("0.0.0.0/0") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> Update-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route2)
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "internet-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "0.0.0.0/0"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="43c9a-113">Questo comando elimina la tabella delle route dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="43c9a-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="43c9a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43c9a-114">PARAMETERS</span></span>

### <span data-ttu-id="43c9a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43c9a-115">-AsJob</span></span>
<span data-ttu-id="43c9a-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="43c9a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43c9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c9a-117">-DefaultProfile</span></span>
<span data-ttu-id="43c9a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43c9a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43c9a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43c9a-119">-InputObject</span></span>
<span data-ttu-id="43c9a-120">La risorsa vhubroute per Update.</span><span class="sxs-lookup"><span data-stu-id="43c9a-120">The vhubroutetable resource to Update.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-121">-Label</span><span class="sxs-lookup"><span data-stu-id="43c9a-121">-Label</span></span>
<span data-ttu-id="43c9a-122">L'elenco di etichette.</span><span class="sxs-lookup"><span data-stu-id="43c9a-122">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="43c9a-123">-Name</span></span>
<span data-ttu-id="43c9a-124">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="43c9a-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="43c9a-125">-ParentObject</span></span>
<span data-ttu-id="43c9a-126">Oggetto hub virtuale padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="43c9a-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="43c9a-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="43c9a-127">-ParentResourceName</span></span>
<span data-ttu-id="43c9a-128">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="43c9a-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c9a-129">-ResourceGroupName</span></span>
<span data-ttu-id="43c9a-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43c9a-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43c9a-131">-ResourceId</span></span>
<span data-ttu-id="43c9a-132">ID risorsa della risorsa vhubroutetable da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="43c9a-132">The resource id of the vhubroutetable resource to Update.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-133">-Route</span><span class="sxs-lookup"><span data-stu-id="43c9a-133">-Route</span></span>
<span data-ttu-id="43c9a-134">Elenco dei percorsi per questa tabella di route.</span><span class="sxs-lookup"><span data-stu-id="43c9a-134">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c9a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43c9a-135">-Confirm</span></span>
<span data-ttu-id="43c9a-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43c9a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43c9a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43c9a-137">-WhatIf</span></span>
<span data-ttu-id="43c9a-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43c9a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43c9a-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43c9a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43c9a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c9a-140">CommonParameters</span></span>
<span data-ttu-id="43c9a-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c9a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c9a-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43c9a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c9a-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="43c9a-143">INPUTS</span></span>

### <span data-ttu-id="43c9a-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="43c9a-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="43c9a-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="43c9a-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="43c9a-146">System.String</span><span class="sxs-lookup"><span data-stu-id="43c9a-146">System.String</span></span>

## <span data-ttu-id="43c9a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43c9a-147">OUTPUTS</span></span>

### <span data-ttu-id="43c9a-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="43c9a-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="43c9a-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="43c9a-149">NOTES</span></span>

## <span data-ttu-id="43c9a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43c9a-150">RELATED LINKS</span></span>

[<span data-ttu-id="43c9a-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="43c9a-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="43c9a-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="43c9a-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="43c9a-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="43c9a-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="43c9a-154">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="43c9a-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)