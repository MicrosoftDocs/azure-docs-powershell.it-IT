---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: aecbc105a87cc058567cb0ff35f0bb0e8cc84c7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688322"
---
# <span data-ttu-id="6ffe1-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="6ffe1-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="6ffe1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ffe1-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffe1-103">Rimuove un argomento della griglia dell'evento Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ffe1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ffe1-104">SYNTAX</span></span>

### <span data-ttu-id="6ffe1-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ffe1-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ffe1-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffe1-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ffe1-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffe1-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ffe1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ffe1-108">DESCRIPTION</span></span>
<span data-ttu-id="6ffe1-109">Rimuove un argomento della griglia dell'evento Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="6ffe1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ffe1-110">EXAMPLES</span></span>

### <span data-ttu-id="6ffe1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ffe1-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="6ffe1-112">Rimuove l'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6ffe1-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6ffe1-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6ffe1-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="6ffe1-114">Rimuove l'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6ffe1-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6ffe1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ffe1-115">PARAMETERS</span></span>

### <span data-ttu-id="6ffe1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ffe1-116">-InputObject</span></span>
<span data-ttu-id="6ffe1-117">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="6ffe1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ffe1-118">-Name</span></span>
<span data-ttu-id="6ffe1-119">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-119">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="6ffe1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ffe1-120">-PassThru</span></span>
<span data-ttu-id="6ffe1-121">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-121">Returns the status of the Remove operation.</span></span> <span data-ttu-id="6ffe1-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6ffe1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffe1-123">-ResourceGroupName</span></span>
<span data-ttu-id="6ffe1-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="6ffe1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ffe1-125">-ResourceId</span></span>
<span data-ttu-id="6ffe1-126">EventGrid argomento ResourceID.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-126">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="6ffe1-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ffe1-127">-Confirm</span></span>
<span data-ttu-id="6ffe1-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ffe1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ffe1-129">-WhatIf</span></span>
<span data-ttu-id="6ffe1-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ffe1-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ffe1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffe1-132">-DefaultProfile</span></span>
<span data-ttu-id="6ffe1-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ffe1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffe1-134">CommonParameters</span></span>
<span data-ttu-id="6ffe1-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ffe1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffe1-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ffe1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffe1-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ffe1-137">INPUTS</span></span>

### <span data-ttu-id="6ffe1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffe1-138">System.String</span></span>
<span data-ttu-id="6ffe1-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="6ffe1-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="6ffe1-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ffe1-140">OUTPUTS</span></span>

### <span data-ttu-id="6ffe1-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="6ffe1-141">System.Object</span></span>

## <span data-ttu-id="6ffe1-142">Note</span><span class="sxs-lookup"><span data-stu-id="6ffe1-142">NOTES</span></span>

## <span data-ttu-id="6ffe1-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ffe1-143">RELATED LINKS</span></span>

