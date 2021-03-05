---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 339569d3415edadbf284f904358f889e7210267a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015982"
---
# <span data-ttu-id="fbb27-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fbb27-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="fbb27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbb27-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb27-103">Rimuove NetworkRuleSet per lo spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="fbb27-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="fbb27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbb27-104">SYNTAX</span></span>

### <span data-ttu-id="fbb27-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fbb27-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb27-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fbb27-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb27-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbb27-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbb27-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fbb27-108">DESCRIPTION</span></span>
<span data-ttu-id="fbb27-109">Rimuove NetworkRuleSet per lo spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="fbb27-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="fbb27-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbb27-110">EXAMPLES</span></span>

### <span data-ttu-id="fbb27-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fbb27-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="fbb27-112">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="fbb27-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="fbb27-113">Elimina NetworkRuleSet per lo spazio dei nomi assegnato "ServiceBus-Namespace1-1375"</span><span class="sxs-lookup"><span data-stu-id="fbb27-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="fbb27-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fbb27-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="fbb27-115">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="fbb27-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="fbb27-116">Elimina NetworkRuleSet con InputObject</span><span class="sxs-lookup"><span data-stu-id="fbb27-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="fbb27-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="fbb27-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="fbb27-118">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="fbb27-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="fbb27-119">Elimina NetworkRuleSet usando ResourceId dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fbb27-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="fbb27-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbb27-120">PARAMETERS</span></span>

### <span data-ttu-id="fbb27-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbb27-121">-AsJob</span></span>
<span data-ttu-id="fbb27-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fbb27-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb27-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb27-123">-DefaultProfile</span></span>
<span data-ttu-id="fbb27-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb27-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb27-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbb27-125">-InputObject</span></span>
<span data-ttu-id="fbb27-126">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="fbb27-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb27-127">-Name</span><span class="sxs-lookup"><span data-stu-id="fbb27-127">-Name</span></span>
<span data-ttu-id="fbb27-128">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fbb27-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb27-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbb27-129">-PassThru</span></span>
<span data-ttu-id="fbb27-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fbb27-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb27-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb27-131">-ResourceGroupName</span></span>
<span data-ttu-id="fbb27-132">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fbb27-132">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb27-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbb27-133">-ResourceId</span></span>
<span data-ttu-id="fbb27-134">ID risorsa spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fbb27-134">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb27-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbb27-135">-Confirm</span></span>
<span data-ttu-id="fbb27-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb27-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb27-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb27-137">-WhatIf</span></span>
<span data-ttu-id="fbb27-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbb27-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb27-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbb27-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb27-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb27-140">CommonParameters</span></span>
<span data-ttu-id="fbb27-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb27-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fbb27-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbb27-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb27-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="fbb27-143">INPUTS</span></span>

### <span data-ttu-id="fbb27-144">Microsoft.Azure.Commands.ServiceBus.Models.PSAttributes</span><span class="sxs-lookup"><span data-stu-id="fbb27-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="fbb27-145">System.String</span><span class="sxs-lookup"><span data-stu-id="fbb27-145">System.String</span></span>

## <span data-ttu-id="fbb27-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbb27-146">OUTPUTS</span></span>

### <span data-ttu-id="fbb27-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb27-147">System.Boolean</span></span>

## <span data-ttu-id="fbb27-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="fbb27-148">NOTES</span></span>

## <span data-ttu-id="fbb27-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbb27-149">RELATED LINKS</span></span>
