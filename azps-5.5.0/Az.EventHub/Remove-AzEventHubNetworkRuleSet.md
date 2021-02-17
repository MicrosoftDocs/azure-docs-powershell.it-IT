---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209538"
---
# <span data-ttu-id="d1bdf-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d1bdf-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="d1bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="d1bdf-103">Rimuove NetworkRuleSet per lo spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="d1bdf-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="d1bdf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1bdf-104">SYNTAX</span></span>

### <span data-ttu-id="d1bdf-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1bdf-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1bdf-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d1bdf-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1bdf-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1bdf-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1bdf-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d1bdf-108">DESCRIPTION</span></span>
<span data-ttu-id="d1bdf-109">Rimuove NetworkRuleSet per lo spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="d1bdf-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="d1bdf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1bdf-110">EXAMPLES</span></span>

### <span data-ttu-id="d1bdf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1bdf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="d1bdf-112">Nome: default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="d1bdf-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="d1bdf-113">Elimina NetworkRuleSet per lo spazio dei nomi Assegnato "Eventhub-Spazio dei nomi1-1375"</span><span class="sxs-lookup"><span data-stu-id="d1bdf-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="d1bdf-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d1bdf-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="d1bdf-115">Elimina NetworkRuleSet con InputObject</span><span class="sxs-lookup"><span data-stu-id="d1bdf-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="d1bdf-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d1bdf-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="d1bdf-117">Nome: default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="d1bdf-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="d1bdf-118">Elimina NetworkRuleSet usando ResourceId dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d1bdf-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="d1bdf-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1bdf-119">PARAMETERS</span></span>

### <span data-ttu-id="d1bdf-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1bdf-120">-AsJob</span></span>
<span data-ttu-id="d1bdf-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d1bdf-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1bdf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1bdf-122">-DefaultProfile</span></span>
<span data-ttu-id="d1bdf-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1bdf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1bdf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1bdf-124">-InputObject</span></span>
<span data-ttu-id="d1bdf-125">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="d1bdf-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1bdf-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d1bdf-126">-Name</span></span>
<span data-ttu-id="d1bdf-127">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d1bdf-127">Namespace Name</span></span>

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

### <span data-ttu-id="d1bdf-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1bdf-128">-PassThru</span></span>
<span data-ttu-id="d1bdf-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d1bdf-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d1bdf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1bdf-130">-ResourceGroupName</span></span>
<span data-ttu-id="d1bdf-131">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d1bdf-131">Resource Group Name</span></span>

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

### <span data-ttu-id="d1bdf-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1bdf-132">-ResourceId</span></span>
<span data-ttu-id="d1bdf-133">ID risorsa spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d1bdf-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="d1bdf-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1bdf-134">-Confirm</span></span>
<span data-ttu-id="d1bdf-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1bdf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1bdf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1bdf-136">-WhatIf</span></span>
<span data-ttu-id="d1bdf-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1bdf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1bdf-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1bdf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1bdf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1bdf-139">CommonParameters</span></span>
<span data-ttu-id="d1bdf-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1bdf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d1bdf-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1bdf-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1bdf-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="d1bdf-142">INPUTS</span></span>

### <span data-ttu-id="d1bdf-143">Microsoft.Azure.Commands.EventHub.Models.PSAttributeAttributes</span><span class="sxs-lookup"><span data-stu-id="d1bdf-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="d1bdf-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d1bdf-144">System.String</span></span>

## <span data-ttu-id="d1bdf-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1bdf-145">OUTPUTS</span></span>

### <span data-ttu-id="d1bdf-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1bdf-146">System.Boolean</span></span>

## <span data-ttu-id="d1bdf-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="d1bdf-147">NOTES</span></span>

## <span data-ttu-id="d1bdf-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1bdf-148">RELATED LINKS</span></span>