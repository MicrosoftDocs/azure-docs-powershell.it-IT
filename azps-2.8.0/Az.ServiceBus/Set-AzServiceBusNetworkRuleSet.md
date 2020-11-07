---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 9465ad8d6f66b62da8b224ab635ca45fed1a8ca1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856137"
---
# <span data-ttu-id="5294c-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5294c-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="5294c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5294c-102">SYNOPSIS</span></span>
<span data-ttu-id="5294c-103">Aggiornare il NetworkruleSet dello spazio dei nomi specifico nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="5294c-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="5294c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5294c-104">SYNTAX</span></span>

### <span data-ttu-id="5294c-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5294c-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5294c-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5294c-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5294c-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5294c-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5294c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5294c-108">DESCRIPTION</span></span>
<span data-ttu-id="5294c-109">Aggiornare il NetwrokruleSet dello spazio dei nomi specifico nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="5294c-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="5294c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5294c-110">EXAMPLES</span></span>

### <span data-ttu-id="5294c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5294c-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="5294c-112">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default tipo: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="5294c-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="5294c-113">Aggiornare il NetworkRuleSet usando i parametri-IPRule e-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5294c-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="5294c-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5294c-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="5294c-115">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default tipo: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="5294c-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="5294c-116">Aggiornare il NetworkRuleSet con-InputObject</span><span class="sxs-lookup"><span data-stu-id="5294c-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="5294c-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5294c-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="5294c-118">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default tipo: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="5294c-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="5294c-119">Aggiornare il NetworkRuleSet using-ResourceId dell'altro spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5294c-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="5294c-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5294c-120">PARAMETERS</span></span>

### <span data-ttu-id="5294c-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="5294c-121">-DefaultAction</span></span>
<span data-ttu-id="5294c-122">Azione predefinita per NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5294c-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="5294c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5294c-123">-DefaultProfile</span></span>
<span data-ttu-id="5294c-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5294c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5294c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5294c-125">-InputObject</span></span>
<span data-ttu-id="5294c-126">Oggetto di configurazione NetworkruleSet</span><span class="sxs-lookup"><span data-stu-id="5294c-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="5294c-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="5294c-127">-IPRule</span></span>
<span data-ttu-id="5294c-128">Elenco di IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="5294c-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="5294c-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="5294c-129">-Name</span></span>
<span data-ttu-id="5294c-130">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="5294c-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="5294c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5294c-131">-ResourceGroupName</span></span>
<span data-ttu-id="5294c-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5294c-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="5294c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5294c-133">-ResourceId</span></span>
<span data-ttu-id="5294c-134">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5294c-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="5294c-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5294c-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="5294c-136">Elenco di VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="5294c-136">List of VirtualNetworkRules</span></span>

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

### <span data-ttu-id="5294c-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5294c-137">-Confirm</span></span>
<span data-ttu-id="5294c-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5294c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5294c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5294c-139">-WhatIf</span></span>
<span data-ttu-id="5294c-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5294c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5294c-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5294c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5294c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5294c-142">CommonParameters</span></span>
<span data-ttu-id="5294c-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5294c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5294c-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5294c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5294c-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5294c-145">INPUTS</span></span>

### <span data-ttu-id="5294c-146">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="5294c-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="5294c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5294c-147">System.String</span></span>

## <span data-ttu-id="5294c-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5294c-148">OUTPUTS</span></span>

### <span data-ttu-id="5294c-149">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="5294c-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="5294c-150">Note</span><span class="sxs-lookup"><span data-stu-id="5294c-150">NOTES</span></span>

## <span data-ttu-id="5294c-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5294c-151">RELATED LINKS</span></span>