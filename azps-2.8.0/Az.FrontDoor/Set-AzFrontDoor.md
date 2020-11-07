---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 57f1bf57495e75167a1936799c24aff5e6387722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674359"
---
# <span data-ttu-id="d128b-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d128b-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="d128b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d128b-102">SYNOPSIS</span></span>
<span data-ttu-id="d128b-103">Aggiornare un bilanciamento del carico della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="d128b-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="d128b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d128b-104">SYNTAX</span></span>

### <span data-ttu-id="d128b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d128b-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d128b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d128b-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d128b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d128b-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d128b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d128b-108">DESCRIPTION</span></span>
<span data-ttu-id="d128b-109">Il cmdlet **set-AzFrontDoor** aggiorna un bilanciamento del carico di porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="d128b-109">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="d128b-110">Se non vengono forniti parametri di input, verranno usati i vecchi parametri della porta anteriore esistente.</span><span class="sxs-lookup"><span data-stu-id="d128b-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="d128b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d128b-111">EXAMPLES</span></span>

### <span data-ttu-id="d128b-112">Esempio 1: aggiornare uno sportello anteriore esistente con FrontDoorName e ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="d128b-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="d128b-113">aggiornare un FrontDoor esistente.</span><span class="sxs-lookup"><span data-stu-id="d128b-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="d128b-114">Esempio 2: aggiornare uno sportello anteriore esistente con l'oggetto PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="d128b-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="d128b-115">aggiornare un FrontDoor esistente.</span><span class="sxs-lookup"><span data-stu-id="d128b-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="d128b-116">Esempio 3: aggiornare una porta anteriore esistente con ResourceId</span><span class="sxs-lookup"><span data-stu-id="d128b-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="d128b-117">aggiornare un FrontDoor esistente.</span><span class="sxs-lookup"><span data-stu-id="d128b-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="d128b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d128b-118">PARAMETERS</span></span>

### <span data-ttu-id="d128b-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="d128b-119">-BackendPool</span></span>
<span data-ttu-id="d128b-120">Backendpools disponibile per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="d128b-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="d128b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d128b-121">-DefaultProfile</span></span>
<span data-ttu-id="d128b-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d128b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d128b-123">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="d128b-123">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="d128b-124">Se disabilitare il controllo nome certificato per le richieste HTTPS a tutti i pool back-end.</span><span class="sxs-lookup"><span data-stu-id="d128b-124">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="d128b-125">Nessun effetto sulle richieste non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d128b-125">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="d128b-126">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d128b-126">-EnabledState</span></span>
<span data-ttu-id="d128b-127">Stato operativo del servizio di bilanciamento del carico della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="d128b-127">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="d128b-128">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="d128b-128">-FrontendEndpoint</span></span>
<span data-ttu-id="d128b-129">Endpoint frontend disponibili per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="d128b-129">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="d128b-130">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="d128b-130">-HealthProbeSetting</span></span>
<span data-ttu-id="d128b-131">Impostazioni della sonda integrità associate all'istanza di porta principale.</span><span class="sxs-lookup"><span data-stu-id="d128b-131">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="d128b-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d128b-132">-InputObject</span></span>
<span data-ttu-id="d128b-133">L'oggetto porta principale da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="d128b-133">The Front Door object to update.</span></span>

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

### <span data-ttu-id="d128b-134">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="d128b-134">-LoadBalancingSetting</span></span>
<span data-ttu-id="d128b-135">Impostazioni di bilanciamento del carico associate all'istanza di porta principale.</span><span class="sxs-lookup"><span data-stu-id="d128b-135">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="d128b-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="d128b-136">-Name</span></span>
<span data-ttu-id="d128b-137">Il nome della porta anteriore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="d128b-137">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="d128b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d128b-138">-ResourceGroupName</span></span>
<span data-ttu-id="d128b-139">Gruppo di risorse a cui appartiene la porta principale.</span><span class="sxs-lookup"><span data-stu-id="d128b-139">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="d128b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d128b-140">-ResourceId</span></span>
<span data-ttu-id="d128b-141">ID risorsa della porta principale da aggiornare</span><span class="sxs-lookup"><span data-stu-id="d128b-141">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d128b-142">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="d128b-142">-RoutingRule</span></span>
<span data-ttu-id="d128b-143">Regole di routing associate a questo FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d128b-143">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="d128b-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="d128b-144">-Tag</span></span>
<span data-ttu-id="d128b-145">I tag si associano a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="d128b-145">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="d128b-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d128b-146">-Confirm</span></span>
<span data-ttu-id="d128b-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d128b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d128b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d128b-148">-WhatIf</span></span>
<span data-ttu-id="d128b-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d128b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d128b-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d128b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d128b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d128b-151">CommonParameters</span></span>
<span data-ttu-id="d128b-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d128b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d128b-153">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d128b-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d128b-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d128b-154">INPUTS</span></span>

### <span data-ttu-id="d128b-155">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d128b-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="d128b-156">System. String</span><span class="sxs-lookup"><span data-stu-id="d128b-156">System.String</span></span>

## <span data-ttu-id="d128b-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d128b-157">OUTPUTS</span></span>

### <span data-ttu-id="d128b-158">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d128b-158">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="d128b-159">Note</span><span class="sxs-lookup"><span data-stu-id="d128b-159">NOTES</span></span>

## <span data-ttu-id="d128b-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d128b-160">RELATED LINKS</span></span>

<span data-ttu-id="d128b-161">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="d128b-161">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
