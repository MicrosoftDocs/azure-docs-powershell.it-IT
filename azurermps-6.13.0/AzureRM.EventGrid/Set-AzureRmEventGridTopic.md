---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 384c05e6424ab7b8d4fbb01a0c4822b73702c419
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516623"
---
# <span data-ttu-id="4946e-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="4946e-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="4946e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4946e-102">SYNOPSIS</span></span>
<span data-ttu-id="4946e-103">Imposta le proprietà di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="4946e-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4946e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4946e-104">SYNTAX</span></span>

### <span data-ttu-id="4946e-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4946e-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4946e-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4946e-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4946e-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4946e-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4946e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4946e-108">DESCRIPTION</span></span>
<span data-ttu-id="4946e-109">Imposta le proprietà di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="4946e-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="4946e-110">Questa operazione può essere usata per sostituire i tag di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="4946e-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="4946e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4946e-111">EXAMPLES</span></span>

### <span data-ttu-id="4946e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4946e-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="4946e-113">Imposta le proprietà dell'argomento griglia dell'evento \` Topic1 \` nel gruppo \` di risorse MyResourceGroupName \` per sostituire i tag con i tag specificati "reparto" e "ambiente".</span><span class="sxs-lookup"><span data-stu-id="4946e-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="4946e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4946e-114">PARAMETERS</span></span>

### <span data-ttu-id="4946e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4946e-115">-DefaultProfile</span></span>
<span data-ttu-id="4946e-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4946e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4946e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4946e-117">-InputObject</span></span>
<span data-ttu-id="4946e-118">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="4946e-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="4946e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4946e-119">-Name</span></span>
<span data-ttu-id="4946e-120">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="4946e-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="4946e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4946e-121">-ResourceGroupName</span></span>
<span data-ttu-id="4946e-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4946e-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="4946e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4946e-123">-ResourceId</span></span>
<span data-ttu-id="4946e-124">EventGrid argomento ResourceID.</span><span class="sxs-lookup"><span data-stu-id="4946e-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="4946e-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4946e-125">-Tag</span></span>
<span data-ttu-id="4946e-126">Hashtable che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="4946e-126">Hashtables which represents resource Tag.</span></span>

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

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4946e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4946e-127">-Confirm</span></span>
<span data-ttu-id="4946e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4946e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4946e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4946e-129">-WhatIf</span></span>
<span data-ttu-id="4946e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4946e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4946e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4946e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4946e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4946e-132">CommonParameters</span></span>
<span data-ttu-id="4946e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4946e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4946e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4946e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4946e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4946e-135">INPUTS</span></span>

### <span data-ttu-id="4946e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4946e-136">System.String</span></span>

### <span data-ttu-id="4946e-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="4946e-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="4946e-138">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4946e-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4946e-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4946e-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4946e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4946e-140">OUTPUTS</span></span>

### <span data-ttu-id="4946e-141">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="4946e-141">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="4946e-142">Note</span><span class="sxs-lookup"><span data-stu-id="4946e-142">NOTES</span></span>

## <span data-ttu-id="4946e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4946e-143">RELATED LINKS</span></span>
