---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: 82d386fb0834db3de03d5692ad8b7a241b6eed90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516628"
---
# <span data-ttu-id="e63aa-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e63aa-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="e63aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e63aa-102">SYNOPSIS</span></span>
<span data-ttu-id="e63aa-103">Rimuove un abbonamento a un evento Grid evento Azure.</span><span class="sxs-lookup"><span data-stu-id="e63aa-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e63aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e63aa-104">SYNTAX</span></span>

### <span data-ttu-id="e63aa-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e63aa-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e63aa-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e63aa-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e63aa-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e63aa-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e63aa-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e63aa-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e63aa-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e63aa-109">DESCRIPTION</span></span>
<span data-ttu-id="e63aa-110">Rimuove un abbonamento a un evento della griglia di eventi di Azure per un argomento della griglia di eventi di Azure, una risorsa, un abbonamento a Azure o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e63aa-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="e63aa-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e63aa-111">EXAMPLES</span></span>

### <span data-ttu-id="e63aa-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e63aa-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="e63aa-113">Rimuove la sottoscrizione dell'evento \` EventSubscription1 in \` un argomento della griglia di eventi di Azure \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e63aa-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e63aa-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e63aa-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="e63aa-115">Rimuove la sottoscrizione dell'evento \` EventSubscription1 \` a un gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e63aa-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e63aa-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e63aa-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="e63aa-117">Rimuove la sottoscrizione dell'evento \` EventSubscription1 \` all'abbonamento Azure predefinito.</span><span class="sxs-lookup"><span data-stu-id="e63aa-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="e63aa-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="e63aa-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="e63aa-119">Rimuove la sottoscrizione dell'evento \` EventSubscription1 \` in uno spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="e63aa-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="e63aa-120">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="e63aa-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="e63aa-121">Rimuove l'argomento della sottoscrizione dell'evento \` EventSubscription1 \` in una griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="e63aa-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="e63aa-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e63aa-122">PARAMETERS</span></span>

### <span data-ttu-id="e63aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e63aa-123">-DefaultProfile</span></span>
<span data-ttu-id="e63aa-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e63aa-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63aa-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e63aa-125">-EventSubscriptionName</span></span>
<span data-ttu-id="e63aa-126">Nome dell'abbonamento a un evento che deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="e63aa-126">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e63aa-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e63aa-127">-InputObject</span></span>
<span data-ttu-id="e63aa-128">Oggetto EventSubscription EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e63aa-128">EventGrid EventSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e63aa-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e63aa-129">-PassThru</span></span>
<span data-ttu-id="e63aa-130">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="e63aa-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="e63aa-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e63aa-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e63aa-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e63aa-132">-ResourceGroupName</span></span>
<span data-ttu-id="e63aa-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e63aa-133">Resource Group Name.</span></span>

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
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e63aa-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e63aa-134">-ResourceId</span></span>
<span data-ttu-id="e63aa-135">Identificatore della risorsa la cui sottoscrizione di eventi deve essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="e63aa-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="e63aa-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="e63aa-136">-TopicName</span></span>
<span data-ttu-id="e63aa-137">Nome argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="e63aa-137">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="e63aa-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e63aa-138">-Confirm</span></span>
<span data-ttu-id="e63aa-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e63aa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e63aa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e63aa-140">-WhatIf</span></span>
<span data-ttu-id="e63aa-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e63aa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e63aa-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e63aa-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e63aa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e63aa-143">CommonParameters</span></span>
<span data-ttu-id="e63aa-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e63aa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e63aa-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e63aa-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e63aa-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e63aa-146">INPUTS</span></span>

### <span data-ttu-id="e63aa-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e63aa-147">System.String</span></span>

### <span data-ttu-id="e63aa-148">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="e63aa-148">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="e63aa-149">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e63aa-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e63aa-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e63aa-150">OUTPUTS</span></span>

### <span data-ttu-id="e63aa-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e63aa-151">System.Boolean</span></span>

## <span data-ttu-id="e63aa-152">Note</span><span class="sxs-lookup"><span data-stu-id="e63aa-152">NOTES</span></span>

## <span data-ttu-id="e63aa-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e63aa-153">RELATED LINKS</span></span>
