---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: a2e2b27023e9af9f08db6446d6d2808402ca27cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192946"
---
# <span data-ttu-id="7d1bd-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7d1bd-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="7d1bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1bd-103">Rimuove un abbonamento a un evento Grid evento Azure.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="7d1bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d1bd-104">SYNTAX</span></span>

### <span data-ttu-id="7d1bd-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d1bd-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1bd-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1bd-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1bd-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1bd-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1bd-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1bd-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1bd-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1bd-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1bd-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1bd-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d1bd-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1bd-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1bd-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1bd-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1bd-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1bd-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d1bd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d1bd-114">DESCRIPTION</span></span>
<span data-ttu-id="7d1bd-115">Rimuove un abbonamento a un evento della griglia di eventi di Azure per un argomento della griglia di eventi di Azure, una risorsa, un abbonamento a Azure o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="7d1bd-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d1bd-116">EXAMPLES</span></span>

### <span data-ttu-id="7d1bd-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d1bd-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7d1bd-118">Rimuove la sottoscrizione dell'evento \` EventSubscription1 in \` un argomento della griglia di eventi di Azure \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7d1bd-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7d1bd-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7d1bd-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7d1bd-120">Rimuove la sottoscrizione dell'evento \` EventSubscription1 \` a un gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7d1bd-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7d1bd-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7d1bd-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7d1bd-122">Rimuove la sottoscrizione dell'evento \` EventSubscription1 \` all'abbonamento Azure predefinito.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="7d1bd-123">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="7d1bd-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7d1bd-124">Rimuove la sottoscrizione dell'evento \` EventSubscription1 \` in uno spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="7d1bd-125">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="7d1bd-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7d1bd-126">Rimuove l'argomento della sottoscrizione dell'evento \` EventSubscription1 \` in una griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="7d1bd-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d1bd-127">PARAMETERS</span></span>

### <span data-ttu-id="7d1bd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1bd-128">-DefaultProfile</span></span>
<span data-ttu-id="7d1bd-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7d1bd-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d1bd-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="7d1bd-130">-DomainInputObject</span></span>
<span data-ttu-id="7d1bd-131">Oggetto di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="7d1bd-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="7d1bd-132">-DomainName</span></span>
<span data-ttu-id="7d1bd-133">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="7d1bd-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="7d1bd-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="7d1bd-135">Oggetto argomento del dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="7d1bd-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="7d1bd-136">-DomainTopicName</span></span>
<span data-ttu-id="7d1bd-137">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="7d1bd-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7d1bd-138">-EventSubscriptionName</span></span>
<span data-ttu-id="7d1bd-139">Nome dell'abbonamento a un evento che deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="7d1bd-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d1bd-140">-InputObject</span></span>
<span data-ttu-id="7d1bd-141">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="7d1bd-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d1bd-142">-PassThru</span></span>
<span data-ttu-id="7d1bd-143">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="7d1bd-144">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7d1bd-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1bd-145">-ResourceGroupName</span></span>
<span data-ttu-id="7d1bd-146">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="7d1bd-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d1bd-147">-ResourceId</span></span>
<span data-ttu-id="7d1bd-148">Identificatore della risorsa la cui sottoscrizione di eventi deve essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="7d1bd-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7d1bd-149">-TopicName</span></span>
<span data-ttu-id="7d1bd-150">Nome argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="7d1bd-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d1bd-151">-Confirm</span></span>
<span data-ttu-id="7d1bd-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d1bd-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1bd-153">-WhatIf</span></span>
<span data-ttu-id="7d1bd-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d1bd-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d1bd-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1bd-156">CommonParameters</span></span>
<span data-ttu-id="7d1bd-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1bd-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d1bd-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1bd-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d1bd-159">INPUTS</span></span>

### <span data-ttu-id="7d1bd-160">System. String</span><span class="sxs-lookup"><span data-stu-id="7d1bd-160">System.String</span></span>

### <span data-ttu-id="7d1bd-161">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="7d1bd-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="7d1bd-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="7d1bd-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="7d1bd-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7d1bd-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="7d1bd-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d1bd-164">OUTPUTS</span></span>

### <span data-ttu-id="7d1bd-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d1bd-165">System.Boolean</span></span>

## <span data-ttu-id="7d1bd-166">Note</span><span class="sxs-lookup"><span data-stu-id="7d1bd-166">NOTES</span></span>

## <span data-ttu-id="7d1bd-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d1bd-167">RELATED LINKS</span></span>