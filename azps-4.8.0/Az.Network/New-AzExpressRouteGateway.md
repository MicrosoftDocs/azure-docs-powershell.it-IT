---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032943"
---
# <span data-ttu-id="21716-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="21716-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="21716-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21716-102">SYNOPSIS</span></span>
<span data-ttu-id="21716-103">Crea un gateway ExpressRoute scalabile.</span><span class="sxs-lookup"><span data-stu-id="21716-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="21716-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21716-104">SYNTAX</span></span>

### <span data-ttu-id="21716-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="21716-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21716-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="21716-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21716-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="21716-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21716-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21716-108">DESCRIPTION</span></span>

<span data-ttu-id="21716-109">New-AzExpressRouteGateway crea un gateway ExpressRoute scalabile.</span><span class="sxs-lookup"><span data-stu-id="21716-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="21716-110">Questa è la connettività definita dal software per la premessa ad Azure all'interno del VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="21716-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="21716-111">Questo gateway può essere ridimensionato in base all'unità di scala specificata in questo o nel cmdlet Set-AzExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="21716-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="21716-112">Una connessione viene configurata da un circuito di ExpressRoute locale al gateway scalabile.</span><span class="sxs-lookup"><span data-stu-id="21716-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="21716-113">Il ExpressRouteGateway sarà nella stessa posizione della VirtualHub a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="21716-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="21716-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21716-114">EXAMPLES</span></span>

### <span data-ttu-id="21716-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="21716-115">Example 1</span></span>

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

<span data-ttu-id="21716-116">Quanto sopra creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="21716-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="21716-117">Un gateway ExpressRoute verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="21716-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="21716-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21716-118">PARAMETERS</span></span>

### <span data-ttu-id="21716-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21716-119">-AsJob</span></span>
<span data-ttu-id="21716-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="21716-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21716-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21716-121">-DefaultProfile</span></span>
<span data-ttu-id="21716-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21716-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21716-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="21716-123">-MaxScaleUnits</span></span>
<span data-ttu-id="21716-124">Numero massimo di unità di scala per questo ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="21716-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="21716-125">Intervallo valido > 2</span><span class="sxs-lookup"><span data-stu-id="21716-125">Valid range > 2</span></span>

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

### <span data-ttu-id="21716-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="21716-126">-MinScaleUnits</span></span>
<span data-ttu-id="21716-127">Il numero minimo di unità di scala per questo ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="21716-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="21716-128">Intervallo valido > 2</span><span class="sxs-lookup"><span data-stu-id="21716-128">Valid range > 2</span></span>

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

### <span data-ttu-id="21716-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="21716-129">-Name</span></span>
<span data-ttu-id="21716-130">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="21716-130">The resource name.</span></span>

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

### <span data-ttu-id="21716-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21716-131">-ResourceGroupName</span></span>
<span data-ttu-id="21716-132">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="21716-132">The resource name.</span></span>

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

### <span data-ttu-id="21716-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="21716-133">-Tag</span></span>
<span data-ttu-id="21716-134">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="21716-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="21716-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="21716-135">-VirtualHub</span></span>
<span data-ttu-id="21716-136">VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="21716-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="21716-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="21716-137">-VirtualHubId</span></span>
<span data-ttu-id="21716-138">ID dell'VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="21716-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="21716-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="21716-139">-VirtualHubName</span></span>
<span data-ttu-id="21716-140">ID dell'VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="21716-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="21716-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="21716-141">-Confirm</span></span>
<span data-ttu-id="21716-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21716-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21716-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21716-143">-WhatIf</span></span>
<span data-ttu-id="21716-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21716-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21716-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21716-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21716-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21716-146">CommonParameters</span></span>
<span data-ttu-id="21716-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21716-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21716-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21716-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21716-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21716-149">INPUTS</span></span>

### <span data-ttu-id="21716-150">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="21716-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="21716-151">System. String</span><span class="sxs-lookup"><span data-stu-id="21716-151">System.String</span></span>

## <span data-ttu-id="21716-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21716-152">OUTPUTS</span></span>

### <span data-ttu-id="21716-153">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="21716-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="21716-154">Note</span><span class="sxs-lookup"><span data-stu-id="21716-154">NOTES</span></span>

## <span data-ttu-id="21716-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21716-155">RELATED LINKS</span></span>
