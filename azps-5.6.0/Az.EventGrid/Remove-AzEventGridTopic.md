---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: 3960f73d115b881bdffab89c225a9321e19af067
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991170"
---
# <span data-ttu-id="b442b-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="b442b-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="b442b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b442b-102">SYNOPSIS</span></span>
<span data-ttu-id="b442b-103">Rimuove un argomento griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="b442b-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="b442b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b442b-104">SYNTAX</span></span>

### <span data-ttu-id="b442b-105">TopicNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b442b-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b442b-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b442b-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b442b-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b442b-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b442b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b442b-108">DESCRIPTION</span></span>
<span data-ttu-id="b442b-109">Rimuove un argomento griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="b442b-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="b442b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b442b-110">EXAMPLES</span></span>

### <span data-ttu-id="b442b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b442b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="b442b-112">Rimuove l'argomento Argomento1 della griglia eventi nel gruppo di \` \` risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="b442b-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b442b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b442b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="b442b-114">Rimuove l'argomento Argomento1 della griglia eventi nel gruppo di \` \` risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="b442b-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b442b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b442b-115">PARAMETERS</span></span>

### <span data-ttu-id="b442b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b442b-116">-DefaultProfile</span></span>
<span data-ttu-id="b442b-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b442b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b442b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b442b-118">-InputObject</span></span>
<span data-ttu-id="b442b-119">Oggetto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="b442b-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b442b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b442b-120">-Name</span></span>
<span data-ttu-id="b442b-121">Nome dell'argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b442b-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b442b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b442b-122">-PassThru</span></span>
<span data-ttu-id="b442b-123">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="b442b-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="b442b-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b442b-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b442b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b442b-125">-ResourceGroupName</span></span>
<span data-ttu-id="b442b-126">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b442b-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b442b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b442b-127">-ResourceId</span></span>
<span data-ttu-id="b442b-128">ResourceID dell'argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b442b-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b442b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b442b-129">-Confirm</span></span>
<span data-ttu-id="b442b-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b442b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b442b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b442b-131">-WhatIf</span></span>
<span data-ttu-id="b442b-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b442b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b442b-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b442b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b442b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b442b-134">CommonParameters</span></span>
<span data-ttu-id="b442b-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b442b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b442b-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b442b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b442b-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="b442b-137">INPUTS</span></span>

### <span data-ttu-id="b442b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b442b-138">System.String</span></span>

### <span data-ttu-id="b442b-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="b442b-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="b442b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b442b-140">OUTPUTS</span></span>

### <span data-ttu-id="b442b-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b442b-141">System.Boolean</span></span>

## <span data-ttu-id="b442b-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="b442b-142">NOTES</span></span>

## <span data-ttu-id="b442b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b442b-143">RELATED LINKS</span></span>
