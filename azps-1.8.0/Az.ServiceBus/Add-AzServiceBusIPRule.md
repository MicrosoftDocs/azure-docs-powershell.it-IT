---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: df7cf094482f849782d6570b0df1af8cbadb7077
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677176"
---
# <span data-ttu-id="de84f-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="de84f-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="de84f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de84f-102">SYNOPSIS</span></span>
<span data-ttu-id="de84f-103">Aggiungere un singolo IPrule alla NetworkRuleSet dello spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="de84f-103">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="de84f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de84f-104">SYNTAX</span></span>

### <span data-ttu-id="de84f-105">IPRulePropertiesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de84f-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de84f-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de84f-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de84f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de84f-107">DESCRIPTION</span></span>
<span data-ttu-id="de84f-108">Aggiungere un singolo IPrule alla NetworkRuleSet dello spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="de84f-108">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="de84f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de84f-109">EXAMPLES</span></span>

### <span data-ttu-id="de84f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de84f-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="de84f-111">Nome: default DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default tipo: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="de84f-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="de84f-112">Aggiungi il IPRule con IpMask "11.22.33.44" e l'azione Consenti fro l'file specificata.</span><span class="sxs-lookup"><span data-stu-id="de84f-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namesapce.</span></span>

### <span data-ttu-id="de84f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="de84f-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="de84f-114">Nome: default DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default tipo: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="de84f-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="de84f-115">Aggiungi il IPRule con IpMask "11.22.33.44" e l'azione Consenti fro l'file specificata.</span><span class="sxs-lookup"><span data-stu-id="de84f-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namesapce.</span></span>

## <span data-ttu-id="de84f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de84f-116">PARAMETERS</span></span>

### <span data-ttu-id="de84f-117">-Azione</span><span class="sxs-lookup"><span data-stu-id="de84f-117">-Action</span></span>
<span data-ttu-id="de84f-118">Azione filtro IP</span><span class="sxs-lookup"><span data-stu-id="de84f-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="de84f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de84f-119">-DefaultProfile</span></span>
<span data-ttu-id="de84f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de84f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de84f-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="de84f-121">-IpMask</span></span>
<span data-ttu-id="de84f-122">ID risorsa subnet</span><span class="sxs-lookup"><span data-stu-id="de84f-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="de84f-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="de84f-123">-IpRuleObject</span></span>
<span data-ttu-id="de84f-124">Oggetto di configurazione IPRule da aggiungere</span><span class="sxs-lookup"><span data-stu-id="de84f-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="de84f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="de84f-125">-Name</span></span>
<span data-ttu-id="de84f-126">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="de84f-126">Namespace Name</span></span>

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

### <span data-ttu-id="de84f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de84f-127">-ResourceGroupName</span></span>
<span data-ttu-id="de84f-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="de84f-128">Resource Group Name</span></span>

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

### <span data-ttu-id="de84f-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="de84f-129">-Confirm</span></span>
<span data-ttu-id="de84f-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de84f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de84f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de84f-131">-WhatIf</span></span>
<span data-ttu-id="de84f-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de84f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de84f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de84f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de84f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de84f-134">CommonParameters</span></span>
<span data-ttu-id="de84f-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de84f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="de84f-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de84f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de84f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de84f-137">INPUTS</span></span>

### <span data-ttu-id="de84f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="de84f-138">System.String</span></span>

### <span data-ttu-id="de84f-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="de84f-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="de84f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de84f-140">OUTPUTS</span></span>

### <span data-ttu-id="de84f-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="de84f-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="de84f-142">Note</span><span class="sxs-lookup"><span data-stu-id="de84f-142">NOTES</span></span>

## <span data-ttu-id="de84f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de84f-143">RELATED LINKS</span></span>