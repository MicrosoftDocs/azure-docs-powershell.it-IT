---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: cea5b69b279b6f7f7a8e783d4ed328237377c18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674386"
---
# <span data-ttu-id="2c162-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="2c162-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="2c162-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c162-102">SYNOPSIS</span></span>
<span data-ttu-id="2c162-103">Creare un nuovo bilanciamento del carico di Azure front door</span><span class="sxs-lookup"><span data-stu-id="2c162-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="2c162-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c162-104">SYNTAX</span></span>

```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c162-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c162-105">DESCRIPTION</span></span>
<span data-ttu-id="2c162-106">Il cmdlet **New-AzFrontDoor** crea un nuovo bilanciamento del carico di Azure porta anteriore nel gruppo di risorse specificato in abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="2c162-106">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="2c162-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c162-107">EXAMPLES</span></span>

### <span data-ttu-id="2c162-108">Esempio 1: creare uno sportello anteriore in base a determinati parametri.</span><span class="sxs-lookup"><span data-stu-id="2c162-108">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="2c162-109">Creare uno sportello anteriore in base a determinati parametri.</span><span class="sxs-lookup"><span data-stu-id="2c162-109">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="2c162-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c162-110">PARAMETERS</span></span>

### <span data-ttu-id="2c162-111">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="2c162-111">-BackendPool</span></span>
<span data-ttu-id="2c162-112">Backendpools disponibile per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="2c162-112">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="2c162-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c162-113">-DefaultProfile</span></span>
<span data-ttu-id="2c162-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c162-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c162-115">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="2c162-115">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="2c162-116">Se disabilitare il controllo nome certificato per le richieste HTTPS a tutti i pool back-end.</span><span class="sxs-lookup"><span data-stu-id="2c162-116">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="2c162-117">Nessun effetto sulle richieste non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2c162-117">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="2c162-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="2c162-118">-EnabledState</span></span>
<span data-ttu-id="2c162-119">EnabledState del bilanciamento del carico della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="2c162-119">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="2c162-120">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="2c162-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="2c162-121">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c162-121">-FrontendEndpoint</span></span>
<span data-ttu-id="2c162-122">Endpoint frontend disponibili per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="2c162-122">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="2c162-123">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="2c162-123">-HealthProbeSetting</span></span>
<span data-ttu-id="2c162-124">Impostazioni della sonda integrità associate all'istanza di porta principale.</span><span class="sxs-lookup"><span data-stu-id="2c162-124">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="2c162-125">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="2c162-125">-LoadBalancingSetting</span></span>
<span data-ttu-id="2c162-126">Impostazioni di bilanciamento del carico associate all'istanza di porta principale.</span><span class="sxs-lookup"><span data-stu-id="2c162-126">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="2c162-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c162-127">-Name</span></span>
<span data-ttu-id="2c162-128">Nome porta principale.</span><span class="sxs-lookup"><span data-stu-id="2c162-128">Front Door name.</span></span>

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

### <span data-ttu-id="2c162-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c162-129">-ResourceGroupName</span></span>
<span data-ttu-id="2c162-130">Nome del gruppo di risorse in cui verrà creata la porta principale.</span><span class="sxs-lookup"><span data-stu-id="2c162-130">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="2c162-131">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="2c162-131">-RoutingRule</span></span>
<span data-ttu-id="2c162-132">Regole di routing associate a questo FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2c162-132">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="2c162-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="2c162-133">-Tag</span></span>
<span data-ttu-id="2c162-134">I tag si associano a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="2c162-134">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="2c162-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2c162-135">-Confirm</span></span>
<span data-ttu-id="2c162-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c162-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c162-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c162-137">-WhatIf</span></span>
<span data-ttu-id="2c162-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c162-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c162-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c162-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c162-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c162-140">CommonParameters</span></span>
<span data-ttu-id="2c162-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c162-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c162-142">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c162-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c162-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c162-143">INPUTS</span></span>

### <span data-ttu-id="2c162-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2c162-144">None</span></span>

## <span data-ttu-id="2c162-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c162-145">OUTPUTS</span></span>

### <span data-ttu-id="2c162-146">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="2c162-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="2c162-147">Note</span><span class="sxs-lookup"><span data-stu-id="2c162-147">NOTES</span></span>

## <span data-ttu-id="2c162-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c162-148">RELATED LINKS</span></span>

<span data-ttu-id="2c162-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="2c162-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>