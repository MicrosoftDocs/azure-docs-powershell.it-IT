---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: c6a975ee5071ff3f31ae3daa0e6e9bf6ed9a42ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514355"
---
# <span data-ttu-id="56467-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="56467-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="56467-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56467-102">SYNOPSIS</span></span>
<span data-ttu-id="56467-103">Imposta le proprietà di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="56467-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56467-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56467-104">SYNTAX</span></span>

### <span data-ttu-id="56467-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56467-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56467-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="56467-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56467-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56467-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56467-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56467-108">DESCRIPTION</span></span>
<span data-ttu-id="56467-109">Imposta le proprietà di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="56467-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="56467-110">Questa operazione può essere usata per sostituire i tag di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="56467-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="56467-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56467-111">EXAMPLES</span></span>

### <span data-ttu-id="56467-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56467-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="56467-113">Imposta le proprietà dell'argomento griglia dell'evento \` Topic1 \` nel gruppo \` di risorse MyResourceGroupName \` per sostituire i tag con i tag specificati "reparto" e "ambiente".</span><span class="sxs-lookup"><span data-stu-id="56467-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="56467-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56467-114">PARAMETERS</span></span>

### <span data-ttu-id="56467-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56467-115">-DefaultProfile</span></span>
<span data-ttu-id="56467-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="56467-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56467-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56467-117">-InputObject</span></span>
<span data-ttu-id="56467-118">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="56467-118">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56467-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="56467-119">-Name</span></span>
<span data-ttu-id="56467-120">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="56467-120">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56467-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56467-121">-ResourceGroupName</span></span>
<span data-ttu-id="56467-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56467-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56467-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56467-123">-ResourceId</span></span>
<span data-ttu-id="56467-124">EventGrid argomento ResourceID.</span><span class="sxs-lookup"><span data-stu-id="56467-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="56467-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="56467-125">-Tag</span></span>
<span data-ttu-id="56467-126">Hashtable che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="56467-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56467-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56467-127">-Confirm</span></span>
<span data-ttu-id="56467-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56467-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56467-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56467-129">-WhatIf</span></span>
<span data-ttu-id="56467-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56467-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56467-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56467-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56467-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56467-132">CommonParameters</span></span>
<span data-ttu-id="56467-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56467-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56467-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56467-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56467-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56467-135">INPUTS</span></span>

### <span data-ttu-id="56467-136">System. String</span><span class="sxs-lookup"><span data-stu-id="56467-136">System.String</span></span>
<span data-ttu-id="56467-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="56467-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="56467-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56467-138">OUTPUTS</span></span>

### <span data-ttu-id="56467-139">Microsoft. Azure. Management. EventGrid. Models. Topic</span><span class="sxs-lookup"><span data-stu-id="56467-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="56467-140">Note</span><span class="sxs-lookup"><span data-stu-id="56467-140">NOTES</span></span>

## <span data-ttu-id="56467-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56467-141">RELATED LINKS</span></span>

