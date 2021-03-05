---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: df81d3df31ad1d04914164d04321151e0df2dfdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974766"
---
# <span data-ttu-id="f8a51-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="f8a51-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="f8a51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8a51-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a51-103">Crea un gateway ExpressRoute scalabile.</span><span class="sxs-lookup"><span data-stu-id="f8a51-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="f8a51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8a51-104">SYNTAX</span></span>

### <span data-ttu-id="f8a51-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8a51-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a51-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="f8a51-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a51-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="f8a51-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8a51-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f8a51-108">DESCRIPTION</span></span>

<span data-ttu-id="f8a51-109">New-AzExpressRouteGateway crea un Gateway ExpressRoute scalabile.</span><span class="sxs-lookup"><span data-stu-id="f8a51-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="f8a51-110">Connettività definita dal software per Azure locale all'interno di VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="f8a51-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="f8a51-111">Il gateway può essere ridimensionato in base all'unità di scala specificata in questo o nel cmdlet Set-AzExpressRouteGateway locale.</span><span class="sxs-lookup"><span data-stu-id="f8a51-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="f8a51-112">Viene impostata una connessione da un circuito ExpressRoute locale al gateway scalabile.</span><span class="sxs-lookup"><span data-stu-id="f8a51-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="f8a51-113">ExpressRouteGateway si posizionerà nella stessa posizione del virtualhub a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="f8a51-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="f8a51-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8a51-114">EXAMPLES</span></span>

### <span data-ttu-id="f8a51-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8a51-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="f8a51-116">In questo modo verrà creato un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a51-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="f8a51-117">Successivamente verrà creato un gateway ExpressRoute nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="f8a51-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="f8a51-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8a51-118">PARAMETERS</span></span>

### <span data-ttu-id="f8a51-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8a51-119">-AsJob</span></span>
<span data-ttu-id="f8a51-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f8a51-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8a51-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a51-121">-DefaultProfile</span></span>
<span data-ttu-id="f8a51-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a51-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8a51-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="f8a51-123">-MaxScaleUnits</span></span>
<span data-ttu-id="f8a51-124">Numero massimo di unità di scala per questo ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="f8a51-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="f8a51-125">Intervallo valido > 2</span><span class="sxs-lookup"><span data-stu-id="f8a51-125">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a51-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="f8a51-126">-MinScaleUnits</span></span>
<span data-ttu-id="f8a51-127">Numero minimo di unità di scala per questo ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="f8a51-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="f8a51-128">Intervallo valido > 2</span><span class="sxs-lookup"><span data-stu-id="f8a51-128">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a51-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f8a51-129">-Name</span></span>
<span data-ttu-id="f8a51-130">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f8a51-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a51-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a51-131">-ResourceGroupName</span></span>
<span data-ttu-id="f8a51-132">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f8a51-132">The resource name.</span></span>

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

### <span data-ttu-id="f8a51-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8a51-133">-Tag</span></span>
<span data-ttu-id="f8a51-134">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="f8a51-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f8a51-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="f8a51-135">-VirtualHub</span></span>
<span data-ttu-id="f8a51-136">VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f8a51-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8a51-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="f8a51-137">-VirtualHubId</span></span>
<span data-ttu-id="f8a51-138">ID di VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f8a51-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8a51-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="f8a51-139">-VirtualHubName</span></span>
<span data-ttu-id="f8a51-140">ID di VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f8a51-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a51-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8a51-141">-Confirm</span></span>
<span data-ttu-id="f8a51-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8a51-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8a51-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8a51-143">-WhatIf</span></span>
<span data-ttu-id="f8a51-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8a51-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8a51-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8a51-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8a51-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a51-146">CommonParameters</span></span>
<span data-ttu-id="f8a51-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8a51-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a51-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8a51-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a51-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="f8a51-149">INPUTS</span></span>

### <span data-ttu-id="f8a51-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f8a51-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="f8a51-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f8a51-151">System.String</span></span>

## <span data-ttu-id="f8a51-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8a51-152">OUTPUTS</span></span>

### <span data-ttu-id="f8a51-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="f8a51-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="f8a51-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="f8a51-154">NOTES</span></span>

## <span data-ttu-id="f8a51-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8a51-155">RELATED LINKS</span></span>
