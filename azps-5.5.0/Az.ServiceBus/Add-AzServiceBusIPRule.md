---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: 7eb4265042083135f8306f601e2a14818aaacb06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201695"
---
# <span data-ttu-id="b2ea9-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="b2ea9-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="b2ea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ea9-103">Aggiungere una singola regola IP a NetworkRuleSet dello spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="b2ea9-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="b2ea9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2ea9-104">SYNTAX</span></span>

### <span data-ttu-id="b2ea9-105">IPRulePropertiesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2ea9-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2ea9-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2ea9-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2ea9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b2ea9-107">DESCRIPTION</span></span>
<span data-ttu-id="b2ea9-108">Aggiungere una singola regola IP a NetworkRuleSet dello spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="b2ea9-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="b2ea9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2ea9-109">EXAMPLES</span></span>

### <span data-ttu-id="b2ea9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b2ea9-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="b2ea9-111">Name : default DefaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="b2ea9-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="b2ea9-112">aggiungere ipRule con IpMask "11.22.33.44" e Action Allow per lo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="b2ea9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b2ea9-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="b2ea9-114">Name : default DefaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="b2ea9-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="b2ea9-115">aggiungere ipRule con IpMask "11.22.33.44" e Action Allow per lo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="b2ea9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2ea9-116">PARAMETERS</span></span>

### <span data-ttu-id="b2ea9-117">-Action</span><span class="sxs-lookup"><span data-stu-id="b2ea9-117">-Action</span></span>
<span data-ttu-id="b2ea9-118">Azione filtro IP</span><span class="sxs-lookup"><span data-stu-id="b2ea9-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="b2ea9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ea9-119">-DefaultProfile</span></span>
<span data-ttu-id="b2ea9-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2ea9-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="b2ea9-121">-IpMask</span></span>
<span data-ttu-id="b2ea9-122">ID risorsa subnet</span><span class="sxs-lookup"><span data-stu-id="b2ea9-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="b2ea9-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="b2ea9-123">-IpRuleObject</span></span>
<span data-ttu-id="b2ea9-124">Oggetto configurazione IPRule da aggiungere</span><span class="sxs-lookup"><span data-stu-id="b2ea9-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="b2ea9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b2ea9-125">-Name</span></span>
<span data-ttu-id="b2ea9-126">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2ea9-126">Namespace Name</span></span>

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

### <span data-ttu-id="b2ea9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2ea9-127">-ResourceGroupName</span></span>
<span data-ttu-id="b2ea9-128">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b2ea9-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b2ea9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2ea9-129">-Confirm</span></span>
<span data-ttu-id="b2ea9-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2ea9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2ea9-131">-WhatIf</span></span>
<span data-ttu-id="b2ea9-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2ea9-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2ea9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ea9-134">CommonParameters</span></span>
<span data-ttu-id="b2ea9-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b2ea9-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2ea9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ea9-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="b2ea9-137">INPUTS</span></span>

### <span data-ttu-id="b2ea9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b2ea9-138">System.String</span></span>

### <span data-ttu-id="b2ea9-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="b2ea9-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="b2ea9-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2ea9-140">OUTPUTS</span></span>

### <span data-ttu-id="b2ea9-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="b2ea9-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="b2ea9-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="b2ea9-142">NOTES</span></span>

## <span data-ttu-id="b2ea9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2ea9-143">RELATED LINKS</span></span>