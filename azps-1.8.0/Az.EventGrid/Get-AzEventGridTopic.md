---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 23004583a08dbcf5ef8785b62d0457b6b6ee0897
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678836"
---
# <span data-ttu-id="92227-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="92227-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="92227-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92227-102">SYNOPSIS</span></span>
<span data-ttu-id="92227-103">Ottiene i dettagli di un argomento della griglia di eventi o ottiene un elenco di tutti gli argomenti della griglia degli eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="92227-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="92227-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92227-104">SYNTAX</span></span>

### <span data-ttu-id="92227-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92227-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92227-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="92227-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92227-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="92227-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92227-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92227-108">DESCRIPTION</span></span>
<span data-ttu-id="92227-109">Il cmdlet Get-AzEventGridTopic ottiene i dettagli di un argomento della griglia di eventi specificato o un elenco di tutti gli argomenti della griglia eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="92227-109">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="92227-110">Se viene fornito il nome dell'argomento, vengono restituiti i dettagli di un singolo argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="92227-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="92227-111">Se il nome dell'argomento non è disponibile, viene restituito un elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="92227-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="92227-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92227-112">EXAMPLES</span></span>

### <span data-ttu-id="92227-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="92227-113">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="92227-114">Ottiene i dettagli dell'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="92227-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="92227-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="92227-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="92227-116">Ottiene i dettagli dell'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="92227-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="92227-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="92227-117">Example 3</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="92227-118">Elenca tutti gli argomenti della griglia degli eventi nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="92227-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="92227-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="92227-119">Example 4</span></span>
```
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="92227-120">Elencare tutti gli argomenti della griglia degli eventi nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="92227-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="92227-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92227-121">PARAMETERS</span></span>

### <span data-ttu-id="92227-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92227-122">-DefaultProfile</span></span>
<span data-ttu-id="92227-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="92227-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92227-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="92227-124">-Name</span></span>
<span data-ttu-id="92227-125">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="92227-125">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="92227-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92227-126">-ResourceGroupName</span></span>
<span data-ttu-id="92227-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="92227-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="92227-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92227-128">-ResourceId</span></span>
<span data-ttu-id="92227-129">Identificatore delle risorse che rappresenta l'argomento della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="92227-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="92227-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92227-130">CommonParameters</span></span>
<span data-ttu-id="92227-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92227-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92227-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92227-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92227-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92227-133">INPUTS</span></span>

### <span data-ttu-id="92227-134">System. String</span><span class="sxs-lookup"><span data-stu-id="92227-134">System.String</span></span>

## <span data-ttu-id="92227-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92227-135">OUTPUTS</span></span>

### <span data-ttu-id="92227-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="92227-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="92227-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="92227-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="92227-138">Note</span><span class="sxs-lookup"><span data-stu-id="92227-138">NOTES</span></span>

## <span data-ttu-id="92227-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92227-139">RELATED LINKS</span></span>
