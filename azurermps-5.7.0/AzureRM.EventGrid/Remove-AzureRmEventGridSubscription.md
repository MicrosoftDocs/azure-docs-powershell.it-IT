---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: 681f831ba93943676b6aadb59378efcdd4e79579
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508168"
---
# <span data-ttu-id="e6b64-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e6b64-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="e6b64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6b64-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b64-103">Rimuove un abbonamento a un evento Grid evento Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b64-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6b64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6b64-104">SYNTAX</span></span>

### <span data-ttu-id="e6b64-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6b64-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b64-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b64-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b64-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e6b64-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b64-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b64-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6b64-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6b64-109">DESCRIPTION</span></span>
<span data-ttu-id="e6b64-110">Rimuove un abbonamento a un evento della griglia di eventi di Azure per un argomento della griglia di eventi di Azure, una risorsa, un abbonamento a Azure o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e6b64-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="e6b64-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6b64-111">EXAMPLES</span></span>

### <span data-ttu-id="e6b64-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6b64-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="e6b64-113">Rimuove la sottoscrizione dell'evento \` EventSubscription1 in \` un argomento della griglia di eventi di Azure \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e6b64-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e6b64-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e6b64-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="e6b64-115">Rimuove la sottoscrizione dell'evento \` EventSubscription1 \` a un gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e6b64-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e6b64-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e6b64-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="e6b64-117">Rimuove la sottoscrizione dell'evento \` EventSubscription1 \` all'abbonamento Azure predefinito.</span><span class="sxs-lookup"><span data-stu-id="e6b64-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="e6b64-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="e6b64-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="e6b64-119">Rimuove la sottoscrizione dell'evento \` EventSubscription1 \` in uno spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="e6b64-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="e6b64-120">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="e6b64-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="e6b64-121">Rimuove l'argomento della sottoscrizione dell'evento \` EventSubscription1 \` in una griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="e6b64-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="e6b64-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6b64-122">PARAMETERS</span></span>

### <span data-ttu-id="e6b64-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b64-123">-DefaultProfile</span></span>
<span data-ttu-id="e6b64-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e6b64-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b64-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e6b64-125">-EventSubscriptionName</span></span>
<span data-ttu-id="e6b64-126">Nome dell'abbonamento a un evento che deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="e6b64-126">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b64-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6b64-127">-InputObject</span></span>
<span data-ttu-id="e6b64-128">Oggetto EventSubscription EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e6b64-128">EventGrid EventSubscription object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b64-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6b64-129">-PassThru</span></span>
<span data-ttu-id="e6b64-130">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="e6b64-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="e6b64-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e6b64-131">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b64-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b64-132">-ResourceGroupName</span></span>
<span data-ttu-id="e6b64-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e6b64-133">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b64-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6b64-134">-ResourceId</span></span>
<span data-ttu-id="e6b64-135">Identificatore della risorsa la cui sottoscrizione di eventi deve essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="e6b64-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b64-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="e6b64-136">-TopicName</span></span>
<span data-ttu-id="e6b64-137">Nome argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="e6b64-137">Event Grid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b64-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6b64-138">-Confirm</span></span>
<span data-ttu-id="e6b64-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6b64-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b64-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6b64-140">-WhatIf</span></span>
<span data-ttu-id="e6b64-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6b64-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6b64-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6b64-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b64-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b64-143">CommonParameters</span></span>
<span data-ttu-id="e6b64-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b64-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b64-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6b64-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b64-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6b64-146">INPUTS</span></span>

### <span data-ttu-id="e6b64-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e6b64-147">System.String</span></span>
<span data-ttu-id="e6b64-148">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="e6b64-148">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="e6b64-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6b64-149">OUTPUTS</span></span>

### <span data-ttu-id="e6b64-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="e6b64-150">System.Object</span></span>

## <span data-ttu-id="e6b64-151">Note</span><span class="sxs-lookup"><span data-stu-id="e6b64-151">NOTES</span></span>

## <span data-ttu-id="e6b64-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6b64-152">RELATED LINKS</span></span>

