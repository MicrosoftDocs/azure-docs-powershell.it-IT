---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 098fc29dd518f62b5b813e4698f5a111947eff3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963069"
---
# <span data-ttu-id="ddd63-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ddd63-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="ddd63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddd63-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd63-103">Aggiungere un'unica regola VirtualNetworkRule a NetworkRuleSet per lo spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="ddd63-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="ddd63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddd63-104">SYNTAX</span></span>

### <span data-ttu-id="ddd63-105">VirtualNetworkRulePropertiesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ddd63-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddd63-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd63-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd63-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ddd63-107">DESCRIPTION</span></span>
<span data-ttu-id="ddd63-108">Aggiungere un'unica regola VirtualNetworkRule a NetworkRuleSet per lo spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="ddd63-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="ddd63-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddd63-109">EXAMPLES</span></span>

### <span data-ttu-id="ddd63-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ddd63-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="ddd63-111">Name : default DefaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type : Microsoft.Eventhub/Spazio dei nomi/NetworkRuleSet IpRules : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="ddd63-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="ddd63-112">Aggiunge la subnet specificata e IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) a NetworkRuleSet per lo spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="ddd63-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="ddd63-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ddd63-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="ddd63-114">Name : default DefaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type : Microsoft.Eventhub/Spazio dei nomi/NetworkRuleSet IpRules : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="ddd63-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="ddd63-115">Aggiunge la $virtualruleset 1 a NetworkRuleSet per lo spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="ddd63-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="ddd63-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddd63-116">PARAMETERS</span></span>

### <span data-ttu-id="ddd63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd63-117">-DefaultProfile</span></span>
<span data-ttu-id="ddd63-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddd63-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ddd63-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="ddd63-120">ARM ID della subnet</span><span class="sxs-lookup"><span data-stu-id="ddd63-120">ARM ID of Subnet</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd63-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ddd63-121">-Name</span></span>
<span data-ttu-id="ddd63-122">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ddd63-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd63-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd63-123">-ResourceGroupName</span></span>
<span data-ttu-id="ddd63-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ddd63-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd63-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ddd63-125">-SubnetId</span></span>
<span data-ttu-id="ddd63-126">ID risorsa subnet</span><span class="sxs-lookup"><span data-stu-id="ddd63-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd63-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ddd63-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="ddd63-128">Oggetto di configurazione VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ddd63-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd63-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddd63-129">-Confirm</span></span>
<span data-ttu-id="ddd63-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd63-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd63-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd63-131">-WhatIf</span></span>
<span data-ttu-id="ddd63-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddd63-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd63-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddd63-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd63-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd63-134">CommonParameters</span></span>
<span data-ttu-id="ddd63-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd63-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ddd63-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd63-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd63-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="ddd63-137">INPUTS</span></span>

### <span data-ttu-id="ddd63-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ddd63-138">System.String</span></span>

### <span data-ttu-id="ddd63-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ddd63-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ddd63-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="ddd63-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="ddd63-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddd63-141">OUTPUTS</span></span>

### <span data-ttu-id="ddd63-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ddd63-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ddd63-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="ddd63-143">NOTES</span></span>

## <span data-ttu-id="ddd63-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddd63-144">RELATED LINKS</span></span>
