---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: d005ef841828dc1fe37915c4a7b0d28ad93e3b44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475076"
---
# <span data-ttu-id="0d046-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0d046-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="0d046-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d046-102">SYNOPSIS</span></span>
<span data-ttu-id="0d046-103">Crea una risorsa di Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="0d046-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="0d046-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d046-104">SYNTAX</span></span>

### <span data-ttu-id="0d046-105">ByVirtualWanObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0d046-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d046-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="0d046-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d046-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d046-107">DESCRIPTION</span></span>
<span data-ttu-id="0d046-108">Crea una risorsa di Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="0d046-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="0d046-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d046-109">EXAMPLES</span></span>

### <span data-ttu-id="0d046-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d046-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="0d046-111">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="0d046-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="0d046-112">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="0d046-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="0d046-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0d046-113">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="0d046-114">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="0d046-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="0d046-115">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="0d046-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="0d046-116">Questo esempio è simile all'esempio 1, ma usa un ID risorsa per fare riferimento alla rete WAN virtuale necessaria per creare l'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d046-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="0d046-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0d046-117">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="0d046-118">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="0d046-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="0d046-119">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24" e una tabella di route allegata.</span><span class="sxs-lookup"><span data-stu-id="0d046-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="0d046-120">Questo esempio è simile all'esempio 2, ma allega anche una tabella di route all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d046-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="0d046-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d046-121">PARAMETERS</span></span>

### <span data-ttu-id="0d046-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0d046-122">-AddressPrefix</span></span>
<span data-ttu-id="0d046-123">Stringa dello spazio indirizzo per questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d046-123">The address space string for this virtual hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d046-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d046-124">-AsJob</span></span>
<span data-ttu-id="0d046-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0d046-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d046-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d046-126">-DefaultProfile</span></span>
<span data-ttu-id="0d046-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d046-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d046-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0d046-128">-HubVnetConnection</span></span>
<span data-ttu-id="0d046-129">Connessioni di rete virtuali Hub associate a questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d046-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="0d046-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0d046-130">-Location</span></span>
<span data-ttu-id="0d046-131">posizione.</span><span class="sxs-lookup"><span data-stu-id="0d046-131">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d046-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d046-132">-Name</span></span>
<span data-ttu-id="0d046-133">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0d046-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d046-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d046-134">-ResourceGroupName</span></span>
<span data-ttu-id="0d046-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d046-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d046-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="0d046-136">-RouteTable</span></span>
<span data-ttu-id="0d046-137">Tabella route associata a questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d046-137">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="0d046-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="0d046-138">-Sku</span></span>
<span data-ttu-id="0d046-139">SKU dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d046-139">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="0d046-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="0d046-140">-Tag</span></span>
<span data-ttu-id="0d046-141">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="0d046-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0d046-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="0d046-142">-VirtualWan</span></span>
<span data-ttu-id="0d046-143">L'oggetto WAN virtuale a cui è collegato l'hub.</span><span class="sxs-lookup"><span data-stu-id="0d046-143">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d046-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="0d046-144">-VirtualWanId</span></span>
<span data-ttu-id="0d046-145">ID dell'oggetto WAN virtuale a cui è collegato questo hub.</span><span class="sxs-lookup"><span data-stu-id="0d046-145">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d046-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d046-146">-Confirm</span></span>
<span data-ttu-id="0d046-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d046-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d046-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d046-148">-WhatIf</span></span>
<span data-ttu-id="0d046-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d046-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d046-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d046-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d046-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d046-151">CommonParameters</span></span>
<span data-ttu-id="0d046-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d046-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d046-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d046-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d046-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d046-154">INPUTS</span></span>

### <span data-ttu-id="0d046-155">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0d046-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="0d046-156">System. String</span><span class="sxs-lookup"><span data-stu-id="0d046-156">System.String</span></span>

## <span data-ttu-id="0d046-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d046-157">OUTPUTS</span></span>

### <span data-ttu-id="0d046-158">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0d046-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="0d046-159">Note</span><span class="sxs-lookup"><span data-stu-id="0d046-159">NOTES</span></span>

## <span data-ttu-id="0d046-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d046-160">RELATED LINKS</span></span>

[<span data-ttu-id="0d046-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0d046-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="0d046-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0d046-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="0d046-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0d046-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
