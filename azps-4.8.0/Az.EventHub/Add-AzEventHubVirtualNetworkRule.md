---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 627519cd4325e7fb9677c358146f2f8a9081151a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192933"
---
# <span data-ttu-id="d497f-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d497f-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="d497f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d497f-102">SYNOPSIS</span></span>
<span data-ttu-id="d497f-103">Aggiungere un singolo VirtualNetworkRule a NetworkRuleSet per lo spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="d497f-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="d497f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d497f-104">SYNTAX</span></span>

### <span data-ttu-id="d497f-105">VirtualNetworkRulePropertiesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d497f-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d497f-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d497f-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d497f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d497f-107">DESCRIPTION</span></span>
<span data-ttu-id="d497f-108">Aggiungere un singolo VirtualNetworkRule a NetworkRuleSet per lo spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="d497f-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="d497f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d497f-109">EXAMPLES</span></span>

### <span data-ttu-id="d497f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d497f-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="d497f-111">Name: default DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default tipo: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="d497f-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="d497f-112">Aggiunge la subnet specificata e IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) a NetworkRuleSet per lo spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="d497f-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="d497f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d497f-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="d497f-114">Name: default DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default tipo: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="d497f-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="d497f-115">Aggiunge la $virtualruleset da 1 a NetworkRuleSet per lo spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="d497f-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="d497f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d497f-116">PARAMETERS</span></span>

### <span data-ttu-id="d497f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d497f-117">-DefaultProfile</span></span>
<span data-ttu-id="d497f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d497f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d497f-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d497f-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="d497f-120">ID ARM della subnet</span><span class="sxs-lookup"><span data-stu-id="d497f-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="d497f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d497f-121">-Name</span></span>
<span data-ttu-id="d497f-122">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d497f-122">Namespace Name</span></span>

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

### <span data-ttu-id="d497f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d497f-123">-ResourceGroupName</span></span>
<span data-ttu-id="d497f-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d497f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d497f-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d497f-125">-SubnetId</span></span>
<span data-ttu-id="d497f-126">ID risorsa subnet</span><span class="sxs-lookup"><span data-stu-id="d497f-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="d497f-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="d497f-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="d497f-128">Oggetto di configurazione VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d497f-128">VirtualNetworkRule Configuration Object</span></span>

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

### <span data-ttu-id="d497f-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d497f-129">-Confirm</span></span>
<span data-ttu-id="d497f-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d497f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d497f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d497f-131">-WhatIf</span></span>
<span data-ttu-id="d497f-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d497f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d497f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d497f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d497f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d497f-134">CommonParameters</span></span>
<span data-ttu-id="d497f-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d497f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d497f-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d497f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d497f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d497f-137">INPUTS</span></span>

### <span data-ttu-id="d497f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d497f-138">System.String</span></span>

### <span data-ttu-id="d497f-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d497f-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d497f-140">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="d497f-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="d497f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d497f-141">OUTPUTS</span></span>

### <span data-ttu-id="d497f-142">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d497f-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="d497f-143">Note</span><span class="sxs-lookup"><span data-stu-id="d497f-143">NOTES</span></span>

## <span data-ttu-id="d497f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d497f-144">RELATED LINKS</span></span>
