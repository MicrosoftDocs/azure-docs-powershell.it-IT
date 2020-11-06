---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
ms.openlocfilehash: 250fa8a5638e1aa9d67d212fd45352c7756d2aef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507436"
---
# <span data-ttu-id="e4623-101">Set-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e4623-101">Set-AzureRmFrontDoor</span></span>

## <span data-ttu-id="e4623-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4623-102">SYNOPSIS</span></span>
<span data-ttu-id="e4623-103">Aggiornare un bilanciamento del carico della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="e4623-103">Update a Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4623-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4623-104">SYNTAX</span></span>

### <span data-ttu-id="e4623-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4623-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4623-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4623-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4623-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4623-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4623-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4623-108">DESCRIPTION</span></span>
<span data-ttu-id="e4623-109">Il cmdlet **set-AzureRmFrontDoor** aggiorna un bilanciamento del carico di porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="e4623-109">The **Set-AzureRmFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="e4623-110">Se non vengono forniti parametri di input, verranno usati i vecchi parametri della porta anteriore esistente.</span><span class="sxs-lookup"><span data-stu-id="e4623-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="e4623-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4623-111">EXAMPLES</span></span>

### <span data-ttu-id="e4623-112">Esempio 1: aggiornare uno sportello anteriore esistente con FrontDoorName e ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e4623-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e4623-113">aggiornare un FrontDoor esistente.</span><span class="sxs-lookup"><span data-stu-id="e4623-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="e4623-114">Esempio 2: aggiornare uno sportello anteriore esistente con l'oggetto PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e4623-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e4623-115">aggiornare un FrontDoor esistente.</span><span class="sxs-lookup"><span data-stu-id="e4623-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="e4623-116">Esempio 3: aggiornare una porta anteriore esistente con ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4623-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e4623-117">aggiornare un FrontDoor esistente.</span><span class="sxs-lookup"><span data-stu-id="e4623-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="e4623-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4623-118">PARAMETERS</span></span>

### <span data-ttu-id="e4623-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="e4623-119">-BackendPool</span></span>
<span data-ttu-id="e4623-120">Backendpools disponibile per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="e4623-120">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4623-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4623-121">-DefaultProfile</span></span>
<span data-ttu-id="e4623-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4623-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4623-123">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e4623-123">-EnabledState</span></span>
<span data-ttu-id="e4623-124">Stato operativo del servizio di bilanciamento del carico della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="e4623-124">Operational status of the Front Door load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4623-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4623-125">-FrontendEndpoint</span></span>
<span data-ttu-id="e4623-126">Endpoint frontend disponibili per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="e4623-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4623-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="e4623-127">-HealthProbeSetting</span></span>
<span data-ttu-id="e4623-128">Impostazioni della sonda integrità associate all'istanza di porta principale.</span><span class="sxs-lookup"><span data-stu-id="e4623-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4623-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4623-129">-InputObject</span></span>
<span data-ttu-id="e4623-130">L'oggetto porta principale da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e4623-130">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4623-131">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="e4623-131">-LoadBalancingSetting</span></span>
<span data-ttu-id="e4623-132">Impostazioni di bilanciamento del carico associate all'istanza di porta principale.</span><span class="sxs-lookup"><span data-stu-id="e4623-132">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4623-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4623-133">-Name</span></span>
<span data-ttu-id="e4623-134">Il nome della porta anteriore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e4623-134">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4623-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4623-135">-ResourceGroupName</span></span>
<span data-ttu-id="e4623-136">Gruppo di risorse a cui appartiene la porta principale.</span><span class="sxs-lookup"><span data-stu-id="e4623-136">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4623-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4623-137">-ResourceId</span></span>
<span data-ttu-id="e4623-138">ID risorsa della porta principale da aggiornare</span><span class="sxs-lookup"><span data-stu-id="e4623-138">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4623-139">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="e4623-139">-RoutingRule</span></span>
<span data-ttu-id="e4623-140">Regole di routing associate a questo FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e4623-140">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4623-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4623-141">-Tag</span></span>
<span data-ttu-id="e4623-142">I tag si associano a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e4623-142">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="e4623-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e4623-143">-Confirm</span></span>
<span data-ttu-id="e4623-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4623-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4623-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4623-145">-WhatIf</span></span>
<span data-ttu-id="e4623-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4623-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4623-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4623-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4623-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4623-148">CommonParameters</span></span>
<span data-ttu-id="e4623-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4623-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4623-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4623-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4623-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4623-151">INPUTS</span></span>

### <span data-ttu-id="e4623-152">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e4623-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="e4623-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e4623-153">System.String</span></span>

## <span data-ttu-id="e4623-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4623-154">OUTPUTS</span></span>

### <span data-ttu-id="e4623-155">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e4623-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="e4623-156">Note</span><span class="sxs-lookup"><span data-stu-id="e4623-156">NOTES</span></span>

## <span data-ttu-id="e4623-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4623-157">RELATED LINKS</span></span>

<span data-ttu-id="e4623-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="e4623-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
