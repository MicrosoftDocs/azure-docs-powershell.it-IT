---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: bd60a5c57f72fd6fd5eae9dffbbdb7bea0752343
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188478"
---
# <span data-ttu-id="b5168-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="b5168-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="b5168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5168-102">SYNOPSIS</span></span>
<span data-ttu-id="b5168-103">Rimuove un argomento griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5168-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="b5168-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5168-104">SYNTAX</span></span>

### <span data-ttu-id="b5168-105">TopicNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5168-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5168-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5168-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5168-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5168-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5168-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5168-108">DESCRIPTION</span></span>
<span data-ttu-id="b5168-109">Rimuove un argomento griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5168-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="b5168-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5168-110">EXAMPLES</span></span>

### <span data-ttu-id="b5168-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5168-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="b5168-112">Rimuove l'argomento Argomento1 della griglia eventi nel gruppo di \` \` risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="b5168-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b5168-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b5168-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="b5168-114">Rimuove l'argomento Argomento1 della griglia eventi nel gruppo di \` \` risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="b5168-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b5168-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5168-115">PARAMETERS</span></span>

### <span data-ttu-id="b5168-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5168-116">-DefaultProfile</span></span>
<span data-ttu-id="b5168-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b5168-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5168-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5168-118">-InputObject</span></span>
<span data-ttu-id="b5168-119">Oggetto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="b5168-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="b5168-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b5168-120">-Name</span></span>
<span data-ttu-id="b5168-121">Nome dell'argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b5168-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="b5168-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5168-122">-PassThru</span></span>
<span data-ttu-id="b5168-123">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="b5168-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="b5168-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b5168-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b5168-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5168-125">-ResourceGroupName</span></span>
<span data-ttu-id="b5168-126">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5168-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="b5168-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5168-127">-ResourceId</span></span>
<span data-ttu-id="b5168-128">ResourceID dell'argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b5168-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="b5168-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5168-129">-Confirm</span></span>
<span data-ttu-id="b5168-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5168-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5168-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5168-131">-WhatIf</span></span>
<span data-ttu-id="b5168-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5168-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5168-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5168-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5168-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5168-134">CommonParameters</span></span>
<span data-ttu-id="b5168-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5168-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5168-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5168-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5168-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5168-137">INPUTS</span></span>

### <span data-ttu-id="b5168-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b5168-138">System.String</span></span>

### <span data-ttu-id="b5168-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="b5168-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="b5168-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5168-140">OUTPUTS</span></span>

### <span data-ttu-id="b5168-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5168-141">System.Boolean</span></span>

## <span data-ttu-id="b5168-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5168-142">NOTES</span></span>

## <span data-ttu-id="b5168-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5168-143">RELATED LINKS</span></span>
