---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 3461d629eac47a1bbf2842d2cb0a913c2734f94e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203059"
---
# <span data-ttu-id="cb3a7-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb3a7-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="cb3a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb3a7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb3a7-103">Recupera una risorsa della tabella delle route dell'hub associata a un virtualhub.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="cb3a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb3a7-104">SYNTAX</span></span>

### <span data-ttu-id="cb3a7-105">ByVHubRouteTableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb3a7-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb3a7-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="cb3a7-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb3a7-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="cb3a7-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb3a7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cb3a7-108">DESCRIPTION</span></span>
<span data-ttu-id="cb3a7-109">Ottiene la tabella delle route dell'hub specificata associata all'hub virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="cb3a7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb3a7-110">EXAMPLES</span></span>

### <span data-ttu-id="cb3a7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cb3a7-111">Example 1</span></span>

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

<span data-ttu-id="cb3a7-112">Questo comando recupera la tabella delle route dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="cb3a7-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cb3a7-113">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName


Name                   : defaultRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []


Name                   : noneRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="cb3a7-114">Questo comando elenca tutte le tabelle delle route dell'hub in VirtualHub specificato.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="cb3a7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb3a7-115">PARAMETERS</span></span>

### <span data-ttu-id="cb3a7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb3a7-116">-AsJob</span></span>
<span data-ttu-id="cb3a7-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cb3a7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb3a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb3a7-118">-DefaultProfile</span></span>
<span data-ttu-id="cb3a7-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb3a7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cb3a7-120">-Name</span></span>
<span data-ttu-id="cb3a7-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-121">The resource name.</span></span>

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

### <span data-ttu-id="cb3a7-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cb3a7-122">-ParentObject</span></span>
<span data-ttu-id="cb3a7-123">Oggetto hub virtuale padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="cb3a7-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="cb3a7-124">-ParentResourceName</span></span>
<span data-ttu-id="cb3a7-125">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-125">The parent resource name.</span></span>

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

### <span data-ttu-id="cb3a7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb3a7-126">-ResourceGroupName</span></span>
<span data-ttu-id="cb3a7-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-127">The resource group name.</span></span>

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

### <span data-ttu-id="cb3a7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb3a7-128">-ResourceId</span></span>
<span data-ttu-id="cb3a7-129">ID risorsa della risorsa vhubroutetable per Ottenere.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="cb3a7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb3a7-130">-Confirm</span></span>
<span data-ttu-id="cb3a7-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb3a7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb3a7-132">-WhatIf</span></span>
<span data-ttu-id="cb3a7-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb3a7-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb3a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb3a7-135">CommonParameters</span></span>
<span data-ttu-id="cb3a7-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb3a7-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb3a7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb3a7-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="cb3a7-138">INPUTS</span></span>

### <span data-ttu-id="cb3a7-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cb3a7-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="cb3a7-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cb3a7-140">System.String</span></span>

## <span data-ttu-id="cb3a7-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb3a7-141">OUTPUTS</span></span>

### <span data-ttu-id="cb3a7-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb3a7-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="cb3a7-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="cb3a7-143">NOTES</span></span>

## <span data-ttu-id="cb3a7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb3a7-144">RELATED LINKS</span></span>

[<span data-ttu-id="cb3a7-145">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="cb3a7-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="cb3a7-146">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb3a7-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="cb3a7-147">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb3a7-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="cb3a7-148">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb3a7-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)