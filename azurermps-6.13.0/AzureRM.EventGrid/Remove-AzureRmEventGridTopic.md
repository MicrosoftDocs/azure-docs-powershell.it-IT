---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: d853d5d4659e41c9696ab87c3f9ab8b58c240044
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516624"
---
# <span data-ttu-id="c5d1d-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="c5d1d-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="c5d1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d1d-103">Rimuove un argomento della griglia dell'evento Azure.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5d1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5d1d-104">SYNTAX</span></span>

### <span data-ttu-id="c5d1d-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5d1d-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5d1d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5d1d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5d1d-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5d1d-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5d1d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5d1d-108">DESCRIPTION</span></span>
<span data-ttu-id="c5d1d-109">Rimuove un argomento della griglia dell'evento Azure.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="c5d1d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5d1d-110">EXAMPLES</span></span>

### <span data-ttu-id="c5d1d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5d1d-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="c5d1d-112">Rimuove l'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c5d1d-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c5d1d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c5d1d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="c5d1d-114">Rimuove l'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c5d1d-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c5d1d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5d1d-115">PARAMETERS</span></span>

### <span data-ttu-id="c5d1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d1d-116">-DefaultProfile</span></span>
<span data-ttu-id="c5d1d-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c5d1d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5d1d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5d1d-118">-InputObject</span></span>
<span data-ttu-id="c5d1d-119">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="c5d1d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5d1d-120">-Name</span></span>
<span data-ttu-id="c5d1d-121">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="c5d1d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5d1d-122">-PassThru</span></span>
<span data-ttu-id="c5d1d-123">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="c5d1d-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c5d1d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d1d-125">-ResourceGroupName</span></span>
<span data-ttu-id="c5d1d-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="c5d1d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5d1d-127">-ResourceId</span></span>
<span data-ttu-id="c5d1d-128">EventGrid argomento ResourceID.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="c5d1d-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5d1d-129">-Confirm</span></span>
<span data-ttu-id="c5d1d-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5d1d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5d1d-131">-WhatIf</span></span>
<span data-ttu-id="c5d1d-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5d1d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5d1d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d1d-134">CommonParameters</span></span>
<span data-ttu-id="c5d1d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d1d-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5d1d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d1d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5d1d-137">INPUTS</span></span>

### <span data-ttu-id="c5d1d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c5d1d-138">System.String</span></span>

### <span data-ttu-id="c5d1d-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c5d1d-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="c5d1d-140">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5d1d-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c5d1d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5d1d-141">OUTPUTS</span></span>

### <span data-ttu-id="c5d1d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5d1d-142">System.Boolean</span></span>

## <span data-ttu-id="c5d1d-143">Note</span><span class="sxs-lookup"><span data-stu-id="c5d1d-143">NOTES</span></span>

## <span data-ttu-id="c5d1d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5d1d-144">RELATED LINKS</span></span>
