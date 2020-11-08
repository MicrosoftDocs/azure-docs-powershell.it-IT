---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 54846520fd8370d171a20970eda1d42af81e4d0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192938"
---
# <span data-ttu-id="40228-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="40228-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="40228-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40228-102">SYNOPSIS</span></span>
<span data-ttu-id="40228-103">Aggiungere una singola regola IP alla NetworkRuleSet dello spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="40228-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="40228-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40228-104">SYNTAX</span></span>

### <span data-ttu-id="40228-105">IPRulePropertiesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="40228-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40228-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40228-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40228-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40228-107">DESCRIPTION</span></span>
<span data-ttu-id="40228-108">Aggiungere una singola regola IP alla NetworkRuleSet dello spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="40228-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="40228-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40228-109">EXAMPLES</span></span>

### <span data-ttu-id="40228-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="40228-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="40228-111">Name: default DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default tipo: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="40228-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="40228-112">Aggiungi IPRule con IpMask "11.22.33.44" e azione Consenti per lo spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="40228-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="40228-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="40228-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="40228-114">Name: default DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default tipo: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="40228-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="40228-115">Aggiungi IPRule con IpMask "11.22.33.44" e azione Consenti per lo spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="40228-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="40228-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40228-116">PARAMETERS</span></span>

### <span data-ttu-id="40228-117">-Azione</span><span class="sxs-lookup"><span data-stu-id="40228-117">-Action</span></span>
<span data-ttu-id="40228-118">Azione filtro IP</span><span class="sxs-lookup"><span data-stu-id="40228-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="40228-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40228-119">-DefaultProfile</span></span>
<span data-ttu-id="40228-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40228-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40228-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="40228-121">-IpMask</span></span>
<span data-ttu-id="40228-122">ID risorsa subnet</span><span class="sxs-lookup"><span data-stu-id="40228-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="40228-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="40228-123">-IpRuleObject</span></span>
<span data-ttu-id="40228-124">Oggetto di configurazione IPRule da aggiungere</span><span class="sxs-lookup"><span data-stu-id="40228-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40228-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="40228-125">-Name</span></span>
<span data-ttu-id="40228-126">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="40228-126">Namespace Name</span></span>

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

### <span data-ttu-id="40228-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40228-127">-ResourceGroupName</span></span>
<span data-ttu-id="40228-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="40228-128">Resource Group Name</span></span>

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

### <span data-ttu-id="40228-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="40228-129">-Confirm</span></span>
<span data-ttu-id="40228-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40228-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40228-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40228-131">-WhatIf</span></span>
<span data-ttu-id="40228-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40228-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40228-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40228-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40228-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40228-134">CommonParameters</span></span>
<span data-ttu-id="40228-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40228-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="40228-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40228-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40228-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40228-137">INPUTS</span></span>

### <span data-ttu-id="40228-138">System. String</span><span class="sxs-lookup"><span data-stu-id="40228-138">System.String</span></span>

### <span data-ttu-id="40228-139">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="40228-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="40228-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40228-140">OUTPUTS</span></span>

### <span data-ttu-id="40228-141">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="40228-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="40228-142">Note</span><span class="sxs-lookup"><span data-stu-id="40228-142">NOTES</span></span>

## <span data-ttu-id="40228-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40228-143">RELATED LINKS</span></span>
