---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 72fd6da6c0abc6419acf3917ebe43fda0fdcfa2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981646"
---
# <span data-ttu-id="a8606-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8606-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="a8606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8606-102">SYNOPSIS</span></span>
<span data-ttu-id="a8606-103">Aggiornare NetworkruleSet dello spazio dei nomi specificato nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="a8606-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="a8606-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8606-104">SYNTAX</span></span>

### <span data-ttu-id="a8606-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8606-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8606-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a8606-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8606-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8606-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8606-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a8606-108">DESCRIPTION</span></span>
<span data-ttu-id="a8606-109">Aggiornare NetwrokruleSet dello spazio dei nomi specificato nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="a8606-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="a8606-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8606-110">EXAMPLES</span></span>

### <span data-ttu-id="a8606-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8606-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="a8606-112">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="a8606-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="a8606-113">Aggiornare NetworkRuleSet con i parametri -IPRule e -VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a8606-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="a8606-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a8606-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="a8606-115">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="a8606-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="a8606-116">Aggiornare NetworkRuleSet con -InputObject</span><span class="sxs-lookup"><span data-stu-id="a8606-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="a8606-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a8606-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="a8606-118">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="a8606-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="a8606-119">Aggiornare NetworkRuleSet usando -ResourceId dell'altro spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a8606-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="a8606-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8606-120">PARAMETERS</span></span>

### <span data-ttu-id="a8606-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="a8606-121">-DefaultAction</span></span>
<span data-ttu-id="a8606-122">Azione predefinita per NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8606-122">Default Action for NetworkRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8606-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8606-123">-DefaultProfile</span></span>
<span data-ttu-id="a8606-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8606-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8606-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8606-125">-InputObject</span></span>
<span data-ttu-id="a8606-126">NetworkruleSet Configuration Object</span><span class="sxs-lookup"><span data-stu-id="a8606-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8606-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="a8606-127">-IPRule</span></span>
<span data-ttu-id="a8606-128">Elenco di IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8606-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8606-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a8606-129">-Name</span></span>
<span data-ttu-id="a8606-130">Nome dello spazio dei nomi di EventHub.</span><span class="sxs-lookup"><span data-stu-id="a8606-130">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8606-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8606-131">-ResourceGroupName</span></span>
<span data-ttu-id="a8606-132">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a8606-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8606-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8606-133">-ResourceId</span></span>
<span data-ttu-id="a8606-134">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a8606-134">Resource ID of Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8606-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a8606-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="a8606-136">Elenco di VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="a8606-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8606-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8606-137">-Confirm</span></span>
<span data-ttu-id="a8606-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8606-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8606-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8606-139">-WhatIf</span></span>
<span data-ttu-id="a8606-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8606-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8606-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8606-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8606-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8606-142">CommonParameters</span></span>
<span data-ttu-id="a8606-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8606-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a8606-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8606-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8606-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="a8606-145">INPUTS</span></span>

### <span data-ttu-id="a8606-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a8606-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="a8606-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a8606-147">System.String</span></span>

## <span data-ttu-id="a8606-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8606-148">OUTPUTS</span></span>

### <span data-ttu-id="a8606-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a8606-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="a8606-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="a8606-150">NOTES</span></span>

## <span data-ttu-id="a8606-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8606-151">RELATED LINKS</span></span>