---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: a07df2c6330757bf9e5b4f211429f6e2918fea39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310723"
---
# <span data-ttu-id="e08cc-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e08cc-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="e08cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e08cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e08cc-103">Aggiorna un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="e08cc-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="e08cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e08cc-104">SYNTAX</span></span>

### <span data-ttu-id="e08cc-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e08cc-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e08cc-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e08cc-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e08cc-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e08cc-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e08cc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e08cc-108">DESCRIPTION</span></span>
<span data-ttu-id="e08cc-109">Il cmdlet **Update-AzVirtualHub** aggiorna un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="e08cc-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="e08cc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e08cc-110">EXAMPLES</span></span>

### <span data-ttu-id="e08cc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e08cc-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="e08cc-112">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="e08cc-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e08cc-113">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="e08cc-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="e08cc-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e08cc-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="e08cc-115">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="e08cc-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e08cc-116">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="e08cc-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="e08cc-117">Questo esempio è simile all'esempio 1, ma allega anche una tabella di route all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="e08cc-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="e08cc-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e08cc-118">PARAMETERS</span></span>

### <span data-ttu-id="e08cc-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e08cc-119">-AddressPrefix</span></span>
<span data-ttu-id="e08cc-120">Stringa dello spazio indirizzo per questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="e08cc-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="e08cc-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e08cc-121">-AsJob</span></span>
<span data-ttu-id="e08cc-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e08cc-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e08cc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e08cc-123">-DefaultProfile</span></span>
<span data-ttu-id="e08cc-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e08cc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e08cc-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e08cc-125">-HubVnetConnection</span></span>
<span data-ttu-id="e08cc-126">Connessioni di rete virtuali Hub associate a questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="e08cc-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08cc-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e08cc-127">-InputObject</span></span>
<span data-ttu-id="e08cc-128">L'oggetto hub virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="e08cc-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e08cc-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="e08cc-129">-Name</span></span>
<span data-ttu-id="e08cc-130">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e08cc-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08cc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e08cc-131">-ResourceGroupName</span></span>
<span data-ttu-id="e08cc-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e08cc-132">The resource group name.</span></span>

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

### <span data-ttu-id="e08cc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e08cc-133">-ResourceId</span></span>
<span data-ttu-id="e08cc-134">ID risorsa dell'hub virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="e08cc-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e08cc-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e08cc-135">-RouteTable</span></span>
<span data-ttu-id="e08cc-136">Tabella route associata a questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="e08cc-136">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08cc-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="e08cc-137">-Sku</span></span>
<span data-ttu-id="e08cc-138">SKU dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="e08cc-138">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="e08cc-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e08cc-139">-Tag</span></span>
<span data-ttu-id="e08cc-140">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e08cc-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08cc-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e08cc-141">-Confirm</span></span>
<span data-ttu-id="e08cc-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e08cc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e08cc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e08cc-143">-WhatIf</span></span>
<span data-ttu-id="e08cc-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e08cc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e08cc-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e08cc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e08cc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e08cc-146">CommonParameters</span></span>
<span data-ttu-id="e08cc-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e08cc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e08cc-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e08cc-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e08cc-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e08cc-149">INPUTS</span></span>

### <span data-ttu-id="e08cc-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e08cc-150">System.String</span></span>

### <span data-ttu-id="e08cc-151">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e08cc-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e08cc-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e08cc-152">OUTPUTS</span></span>

### <span data-ttu-id="e08cc-153">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e08cc-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e08cc-154">Note</span><span class="sxs-lookup"><span data-stu-id="e08cc-154">NOTES</span></span>

## <span data-ttu-id="e08cc-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e08cc-155">RELATED LINKS</span></span>

[<span data-ttu-id="e08cc-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e08cc-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="e08cc-157">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e08cc-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="e08cc-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e08cc-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)
