---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488864"
---
# <span data-ttu-id="f19a2-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f19a2-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="f19a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f19a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f19a2-103">Modifica un hub virtuale per aggiungere una tabella di route HUb virtuale.</span><span class="sxs-lookup"><span data-stu-id="f19a2-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="f19a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f19a2-104">SYNTAX</span></span>

### <span data-ttu-id="f19a2-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f19a2-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f19a2-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="f19a2-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19a2-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="f19a2-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f19a2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f19a2-108">DESCRIPTION</span></span>
<span data-ttu-id="f19a2-109">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="f19a2-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="f19a2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f19a2-110">EXAMPLES</span></span>

### <span data-ttu-id="f19a2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f19a2-111">Example 1</span></span>
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

<span data-ttu-id="f19a2-112">Prima di tutto creiamo un oggetto Route hub virtuale e lo usiamo per creare una risorsa tabella route hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="f19a2-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="f19a2-113">Impostiamo quindi la risorsa della tabella di route nell'hub virtuale usando il comando Set-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="f19a2-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="f19a2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f19a2-114">PARAMETERS</span></span>

### <span data-ttu-id="f19a2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f19a2-115">-AsJob</span></span>
<span data-ttu-id="f19a2-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f19a2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f19a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19a2-117">-DefaultProfile</span></span>
<span data-ttu-id="f19a2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f19a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f19a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f19a2-119">-InputObject</span></span>
<span data-ttu-id="f19a2-120">L'oggetto hub virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="f19a2-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="f19a2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f19a2-121">-Name</span></span>
<span data-ttu-id="f19a2-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f19a2-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f19a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="f19a2-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f19a2-124">The resource group name.</span></span>

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

### <span data-ttu-id="f19a2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f19a2-125">-ResourceId</span></span>
<span data-ttu-id="f19a2-126">ID risorsa dell'hub virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="f19a2-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="f19a2-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="f19a2-127">-RouteTable</span></span>
<span data-ttu-id="f19a2-128">Tabelle route associate a questo hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="f19a2-128">The route tables associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19a2-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="f19a2-129">-Tag</span></span>
<span data-ttu-id="f19a2-130">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f19a2-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f19a2-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f19a2-131">-Confirm</span></span>
<span data-ttu-id="f19a2-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f19a2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f19a2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f19a2-133">-WhatIf</span></span>
<span data-ttu-id="f19a2-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f19a2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f19a2-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f19a2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f19a2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19a2-136">CommonParameters</span></span>
<span data-ttu-id="f19a2-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f19a2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19a2-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f19a2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19a2-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f19a2-139">INPUTS</span></span>

### <span data-ttu-id="f19a2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f19a2-140">System.String</span></span>

### <span data-ttu-id="f19a2-141">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f19a2-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="f19a2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f19a2-142">OUTPUTS</span></span>

### <span data-ttu-id="f19a2-143">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f19a2-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="f19a2-144">Note</span><span class="sxs-lookup"><span data-stu-id="f19a2-144">NOTES</span></span>

## <span data-ttu-id="f19a2-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f19a2-145">RELATED LINKS</span></span>
