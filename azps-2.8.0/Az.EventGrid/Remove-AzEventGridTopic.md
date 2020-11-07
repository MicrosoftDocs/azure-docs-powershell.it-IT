---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: 3cc0d587713bf287d9cc3bfa720d867e81370a8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674468"
---
# <span data-ttu-id="3eb9f-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="3eb9f-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="3eb9f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3eb9f-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb9f-103">Rimuove un argomento della griglia dell'evento Azure.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="3eb9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3eb9f-104">SYNTAX</span></span>

### <span data-ttu-id="3eb9f-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3eb9f-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb9f-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eb9f-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb9f-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eb9f-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb9f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3eb9f-108">DESCRIPTION</span></span>
<span data-ttu-id="3eb9f-109">Rimuove un argomento della griglia dell'evento Azure.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="3eb9f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3eb9f-110">EXAMPLES</span></span>

### <span data-ttu-id="3eb9f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3eb9f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="3eb9f-112">Rimuove l'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="3eb9f-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3eb9f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3eb9f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="3eb9f-114">Rimuove l'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="3eb9f-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3eb9f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3eb9f-115">PARAMETERS</span></span>

### <span data-ttu-id="3eb9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb9f-116">-DefaultProfile</span></span>
<span data-ttu-id="3eb9f-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3eb9f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3eb9f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eb9f-118">-InputObject</span></span>
<span data-ttu-id="3eb9f-119">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="3eb9f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3eb9f-120">-Name</span></span>
<span data-ttu-id="3eb9f-121">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="3eb9f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3eb9f-122">-PassThru</span></span>
<span data-ttu-id="3eb9f-123">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="3eb9f-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3eb9f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb9f-125">-ResourceGroupName</span></span>
<span data-ttu-id="3eb9f-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="3eb9f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3eb9f-127">-ResourceId</span></span>
<span data-ttu-id="3eb9f-128">EventGrid argomento ResourceID.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="3eb9f-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3eb9f-129">-Confirm</span></span>
<span data-ttu-id="3eb9f-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb9f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb9f-131">-WhatIf</span></span>
<span data-ttu-id="3eb9f-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eb9f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb9f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb9f-134">CommonParameters</span></span>
<span data-ttu-id="3eb9f-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb9f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb9f-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb9f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb9f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3eb9f-137">INPUTS</span></span>

### <span data-ttu-id="3eb9f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3eb9f-138">System.String</span></span>

### <span data-ttu-id="3eb9f-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="3eb9f-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="3eb9f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3eb9f-140">OUTPUTS</span></span>

### <span data-ttu-id="3eb9f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3eb9f-141">System.Boolean</span></span>

## <span data-ttu-id="3eb9f-142">Note</span><span class="sxs-lookup"><span data-stu-id="3eb9f-142">NOTES</span></span>

## <span data-ttu-id="3eb9f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3eb9f-143">RELATED LINKS</span></span>
