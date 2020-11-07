---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: 8527b383dd5469d1a9bc34b7916a1e28b3f673f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852877"
---
# <span data-ttu-id="36c71-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36c71-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="36c71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36c71-102">SYNOPSIS</span></span>
<span data-ttu-id="36c71-103">Crea una risorsa di Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="36c71-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="36c71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36c71-104">SYNTAX</span></span>

### <span data-ttu-id="36c71-105">ByVirtualWanObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36c71-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36c71-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="36c71-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36c71-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36c71-107">DESCRIPTION</span></span>
<span data-ttu-id="36c71-108">Crea una risorsa di Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="36c71-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="36c71-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36c71-109">EXAMPLES</span></span>

### <span data-ttu-id="36c71-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="36c71-110">Example 1</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="36c71-111">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="36c71-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="36c71-112">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="36c71-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="36c71-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="36c71-113">Example 2</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="36c71-114">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="36c71-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="36c71-115">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="36c71-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="36c71-116">Questo esempio è simile all'esempio 1, ma usa un ID risorsa per fare riferimento alla rete WAN virtuale necessaria per creare l'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="36c71-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="36c71-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="36c71-117">Example 3</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="36c71-118">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="36c71-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="36c71-119">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24" e una tabella di route allegata.</span><span class="sxs-lookup"><span data-stu-id="36c71-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="36c71-120">Questo esempio è simile all'esempio 2, ma allega anche una tabella di route all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="36c71-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="36c71-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36c71-121">PARAMETERS</span></span>

### <span data-ttu-id="36c71-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="36c71-122">-AddressPrefix</span></span>
<span data-ttu-id="36c71-123">Stringa dello spazio indirizzo per questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="36c71-123">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c71-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36c71-124">-AsJob</span></span>
<span data-ttu-id="36c71-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="36c71-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c71-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c71-126">-DefaultProfile</span></span>
<span data-ttu-id="36c71-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36c71-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36c71-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="36c71-128">-HubVnetConnection</span></span>
<span data-ttu-id="36c71-129">Connessioni di rete virtuali Hub associate a questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="36c71-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c71-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="36c71-130">-Location</span></span>
<span data-ttu-id="36c71-131">posizione.</span><span class="sxs-lookup"><span data-stu-id="36c71-131">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c71-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="36c71-132">-Name</span></span>
<span data-ttu-id="36c71-133">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="36c71-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c71-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36c71-134">-ResourceGroupName</span></span>
<span data-ttu-id="36c71-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36c71-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c71-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="36c71-136">-RouteTable</span></span>
<span data-ttu-id="36c71-137">Tabella route associata a questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="36c71-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c71-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="36c71-138">-Tag</span></span>
<span data-ttu-id="36c71-139">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="36c71-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c71-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="36c71-140">-VirtualWan</span></span>
<span data-ttu-id="36c71-141">L'oggetto WAN virtuale a cui è collegato l'hub.</span><span class="sxs-lookup"><span data-stu-id="36c71-141">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36c71-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="36c71-142">-VirtualWanId</span></span>
<span data-ttu-id="36c71-143">ID dell'oggetto WAN virtuale a cui è collegato questo hub.</span><span class="sxs-lookup"><span data-stu-id="36c71-143">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c71-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36c71-144">-Confirm</span></span>
<span data-ttu-id="36c71-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36c71-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36c71-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36c71-146">-WhatIf</span></span>
<span data-ttu-id="36c71-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36c71-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36c71-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36c71-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36c71-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c71-149">CommonParameters</span></span>
<span data-ttu-id="36c71-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36c71-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c71-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36c71-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c71-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36c71-152">INPUTS</span></span>

### <span data-ttu-id="36c71-153">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="36c71-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="36c71-154">System. String</span><span class="sxs-lookup"><span data-stu-id="36c71-154">System.String</span></span>

## <span data-ttu-id="36c71-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36c71-155">OUTPUTS</span></span>

### <span data-ttu-id="36c71-156">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36c71-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="36c71-157">Note</span><span class="sxs-lookup"><span data-stu-id="36c71-157">NOTES</span></span>

## <span data-ttu-id="36c71-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36c71-158">RELATED LINKS</span></span>

[<span data-ttu-id="36c71-159">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36c71-159">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="36c71-160">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36c71-160">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="36c71-161">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36c71-161">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
