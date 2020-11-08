---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200893"
---
# <span data-ttu-id="d3592-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d3592-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="d3592-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3592-102">SYNOPSIS</span></span>
<span data-ttu-id="d3592-103">Creare un nuovo bilanciamento del carico di Azure front door</span><span class="sxs-lookup"><span data-stu-id="d3592-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="d3592-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3592-104">SYNTAX</span></span>

### <span data-ttu-id="d3592-105">ByFieldsWithBackendPoolsSettingParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3592-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3592-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3592-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3592-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3592-107">DESCRIPTION</span></span>
<span data-ttu-id="d3592-108">Il cmdlet **New-AzFrontDoor** crea un nuovo bilanciamento del carico di Azure porta anteriore nel gruppo di risorse specificato in abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="d3592-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="d3592-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3592-109">EXAMPLES</span></span>

### <span data-ttu-id="d3592-110">Esempio 1: creare uno sportello anteriore in base a determinati parametri.</span><span class="sxs-lookup"><span data-stu-id="d3592-110">Example 1: Create a Front Door based on given parameters.</span></span>
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

<span data-ttu-id="d3592-111">Creare uno sportello anteriore in base a determinati parametri.</span><span class="sxs-lookup"><span data-stu-id="d3592-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="d3592-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3592-112">PARAMETERS</span></span>

### <span data-ttu-id="d3592-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="d3592-113">-BackendPool</span></span>
<span data-ttu-id="d3592-114">Backendpools disponibile per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="d3592-114">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="d3592-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="d3592-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="d3592-116">Impostazioni per tutti i backendPools</span><span class="sxs-lookup"><span data-stu-id="d3592-116">Settings for all backendPools</span></span>

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

### <span data-ttu-id="d3592-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3592-117">-DefaultProfile</span></span>
<span data-ttu-id="d3592-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3592-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3592-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="d3592-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="d3592-120">Se disabilitare il controllo nome certificato per le richieste HTTPS a tutti i pool back-end.</span><span class="sxs-lookup"><span data-stu-id="d3592-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="d3592-121">Nessun effetto sulle richieste non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d3592-121">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="d3592-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d3592-122">-EnabledState</span></span>
<span data-ttu-id="d3592-123">EnabledState del bilanciamento del carico della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="d3592-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="d3592-124">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="d3592-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="d3592-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3592-125">-FrontendEndpoint</span></span>
<span data-ttu-id="d3592-126">Endpoint frontend disponibili per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="d3592-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="d3592-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="d3592-127">-HealthProbeSetting</span></span>
<span data-ttu-id="d3592-128">Impostazioni della sonda integrità associate all'istanza di porta principale.</span><span class="sxs-lookup"><span data-stu-id="d3592-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="d3592-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="d3592-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="d3592-130">Impostazioni di bilanciamento del carico associate all'istanza di porta principale.</span><span class="sxs-lookup"><span data-stu-id="d3592-130">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="d3592-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3592-131">-Name</span></span>
<span data-ttu-id="d3592-132">Nome porta principale.</span><span class="sxs-lookup"><span data-stu-id="d3592-132">Front Door name.</span></span>

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

### <span data-ttu-id="d3592-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3592-133">-ResourceGroupName</span></span>
<span data-ttu-id="d3592-134">Nome del gruppo di risorse in cui verrà creata la porta principale.</span><span class="sxs-lookup"><span data-stu-id="d3592-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="d3592-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3592-135">-RoutingRule</span></span>
<span data-ttu-id="d3592-136">Regole di routing associate a questo FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d3592-136">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="d3592-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="d3592-137">-Tag</span></span>
<span data-ttu-id="d3592-138">I tag si associano a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="d3592-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="d3592-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3592-139">-Confirm</span></span>
<span data-ttu-id="d3592-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3592-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3592-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3592-141">-WhatIf</span></span>
<span data-ttu-id="d3592-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3592-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3592-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3592-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3592-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3592-144">CommonParameters</span></span>
<span data-ttu-id="d3592-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3592-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3592-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3592-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3592-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3592-147">INPUTS</span></span>

### <span data-ttu-id="d3592-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d3592-148">None</span></span>
## <span data-ttu-id="d3592-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3592-149">OUTPUTS</span></span>

### <span data-ttu-id="d3592-150">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d3592-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="d3592-151">Note</span><span class="sxs-lookup"><span data-stu-id="d3592-151">NOTES</span></span>

## <span data-ttu-id="d3592-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3592-152">RELATED LINKS</span></span>

<span data-ttu-id="d3592-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="d3592-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>