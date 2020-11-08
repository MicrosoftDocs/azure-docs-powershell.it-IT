---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202129"
---
# <span data-ttu-id="c3888-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3888-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="c3888-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3888-102">SYNOPSIS</span></span>
<span data-ttu-id="c3888-103">Rimuove NetworkRuleSet per lo spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="c3888-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="c3888-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3888-104">SYNTAX</span></span>

### <span data-ttu-id="c3888-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3888-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3888-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3888-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3888-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3888-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3888-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3888-108">DESCRIPTION</span></span>
<span data-ttu-id="c3888-109">Rimuove NetworkRuleSet per lo spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="c3888-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="c3888-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3888-110">EXAMPLES</span></span>

### <span data-ttu-id="c3888-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c3888-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="c3888-112">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="c3888-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="c3888-113">Elimina il NetworkRuleSet per lo spazio dei nomi "Eventhub-Namespace1-1375" indicato</span><span class="sxs-lookup"><span data-stu-id="c3888-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="c3888-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c3888-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="c3888-115">Elimina il NetworkRuleSet usando InputObject</span><span class="sxs-lookup"><span data-stu-id="c3888-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="c3888-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c3888-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="c3888-117">Nome: default DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="c3888-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="c3888-118">Elimina NetworkRuleSet usando ResourceId dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c3888-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="c3888-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3888-119">PARAMETERS</span></span>

### <span data-ttu-id="c3888-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3888-120">-AsJob</span></span>
<span data-ttu-id="c3888-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c3888-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3888-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3888-122">-DefaultProfile</span></span>
<span data-ttu-id="c3888-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3888-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3888-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3888-124">-InputObject</span></span>
<span data-ttu-id="c3888-125">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="c3888-125">Namespace Object</span></span>

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

### <span data-ttu-id="c3888-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3888-126">-Name</span></span>
<span data-ttu-id="c3888-127">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c3888-127">Namespace Name</span></span>

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

### <span data-ttu-id="c3888-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3888-128">-PassThru</span></span>
<span data-ttu-id="c3888-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c3888-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c3888-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3888-130">-ResourceGroupName</span></span>
<span data-ttu-id="c3888-131">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c3888-131">Resource Group Name</span></span>

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

### <span data-ttu-id="c3888-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3888-132">-ResourceId</span></span>
<span data-ttu-id="c3888-133">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c3888-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="c3888-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c3888-134">-Confirm</span></span>
<span data-ttu-id="c3888-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3888-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3888-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3888-136">-WhatIf</span></span>
<span data-ttu-id="c3888-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3888-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3888-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3888-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3888-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3888-139">CommonParameters</span></span>
<span data-ttu-id="c3888-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3888-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c3888-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3888-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3888-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3888-142">INPUTS</span></span>

### <span data-ttu-id="c3888-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c3888-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="c3888-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c3888-144">System.String</span></span>

## <span data-ttu-id="c3888-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3888-145">OUTPUTS</span></span>

### <span data-ttu-id="c3888-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3888-146">System.Boolean</span></span>

## <span data-ttu-id="c3888-147">Note</span><span class="sxs-lookup"><span data-stu-id="c3888-147">NOTES</span></span>

## <span data-ttu-id="c3888-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3888-148">RELATED LINKS</span></span>