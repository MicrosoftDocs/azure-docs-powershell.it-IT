---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: e0450df003b474cae57319d5450423af58f4d3eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967597"
---
# <span data-ttu-id="b7d66-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="b7d66-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="b7d66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7d66-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d66-103">Aggiungere una singola regola IP a NetworkRuleSet dello spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="b7d66-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="b7d66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7d66-104">SYNTAX</span></span>

### <span data-ttu-id="b7d66-105">IPRulePropertiesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7d66-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7d66-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7d66-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7d66-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b7d66-107">DESCRIPTION</span></span>
<span data-ttu-id="b7d66-108">Aggiungere una singola regola IP a NetworkRuleSet dello spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="b7d66-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="b7d66-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7d66-109">EXAMPLES</span></span>

### <span data-ttu-id="b7d66-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b7d66-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="b7d66-111">Name : default DefaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="b7d66-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="b7d66-112">aggiungere IPRule con IpMask "11.22.33.44" e Action Allow per lo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="b7d66-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="b7d66-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b7d66-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="b7d66-114">Nome: defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="b7d66-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="b7d66-115">aggiungere ipRule con IpMask "11.22.33.44" e Action Allow per lo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="b7d66-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="b7d66-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7d66-116">PARAMETERS</span></span>

### <span data-ttu-id="b7d66-117">-Action</span><span class="sxs-lookup"><span data-stu-id="b7d66-117">-Action</span></span>
<span data-ttu-id="b7d66-118">Azione filtro IP</span><span class="sxs-lookup"><span data-stu-id="b7d66-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d66-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d66-119">-DefaultProfile</span></span>
<span data-ttu-id="b7d66-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7d66-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7d66-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="b7d66-121">-IpMask</span></span>
<span data-ttu-id="b7d66-122">ID risorsa subnet</span><span class="sxs-lookup"><span data-stu-id="b7d66-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d66-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="b7d66-123">-IpRuleObject</span></span>
<span data-ttu-id="b7d66-124">Oggetto configurazione IPRule da aggiungere</span><span class="sxs-lookup"><span data-stu-id="b7d66-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d66-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b7d66-125">-Name</span></span>
<span data-ttu-id="b7d66-126">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b7d66-126">Namespace Name</span></span>

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

### <span data-ttu-id="b7d66-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7d66-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7d66-128">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b7d66-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b7d66-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7d66-129">-Confirm</span></span>
<span data-ttu-id="b7d66-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7d66-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7d66-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7d66-131">-WhatIf</span></span>
<span data-ttu-id="b7d66-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7d66-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7d66-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7d66-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7d66-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d66-134">CommonParameters</span></span>
<span data-ttu-id="b7d66-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7d66-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b7d66-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7d66-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d66-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="b7d66-137">INPUTS</span></span>

### <span data-ttu-id="b7d66-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b7d66-138">System.String</span></span>

### <span data-ttu-id="b7d66-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="b7d66-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="b7d66-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7d66-140">OUTPUTS</span></span>

### <span data-ttu-id="b7d66-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="b7d66-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="b7d66-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="b7d66-142">NOTES</span></span>

## <span data-ttu-id="b7d66-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7d66-143">RELATED LINKS</span></span>