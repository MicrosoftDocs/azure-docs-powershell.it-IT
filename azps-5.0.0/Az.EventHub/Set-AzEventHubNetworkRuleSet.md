---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 6f769613516dbd1f94400832bd8fac0045fec198
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193415"
---
# <span data-ttu-id="1426b-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1426b-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="1426b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1426b-102">SYNOPSIS</span></span>
<span data-ttu-id="1426b-103">Aggiornare il NetworkruleSet dello spazio dei nomi specifico nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="1426b-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="1426b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1426b-104">SYNTAX</span></span>

### <span data-ttu-id="1426b-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1426b-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1426b-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1426b-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1426b-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1426b-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1426b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1426b-108">DESCRIPTION</span></span>
<span data-ttu-id="1426b-109">Aggiornare il NetworkruleSet dello spazio dei nomi specifico nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="1426b-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="1426b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1426b-110">EXAMPLES</span></span>

### <span data-ttu-id="1426b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1426b-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="1426b-112">Name: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default tipo: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="1426b-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="1426b-113">Aggiornare il NetworkRuleSet usando i parametri-IPRule e-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1426b-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="1426b-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1426b-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="1426b-115">Name: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default tipo: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="1426b-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="1426b-116">Aggiornare il NetworkRuleSet con-InputObject</span><span class="sxs-lookup"><span data-stu-id="1426b-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="1426b-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1426b-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="1426b-118">Name: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default tipo: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="1426b-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="1426b-119">Aggiornare il NetworkRuleSet using-ResourceId dell'altro spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="1426b-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="1426b-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1426b-120">PARAMETERS</span></span>

### <span data-ttu-id="1426b-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="1426b-121">-DefaultAction</span></span>
<span data-ttu-id="1426b-122">Azione predefinita per NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1426b-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="1426b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1426b-123">-DefaultProfile</span></span>
<span data-ttu-id="1426b-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1426b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1426b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1426b-125">-InputObject</span></span>
<span data-ttu-id="1426b-126">Oggetto di configurazione NetworkruleSet</span><span class="sxs-lookup"><span data-stu-id="1426b-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1426b-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="1426b-127">-IPRule</span></span>
<span data-ttu-id="1426b-128">Elenco di IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="1426b-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1426b-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="1426b-129">-Name</span></span>
<span data-ttu-id="1426b-130">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="1426b-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="1426b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1426b-131">-ResourceGroupName</span></span>
<span data-ttu-id="1426b-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1426b-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="1426b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1426b-133">-ResourceId</span></span>
<span data-ttu-id="1426b-134">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1426b-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="1426b-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="1426b-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="1426b-136">Indica se TrustedServiceAccessEnabled è abilitato</span><span class="sxs-lookup"><span data-stu-id="1426b-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1426b-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1426b-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="1426b-138">Elenco di VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="1426b-138">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1426b-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1426b-139">-Confirm</span></span>
<span data-ttu-id="1426b-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1426b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1426b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1426b-141">-WhatIf</span></span>
<span data-ttu-id="1426b-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1426b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1426b-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1426b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1426b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1426b-144">CommonParameters</span></span>
<span data-ttu-id="1426b-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1426b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1426b-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1426b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1426b-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1426b-147">INPUTS</span></span>

### <span data-ttu-id="1426b-148">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="1426b-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="1426b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1426b-149">System.String</span></span>

## <span data-ttu-id="1426b-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1426b-150">OUTPUTS</span></span>

### <span data-ttu-id="1426b-151">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="1426b-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="1426b-152">Note</span><span class="sxs-lookup"><span data-stu-id="1426b-152">NOTES</span></span>

## <span data-ttu-id="1426b-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1426b-153">RELATED LINKS</span></span>