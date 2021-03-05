---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 1625e3325164156b1809640c54d4b75698ae7363
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991197"
---
# <span data-ttu-id="ee07b-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ee07b-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="ee07b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee07b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee07b-103">Rimuove la sottoscrizione di un evento della griglia degli eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee07b-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="ee07b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee07b-104">SYNTAX</span></span>

### <span data-ttu-id="ee07b-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ee07b-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee07b-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee07b-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee07b-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee07b-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee07b-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee07b-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee07b-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee07b-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee07b-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee07b-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee07b-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee07b-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee07b-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee07b-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee07b-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee07b-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee07b-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ee07b-114">DESCRIPTION</span></span>
<span data-ttu-id="ee07b-115">Rimuove una sottoscrizione a un evento della Griglia eventi di Azure per un argomento griglia eventi di Azure, una risorsa, una sottoscrizione o un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee07b-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="ee07b-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee07b-116">EXAMPLES</span></span>

### <span data-ttu-id="ee07b-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee07b-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ee07b-118">Rimuove la sottoscrizione evento EventSubscription1 in un argomento Griglia eventi di Azure Topic1 nel gruppo \` \` di risorse \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="ee07b-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ee07b-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ee07b-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ee07b-120">Rimuove la sottoscrizione evento \` EventSubscription1 a un gruppo \` di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="ee07b-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ee07b-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ee07b-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ee07b-122">Rimuove la sottoscrizione evento \` EventSubscription1 \` dalla sottoscrizione predefinita di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee07b-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="ee07b-123">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="ee07b-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ee07b-124">Rimuove la sottoscrizione evento \` EventSubscription1 in uno \` spazio dei nomi dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="ee07b-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="ee07b-125">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="ee07b-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ee07b-126">Rimuove la sottoscrizione evento \` EventSubscription1 \` in un argomento della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="ee07b-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="ee07b-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee07b-127">PARAMETERS</span></span>

### <span data-ttu-id="ee07b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee07b-128">-DefaultProfile</span></span>
<span data-ttu-id="ee07b-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ee07b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee07b-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="ee07b-130">-DomainInputObject</span></span>
<span data-ttu-id="ee07b-131">Oggetto Domain EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ee07b-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="ee07b-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="ee07b-132">-DomainName</span></span>
<span data-ttu-id="ee07b-133">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ee07b-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="ee07b-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="ee07b-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="ee07b-135">Oggetto Domain Topic di EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ee07b-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="ee07b-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="ee07b-136">-DomainTopicName</span></span>
<span data-ttu-id="ee07b-137">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ee07b-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="ee07b-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ee07b-138">-EventSubscriptionName</span></span>
<span data-ttu-id="ee07b-139">Nome della sottoscrizione dell'evento che deve essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="ee07b-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="ee07b-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee07b-140">-InputObject</span></span>
<span data-ttu-id="ee07b-141">Oggetto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="ee07b-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="ee07b-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee07b-142">-PassThru</span></span>
<span data-ttu-id="ee07b-143">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="ee07b-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="ee07b-144">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ee07b-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee07b-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee07b-145">-ResourceGroupName</span></span>
<span data-ttu-id="ee07b-146">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ee07b-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee07b-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee07b-147">-ResourceId</span></span>
<span data-ttu-id="ee07b-148">Identificatore della risorsa di cui rimuovere la sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="ee07b-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="ee07b-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ee07b-149">-TopicName</span></span>
<span data-ttu-id="ee07b-150">Nome argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="ee07b-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="ee07b-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee07b-151">-Confirm</span></span>
<span data-ttu-id="ee07b-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee07b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee07b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee07b-153">-WhatIf</span></span>
<span data-ttu-id="ee07b-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee07b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee07b-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee07b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee07b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee07b-156">CommonParameters</span></span>
<span data-ttu-id="ee07b-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee07b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee07b-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee07b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee07b-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="ee07b-159">INPUTS</span></span>

### <span data-ttu-id="ee07b-160">System.String</span><span class="sxs-lookup"><span data-stu-id="ee07b-160">System.String</span></span>

### <span data-ttu-id="ee07b-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="ee07b-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="ee07b-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="ee07b-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="ee07b-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ee07b-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="ee07b-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee07b-164">OUTPUTS</span></span>

### <span data-ttu-id="ee07b-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee07b-165">System.Boolean</span></span>

## <span data-ttu-id="ee07b-166">NOTE</span><span class="sxs-lookup"><span data-stu-id="ee07b-166">NOTES</span></span>

## <span data-ttu-id="ee07b-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee07b-167">RELATED LINKS</span></span>
