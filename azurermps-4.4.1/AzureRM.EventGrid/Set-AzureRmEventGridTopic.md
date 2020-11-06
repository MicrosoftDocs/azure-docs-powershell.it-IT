---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 509f10432139ca0f2d9aaca216f22d998b7963a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521681"
---
# <span data-ttu-id="dde24-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="dde24-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="dde24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dde24-102">SYNOPSIS</span></span>
<span data-ttu-id="dde24-103">Impostare le proprietà di un argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="dde24-103">Set the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dde24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dde24-104">SYNTAX</span></span>

### <span data-ttu-id="dde24-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dde24-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dde24-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="dde24-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dde24-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dde24-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dde24-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dde24-108">DESCRIPTION</span></span>
<span data-ttu-id="dde24-109">Impostare le proprietà di un argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="dde24-109">Set the properties of an Event Grid topic.</span></span> <span data-ttu-id="dde24-110">Questa operazione può essere usata per sostituire i tag di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="dde24-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="dde24-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dde24-111">EXAMPLES</span></span>

### <span data-ttu-id="dde24-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dde24-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="dde24-113">Imposta le proprietà dell'argomento griglia dell'evento \` Topic1 \` nel gruppo \` di risorse MyResourceGroupName \` per sostituire i tag con i tag specificati "reparto" e "ambiente".</span><span class="sxs-lookup"><span data-stu-id="dde24-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="dde24-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dde24-114">PARAMETERS</span></span>

### <span data-ttu-id="dde24-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dde24-115">-InputObject</span></span>
<span data-ttu-id="dde24-116">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="dde24-116">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="dde24-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="dde24-117">-Name</span></span>
<span data-ttu-id="dde24-118">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="dde24-118">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="dde24-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde24-119">-ResourceGroupName</span></span>
<span data-ttu-id="dde24-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dde24-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="dde24-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dde24-121">-ResourceId</span></span>
<span data-ttu-id="dde24-122">EventGrid argomento ResourceID.</span><span class="sxs-lookup"><span data-stu-id="dde24-122">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="dde24-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="dde24-123">-Tag</span></span>
<span data-ttu-id="dde24-124">Hashtable che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="dde24-124">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="dde24-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dde24-125">-Confirm</span></span>
<span data-ttu-id="dde24-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dde24-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dde24-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dde24-127">-WhatIf</span></span>
<span data-ttu-id="dde24-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dde24-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dde24-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dde24-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dde24-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde24-130">-DefaultProfile</span></span>
<span data-ttu-id="dde24-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dde24-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dde24-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde24-132">CommonParameters</span></span>
<span data-ttu-id="dde24-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde24-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde24-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dde24-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde24-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dde24-135">INPUTS</span></span>

### <span data-ttu-id="dde24-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dde24-136">System.String</span></span>
<span data-ttu-id="dde24-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dde24-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dde24-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dde24-138">OUTPUTS</span></span>

### <span data-ttu-id="dde24-139">Microsoft. Azure. Management. EventGrid. Models. Topic</span><span class="sxs-lookup"><span data-stu-id="dde24-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="dde24-140">Note</span><span class="sxs-lookup"><span data-stu-id="dde24-140">NOTES</span></span>

## <span data-ttu-id="dde24-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dde24-141">RELATED LINKS</span></span>

