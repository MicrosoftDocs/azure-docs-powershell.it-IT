---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
ms.openlocfilehash: 4058f9a2ba0de1e5610773ad4af21c8bb788d58c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686615"
---
# <span data-ttu-id="09259-101">New-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="09259-101">New-AzureRmVirtualHub</span></span>

## <span data-ttu-id="09259-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09259-102">SYNOPSIS</span></span>
<span data-ttu-id="09259-103">Crea una risorsa di Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="09259-103">Creates an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09259-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09259-104">SYNTAX</span></span>

### <span data-ttu-id="09259-105">ByVirtualWanObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09259-105">ByVirtualWanObject (Default)</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 -AddressPrefix <String> -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09259-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="09259-106">ByVirtualWanResourceId</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09259-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09259-107">DESCRIPTION</span></span>
<span data-ttu-id="09259-108">Crea una risorsa di Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="09259-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="09259-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09259-109">EXAMPLES</span></span>

### <span data-ttu-id="09259-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09259-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

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

<span data-ttu-id="09259-111">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="09259-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="09259-112">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="09259-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="09259-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="09259-113">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

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

<span data-ttu-id="09259-114">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="09259-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="09259-115">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="09259-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="09259-116">Questo esempio è simile all'esempio 1, ma usa un ID risorsa per fare riferimento alla rete WAN virtuale necessaria per creare l'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="09259-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="09259-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="09259-117">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

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

<span data-ttu-id="09259-118">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="09259-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="09259-119">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24" e una tabella di route allegata.</span><span class="sxs-lookup"><span data-stu-id="09259-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="09259-120">Questo esempio è simile all'esempio 2, ma allega anche una tabella di route all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="09259-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="09259-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09259-121">PARAMETERS</span></span>

### <span data-ttu-id="09259-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="09259-122">-AddressPrefix</span></span>
<span data-ttu-id="09259-123">Stringa dello spazio indirizzo per questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="09259-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="09259-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09259-124">-AsJob</span></span>
<span data-ttu-id="09259-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="09259-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09259-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09259-126">-DefaultProfile</span></span>
<span data-ttu-id="09259-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09259-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09259-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="09259-128">-HubVnetConnection</span></span>
<span data-ttu-id="09259-129">Connessioni di rete virtuali Hub associate a questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="09259-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="09259-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="09259-130">-Location</span></span>
<span data-ttu-id="09259-131">posizione.</span><span class="sxs-lookup"><span data-stu-id="09259-131">location.</span></span>

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

### <span data-ttu-id="09259-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="09259-132">-Name</span></span>
<span data-ttu-id="09259-133">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="09259-133">The resource name.</span></span>

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

### <span data-ttu-id="09259-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09259-134">-ResourceGroupName</span></span>
<span data-ttu-id="09259-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09259-135">The resource group name.</span></span>

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

### <span data-ttu-id="09259-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="09259-136">-RouteTable</span></span>
<span data-ttu-id="09259-137">Tabella route associata a questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="09259-137">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="09259-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="09259-138">-Tag</span></span>
<span data-ttu-id="09259-139">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="09259-139">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="09259-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="09259-140">-VirtualWan</span></span>
<span data-ttu-id="09259-141">L'oggetto WAN virtuale a cui è collegato l'hub.</span><span class="sxs-lookup"><span data-stu-id="09259-141">The virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="09259-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="09259-142">-VirtualWanId</span></span>
<span data-ttu-id="09259-143">ID dell'oggetto WAN virtuale a cui è collegato questo hub.</span><span class="sxs-lookup"><span data-stu-id="09259-143">The id of virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="09259-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09259-144">-Confirm</span></span>
<span data-ttu-id="09259-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09259-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09259-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09259-146">-WhatIf</span></span>
<span data-ttu-id="09259-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09259-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09259-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09259-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09259-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09259-149">CommonParameters</span></span>
<span data-ttu-id="09259-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09259-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09259-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09259-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09259-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09259-152">INPUTS</span></span>

### <span data-ttu-id="09259-153">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="09259-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="09259-154">System. String</span><span class="sxs-lookup"><span data-stu-id="09259-154">System.String</span></span>

## <span data-ttu-id="09259-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09259-155">OUTPUTS</span></span>

### <span data-ttu-id="09259-156">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="09259-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="09259-157">Note</span><span class="sxs-lookup"><span data-stu-id="09259-157">NOTES</span></span>

## <span data-ttu-id="09259-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09259-158">RELATED LINKS</span></span>
