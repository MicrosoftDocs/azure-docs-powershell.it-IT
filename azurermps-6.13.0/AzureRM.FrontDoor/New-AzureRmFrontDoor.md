---
<span data-ttu-id="47b52-101">file della Guida esterno: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml nome modulo: AzureRM. FrontDoor versione online: l'URL corrispondente deve essere il seguente: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span><span class="sxs-lookup"><span data-stu-id="47b52-101">external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Module Name: AzureRM.FrontDoor online version: The corresponding URL should be the following: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span></span>
---

# <a name="new-azurermfrontdoor"></a><span data-ttu-id="47b52-102">New-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="47b52-102">New-AzureRmFrontDoor</span></span>

## <a name="synopsis"></a><span data-ttu-id="47b52-103">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47b52-103">SYNOPSIS</span></span>
<span data-ttu-id="47b52-104">Creare un nuovo bilanciamento del carico di Azure front door</span><span class="sxs-lookup"><span data-stu-id="47b52-104">Create a new Azure Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a><span data-ttu-id="47b52-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47b52-105">SYNTAX</span></span>

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a><span data-ttu-id="47b52-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47b52-106">DESCRIPTION</span></span>
<span data-ttu-id="47b52-107">Il cmdlet **New-AzureRmFrontDoor** crea un nuovo bilanciamento del carico di Azure porta anteriore nel gruppo di risorse specificato in abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="47b52-107">The **New-AzureRmFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <a name="examples"></a><span data-ttu-id="47b52-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47b52-108">EXAMPLES</span></span>

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a><span data-ttu-id="47b52-109">Esempio 1: creare uno sportello anteriore in base a determinati parametri.</span><span class="sxs-lookup"><span data-stu-id="47b52-109">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="47b52-110">Creare uno sportello anteriore in base a determinati parametri.</span><span class="sxs-lookup"><span data-stu-id="47b52-110">Create a Front Door based on given parameters.</span></span>

## <a name="parameters"></a><span data-ttu-id="47b52-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47b52-111">PARAMETERS</span></span>

### <a name="-backendpool"></a><span data-ttu-id="47b52-112">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="47b52-112">-BackendPool</span></span>
<span data-ttu-id="47b52-113">Backendpools disponibile per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="47b52-113">Backendpools available to routing rule.</span></span>

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

### <a name="-defaultprofile"></a><span data-ttu-id="47b52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b52-114">-DefaultProfile</span></span>
<span data-ttu-id="47b52-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47b52-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <a name="-enabledstate"></a><span data-ttu-id="47b52-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="47b52-116">-EnabledState</span></span>
<span data-ttu-id="47b52-117">EnabledState del bilanciamento del carico della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="47b52-117">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="47b52-118">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="47b52-118">Default value is Enabled</span></span>

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

### <a name="-frontendendpoint"></a><span data-ttu-id="47b52-119">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="47b52-119">-FrontendEndpoint</span></span>
<span data-ttu-id="47b52-120">Endpoint frontend disponibili per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="47b52-120">Frontend endpoints available to routing rule.</span></span>

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

### <a name="-healthprobesetting"></a><span data-ttu-id="47b52-121">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="47b52-121">-HealthProbeSetting</span></span>
<span data-ttu-id="47b52-122">Impostazioni della sonda integrità associate all'istanza di porta principale.</span><span class="sxs-lookup"><span data-stu-id="47b52-122">Health probe settings associated with this Front Door instance.</span></span>

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

### <a name="-loadbalancingsetting"></a><span data-ttu-id="47b52-123">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="47b52-123">-LoadBalancingSetting</span></span>
<span data-ttu-id="47b52-124">Impostazioni di bilanciamento del carico associate all'istanza di porta principale.</span><span class="sxs-lookup"><span data-stu-id="47b52-124">Load balancing settings associated with this Front Door instance.</span></span>

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

### <a name="-name"></a><span data-ttu-id="47b52-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="47b52-125">-Name</span></span>
<span data-ttu-id="47b52-126">Nome porta principale.</span><span class="sxs-lookup"><span data-stu-id="47b52-126">Front Door name.</span></span>

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

### <a name="-resourcegroupname"></a><span data-ttu-id="47b52-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b52-127">-ResourceGroupName</span></span>
<span data-ttu-id="47b52-128">Nome del gruppo di risorse in cui verrà creata la porta principale.</span><span class="sxs-lookup"><span data-stu-id="47b52-128">The resource group name that the Front Door will be created in.</span></span>

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

### <a name="-routingrule"></a><span data-ttu-id="47b52-129">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="47b52-129">-RoutingRule</span></span>
<span data-ttu-id="47b52-130">Regole di routing associate a questo FrontDoor</span><span class="sxs-lookup"><span data-stu-id="47b52-130">Routing rules associated with this FrontDoor</span></span>

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

### <a name="-tag"></a><span data-ttu-id="47b52-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="47b52-131">-Tag</span></span>
<span data-ttu-id="47b52-132">I tag si associano a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="47b52-132">The tags associate with the FrontDoor.</span></span>

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

### <a name="-confirm"></a><span data-ttu-id="47b52-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47b52-133">-Confirm</span></span>
<span data-ttu-id="47b52-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47b52-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <a name="-whatif"></a><span data-ttu-id="47b52-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b52-135">-WhatIf</span></span>
<span data-ttu-id="47b52-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47b52-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b52-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47b52-137">The cmdlet is not run.</span></span>

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

### <a name="commonparameters"></a><span data-ttu-id="47b52-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b52-138">CommonParameters</span></span>
<span data-ttu-id="47b52-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b52-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b52-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47b52-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <a name="inputs"></a><span data-ttu-id="47b52-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47b52-141">INPUTS</span></span>

### <a name="systemstring"></a><span data-ttu-id="47b52-142">System. String</span><span class="sxs-lookup"><span data-stu-id="47b52-142">System.String</span></span>

## <a name="outputs"></a><span data-ttu-id="47b52-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47b52-143">OUTPUTS</span></span>

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a><span data-ttu-id="47b52-144">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="47b52-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <a name="notes"></a><span data-ttu-id="47b52-145">Note</span><span class="sxs-lookup"><span data-stu-id="47b52-145">NOTES</span></span>

## <a name="related-links"></a><span data-ttu-id="47b52-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47b52-146">RELATED LINKS</span></span>

<span data-ttu-id="47b52-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="47b52-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
