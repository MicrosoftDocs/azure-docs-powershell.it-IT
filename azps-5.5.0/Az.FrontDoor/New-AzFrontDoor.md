---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188430"
---
# <span data-ttu-id="e3445-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3445-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="e3445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3445-102">SYNOPSIS</span></span>
<span data-ttu-id="e3445-103">Creare una nuova bilanciamento del carico di Azure Front Door</span><span class="sxs-lookup"><span data-stu-id="e3445-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="e3445-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3445-104">SYNTAX</span></span>

### <span data-ttu-id="e3445-105">ByFieldsWithBackendPoolsSettingParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3445-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3445-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3445-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3445-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3445-107">DESCRIPTION</span></span>
<span data-ttu-id="e3445-108">Il cmdlet **New-AzFrontDoor** crea una nuova bilanciamento del carico azure front-door nel gruppo di risorse specificato nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="e3445-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="e3445-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3445-109">EXAMPLES</span></span>

### <span data-ttu-id="e3445-110">Esempio 1: Creare una porta anteriore in base a specifici parametri.</span><span class="sxs-lookup"><span data-stu-id="e3445-110">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="e3445-111">Creare una porta anteriore in base a specifici parametri.</span><span class="sxs-lookup"><span data-stu-id="e3445-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="e3445-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3445-112">PARAMETERS</span></span>

### <span data-ttu-id="e3445-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="e3445-113">-BackendPool</span></span>
<span data-ttu-id="e3445-114">Pool di back-end disponibili per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="e3445-114">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3445-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="e3445-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="e3445-116">Impostazioni per tutti i back-endPool</span><span class="sxs-lookup"><span data-stu-id="e3445-116">Settings for all backendPools</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3445-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3445-117">-DefaultProfile</span></span>
<span data-ttu-id="e3445-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3445-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3445-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="e3445-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="e3445-120">Se disabilitare il controllo del nome del certificato nelle richieste HTTPS a tutti i pool back-end.</span><span class="sxs-lookup"><span data-stu-id="e3445-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="e3445-121">Nessun effetto sulle richieste non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e3445-121">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3445-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e3445-122">-EnabledState</span></span>
<span data-ttu-id="e3445-123">EnabledState della bilanciamento del carico anteriore.</span><span class="sxs-lookup"><span data-stu-id="e3445-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="e3445-124">Il valore predefinito è Abilitato</span><span class="sxs-lookup"><span data-stu-id="e3445-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="e3445-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3445-125">-FrontendEndpoint</span></span>
<span data-ttu-id="e3445-126">Endpoint di frontend disponibili per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="e3445-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3445-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="e3445-127">-HealthProbeSetting</span></span>
<span data-ttu-id="e3445-128">Impostazioni integrità associate all'istanza di Front Door.</span><span class="sxs-lookup"><span data-stu-id="e3445-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3445-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="e3445-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="e3445-130">Impostazioni di bilanciamento del carico associate a questa istanza di Front Door.</span><span class="sxs-lookup"><span data-stu-id="e3445-130">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3445-131">-Name</span><span class="sxs-lookup"><span data-stu-id="e3445-131">-Name</span></span>
<span data-ttu-id="e3445-132">Nome della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="e3445-132">Front Door name.</span></span>

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

### <span data-ttu-id="e3445-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3445-133">-ResourceGroupName</span></span>
<span data-ttu-id="e3445-134">Nome del gruppo di risorse con cui verrà creata la porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="e3445-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="e3445-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="e3445-135">-RoutingRule</span></span>
<span data-ttu-id="e3445-136">Regole di routing associate a FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3445-136">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3445-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3445-137">-Tag</span></span>
<span data-ttu-id="e3445-138">I tag associati a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e3445-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="e3445-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3445-139">-Confirm</span></span>
<span data-ttu-id="e3445-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3445-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3445-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3445-141">-WhatIf</span></span>
<span data-ttu-id="e3445-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3445-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3445-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3445-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3445-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3445-144">CommonParameters</span></span>
<span data-ttu-id="e3445-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3445-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3445-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3445-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3445-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3445-147">INPUTS</span></span>

### <span data-ttu-id="e3445-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3445-148">None</span></span>
## <span data-ttu-id="e3445-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3445-149">OUTPUTS</span></span>

### <span data-ttu-id="e3445-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3445-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="e3445-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3445-151">NOTES</span></span>

## <span data-ttu-id="e3445-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3445-152">RELATED LINKS</span></span>

<span data-ttu-id="e3445-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="e3445-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>