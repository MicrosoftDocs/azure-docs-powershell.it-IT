---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: faa634facf6baa8d0d55490ec32a9395feaea5db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963982"
---
# <span data-ttu-id="c4fe5-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="c4fe5-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="c4fe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="c4fe5-103">Aggiorna un gateway ExpressRoute scalabile.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="c4fe5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4fe5-104">SYNTAX</span></span>

### <span data-ttu-id="c4fe5-105">ByExpressRouteGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4fe5-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4fe5-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c4fe5-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4fe5-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c4fe5-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4fe5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c4fe5-108">DESCRIPTION</span></span>

<span data-ttu-id="c4fe5-109">Il cmdlet **Set-AzExpressRouteGateway** consente di aggiornare le unità di scala per un expressRouteGateway esistente o aggiornare i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="c4fe5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4fe5-110">EXAMPLES</span></span>

### <span data-ttu-id="c4fe5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c4fe5-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="c4fe5-112">La procedura precedente consente di creare un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c4fe5-113">Successivamente verrà creato un gateway ExpressRoute nell'hub virtuale con 2 unità di scala che verranno quindi modificate in 3 unità di scala</span><span class="sxs-lookup"><span data-stu-id="c4fe5-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="c4fe5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4fe5-114">PARAMETERS</span></span>

### <span data-ttu-id="c4fe5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4fe5-115">-AsJob</span></span>
<span data-ttu-id="c4fe5-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c4fe5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4fe5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4fe5-117">-DefaultProfile</span></span>
<span data-ttu-id="c4fe5-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4fe5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4fe5-119">-InputObject</span></span>
<span data-ttu-id="c4fe5-120">ExpressRouteGateway da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-120">The ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fe5-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="c4fe5-121">-MaxScaleUnits</span></span>
<span data-ttu-id="c4fe5-122">Numero massimo di unità di scala per questo ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="c4fe5-123">Intervallo valido > 2</span><span class="sxs-lookup"><span data-stu-id="c4fe5-123">Valid range > 2</span></span>

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

### <span data-ttu-id="c4fe5-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="c4fe5-124">-MinScaleUnits</span></span>
<span data-ttu-id="c4fe5-125">Numero minimo di unità di scala per questo ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="c4fe5-126">Intervallo valido > 2</span><span class="sxs-lookup"><span data-stu-id="c4fe5-126">Valid range > 2</span></span>

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

### <span data-ttu-id="c4fe5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c4fe5-127">-Name</span></span>
<span data-ttu-id="c4fe5-128">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fe5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4fe5-129">-ResourceGroupName</span></span>
<span data-ttu-id="c4fe5-130">Nome del gruppo di risorse di ExpressRouteGateway da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fe5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4fe5-131">-ResourceId</span></span>
<span data-ttu-id="c4fe5-132">ID di ExpressRouteGateway da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fe5-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4fe5-133">-Tag</span></span>
<span data-ttu-id="c4fe5-134">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c4fe5-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4fe5-135">-Confirm</span></span>
<span data-ttu-id="c4fe5-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4fe5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4fe5-137">-WhatIf</span></span>
<span data-ttu-id="c4fe5-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4fe5-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4fe5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fe5-140">CommonParameters</span></span>
<span data-ttu-id="c4fe5-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4fe5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fe5-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4fe5-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fe5-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="c4fe5-143">INPUTS</span></span>

### <span data-ttu-id="c4fe5-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c4fe5-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="c4fe5-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c4fe5-145">System.String</span></span>

## <span data-ttu-id="c4fe5-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4fe5-146">OUTPUTS</span></span>

### <span data-ttu-id="c4fe5-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="c4fe5-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="c4fe5-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="c4fe5-148">NOTES</span></span>

## <span data-ttu-id="c4fe5-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4fe5-149">RELATED LINKS</span></span>
