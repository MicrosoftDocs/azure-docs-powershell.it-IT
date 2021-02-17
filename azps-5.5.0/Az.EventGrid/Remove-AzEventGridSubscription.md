---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: a2e2b27023e9af9f08db6446d6d2808402ca27cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188486"
---
# <span data-ttu-id="70674-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="70674-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="70674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70674-102">SYNOPSIS</span></span>
<span data-ttu-id="70674-103">Rimuove una sottoscrizione di evento della griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="70674-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="70674-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70674-104">SYNTAX</span></span>

### <span data-ttu-id="70674-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70674-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70674-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="70674-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70674-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70674-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70674-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70674-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70674-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70674-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70674-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="70674-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70674-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="70674-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70674-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="70674-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70674-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="70674-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70674-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="70674-114">DESCRIPTION</span></span>
<span data-ttu-id="70674-115">Rimuove una sottoscrizione a un evento della Griglia eventi di Azure per un argomento griglia eventi di Azure, una risorsa, una sottoscrizione o un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="70674-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="70674-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70674-116">EXAMPLES</span></span>

### <span data-ttu-id="70674-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="70674-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="70674-118">Rimuove la sottoscrizione evento EventSubscription1 in un argomento Griglia eventi di Azure Topic1 nel gruppo \` \` di risorse \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="70674-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="70674-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="70674-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="70674-120">Rimuove la sottoscrizione evento \` EventSubscription1 \` a un gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="70674-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="70674-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="70674-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="70674-122">Rimuove la sottoscrizione evento \` EventSubscription1 \` dalla sottoscrizione predefinita di Azure.</span><span class="sxs-lookup"><span data-stu-id="70674-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="70674-123">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="70674-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="70674-124">Rimuove la sottoscrizione evento \` EventSubscription1 in uno \` spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="70674-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="70674-125">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="70674-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="70674-126">Rimuove la sottoscrizione \` dell'evento EventSubscription1 \` in un argomento della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="70674-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="70674-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70674-127">PARAMETERS</span></span>

### <span data-ttu-id="70674-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70674-128">-DefaultProfile</span></span>
<span data-ttu-id="70674-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="70674-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70674-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="70674-130">-DomainInputObject</span></span>
<span data-ttu-id="70674-131">Oggetto Dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="70674-131">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70674-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="70674-132">-DomainName</span></span>
<span data-ttu-id="70674-133">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="70674-133">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70674-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="70674-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="70674-135">Oggetto Domain Topic di EventGrid.</span><span class="sxs-lookup"><span data-stu-id="70674-135">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70674-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="70674-136">-DomainTopicName</span></span>
<span data-ttu-id="70674-137">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="70674-137">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70674-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="70674-138">-EventSubscriptionName</span></span>
<span data-ttu-id="70674-139">Nome della sottoscrizione dell'evento che deve essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="70674-139">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet, DomainNameParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70674-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70674-140">-InputObject</span></span>
<span data-ttu-id="70674-141">Oggetto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="70674-141">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70674-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70674-142">-PassThru</span></span>
<span data-ttu-id="70674-143">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="70674-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="70674-144">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="70674-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="70674-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70674-145">-ResourceGroupName</span></span>
<span data-ttu-id="70674-146">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="70674-146">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70674-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70674-147">-ResourceId</span></span>
<span data-ttu-id="70674-148">Identificatore della risorsa di cui rimuovere la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="70674-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70674-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="70674-149">-TopicName</span></span>
<span data-ttu-id="70674-150">Nome argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="70674-150">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70674-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70674-151">-Confirm</span></span>
<span data-ttu-id="70674-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70674-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70674-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70674-153">-WhatIf</span></span>
<span data-ttu-id="70674-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70674-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70674-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70674-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70674-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70674-156">CommonParameters</span></span>
<span data-ttu-id="70674-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70674-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70674-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70674-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70674-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="70674-159">INPUTS</span></span>

### <span data-ttu-id="70674-160">System.String</span><span class="sxs-lookup"><span data-stu-id="70674-160">System.String</span></span>

### <span data-ttu-id="70674-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="70674-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="70674-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="70674-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="70674-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="70674-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="70674-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70674-164">OUTPUTS</span></span>

### <span data-ttu-id="70674-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70674-165">System.Boolean</span></span>

## <span data-ttu-id="70674-166">NOTE</span><span class="sxs-lookup"><span data-stu-id="70674-166">NOTES</span></span>

## <span data-ttu-id="70674-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70674-167">RELATED LINKS</span></span>
