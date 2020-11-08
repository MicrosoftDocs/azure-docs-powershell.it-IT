---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 3461d629eac47a1bbf2842d2cb0a913c2734f94e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189006"
---
# <span data-ttu-id="f990b-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f990b-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="f990b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f990b-102">SYNOPSIS</span></span>
<span data-ttu-id="f990b-103">Recupera una risorsa della tabella route Hub associata a un VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="f990b-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="f990b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f990b-104">SYNTAX</span></span>

### <span data-ttu-id="f990b-105">ByVHubRouteTableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f990b-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f990b-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="f990b-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f990b-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="f990b-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f990b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f990b-108">DESCRIPTION</span></span>
<span data-ttu-id="f990b-109">Ottiene la tabella route Hub specificata associata all'hub virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="f990b-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="f990b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f990b-110">EXAMPLES</span></span>

### <span data-ttu-id="f990b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f990b-111">Example 1</span></span>

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

<span data-ttu-id="f990b-112">Questo comando consente di ottenere la tabella route Hub dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="f990b-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="f990b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f990b-113">Example 2</span></span>

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

<span data-ttu-id="f990b-114">Questo comando elenca tutte le tabelle Route Hub nel VirtualHub specificato.</span><span class="sxs-lookup"><span data-stu-id="f990b-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="f990b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f990b-115">PARAMETERS</span></span>

### <span data-ttu-id="f990b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f990b-116">-AsJob</span></span>
<span data-ttu-id="f990b-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f990b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f990b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f990b-118">-DefaultProfile</span></span>
<span data-ttu-id="f990b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f990b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f990b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f990b-120">-Name</span></span>
<span data-ttu-id="f990b-121">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f990b-121">The resource name.</span></span>

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

### <span data-ttu-id="f990b-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f990b-122">-ParentObject</span></span>
<span data-ttu-id="f990b-123">L'oggetto hub virtuale padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f990b-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="f990b-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f990b-124">-ParentResourceName</span></span>
<span data-ttu-id="f990b-125">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="f990b-125">The parent resource name.</span></span>

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

### <span data-ttu-id="f990b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f990b-126">-ResourceGroupName</span></span>
<span data-ttu-id="f990b-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f990b-127">The resource group name.</span></span>

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

### <span data-ttu-id="f990b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f990b-128">-ResourceId</span></span>
<span data-ttu-id="f990b-129">ID risorsa della risorsa vhubroutetable da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f990b-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="f990b-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f990b-130">-Confirm</span></span>
<span data-ttu-id="f990b-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f990b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f990b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f990b-132">-WhatIf</span></span>
<span data-ttu-id="f990b-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f990b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f990b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f990b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f990b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f990b-135">CommonParameters</span></span>
<span data-ttu-id="f990b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f990b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f990b-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f990b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f990b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f990b-138">INPUTS</span></span>

### <span data-ttu-id="f990b-139">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f990b-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="f990b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f990b-140">System.String</span></span>

## <span data-ttu-id="f990b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f990b-141">OUTPUTS</span></span>

### <span data-ttu-id="f990b-142">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f990b-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="f990b-143">Note</span><span class="sxs-lookup"><span data-stu-id="f990b-143">NOTES</span></span>

## <span data-ttu-id="f990b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f990b-144">RELATED LINKS</span></span>

[<span data-ttu-id="f990b-145">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="f990b-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="f990b-146">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f990b-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="f990b-147">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f990b-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="f990b-148">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f990b-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)