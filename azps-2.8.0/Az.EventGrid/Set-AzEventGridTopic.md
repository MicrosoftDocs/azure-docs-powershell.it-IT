---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: f27533a36314ae2b31cd0055e8cc17027c95016a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674465"
---
# <span data-ttu-id="047e5-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="047e5-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="047e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="047e5-102">SYNOPSIS</span></span>
<span data-ttu-id="047e5-103">Imposta le proprietà di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="047e5-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="047e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="047e5-104">SYNTAX</span></span>

### <span data-ttu-id="047e5-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="047e5-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="047e5-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="047e5-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="047e5-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="047e5-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="047e5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="047e5-108">DESCRIPTION</span></span>
<span data-ttu-id="047e5-109">Imposta le proprietà di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="047e5-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="047e5-110">Questa operazione può essere usata per sostituire i tag di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="047e5-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="047e5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="047e5-111">EXAMPLES</span></span>

### <span data-ttu-id="047e5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="047e5-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="047e5-113">Imposta le proprietà dell'argomento griglia dell'evento \` Topic1 \` nel gruppo \` di risorse MyResourceGroupName \` per sostituire i tag con i tag specificati "reparto" e "ambiente".</span><span class="sxs-lookup"><span data-stu-id="047e5-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="047e5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="047e5-114">PARAMETERS</span></span>

### <span data-ttu-id="047e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="047e5-115">-DefaultProfile</span></span>
<span data-ttu-id="047e5-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="047e5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="047e5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="047e5-117">-InputObject</span></span>
<span data-ttu-id="047e5-118">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="047e5-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="047e5-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="047e5-119">-Name</span></span>
<span data-ttu-id="047e5-120">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="047e5-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="047e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="047e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="047e5-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="047e5-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="047e5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="047e5-123">-ResourceId</span></span>
<span data-ttu-id="047e5-124">EventGrid argomento ResourceID.</span><span class="sxs-lookup"><span data-stu-id="047e5-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="047e5-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="047e5-125">-Tag</span></span>
<span data-ttu-id="047e5-126">Hashtable che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="047e5-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047e5-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="047e5-127">-Confirm</span></span>
<span data-ttu-id="047e5-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="047e5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="047e5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="047e5-129">-WhatIf</span></span>
<span data-ttu-id="047e5-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="047e5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="047e5-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="047e5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="047e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047e5-132">CommonParameters</span></span>
<span data-ttu-id="047e5-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="047e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047e5-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="047e5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047e5-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="047e5-135">INPUTS</span></span>

### <span data-ttu-id="047e5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="047e5-136">System.String</span></span>

### <span data-ttu-id="047e5-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="047e5-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="047e5-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="047e5-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="047e5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="047e5-139">OUTPUTS</span></span>

### <span data-ttu-id="047e5-140">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="047e5-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="047e5-141">Note</span><span class="sxs-lookup"><span data-stu-id="047e5-141">NOTES</span></span>

## <span data-ttu-id="047e5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="047e5-142">RELATED LINKS</span></span>
