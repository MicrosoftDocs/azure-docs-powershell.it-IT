---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 8ea4fc7674af247ffded2c6c4317f07a831adf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520096"
---
# <span data-ttu-id="430dd-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="430dd-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="430dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="430dd-102">SYNOPSIS</span></span>
<span data-ttu-id="430dd-103">Ottiene i dettagli di un argomento della griglia di eventi o ottiene un elenco di tutti gli argomenti della griglia degli eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="430dd-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="430dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="430dd-104">SYNTAX</span></span>

### <span data-ttu-id="430dd-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="430dd-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="430dd-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="430dd-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="430dd-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="430dd-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="430dd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="430dd-108">DESCRIPTION</span></span>
<span data-ttu-id="430dd-109">Il cmdlet Get-AzureRmEventGridTopic ottiene i dettagli di un argomento della griglia di eventi specificato o un elenco di tutti gli argomenti della griglia eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="430dd-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="430dd-110">Se viene fornito il nome dell'argomento, vengono restituiti i dettagli di un singolo argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="430dd-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="430dd-111">Se il nome dell'argomento non è disponibile, viene restituito un elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="430dd-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="430dd-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="430dd-112">EXAMPLES</span></span>

### <span data-ttu-id="430dd-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="430dd-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="430dd-114">Ottiene i dettagli dell'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="430dd-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="430dd-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="430dd-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="430dd-116">Ottiene i dettagli dell'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="430dd-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="430dd-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="430dd-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="430dd-118">Elenca tutti gli argomenti della griglia degli eventi nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="430dd-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="430dd-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="430dd-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="430dd-120">Elencare tutti gli argomenti della griglia degli eventi nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="430dd-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="430dd-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="430dd-121">PARAMETERS</span></span>

### <span data-ttu-id="430dd-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="430dd-122">-Name</span></span>
<span data-ttu-id="430dd-123">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="430dd-123">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="430dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="430dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="430dd-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="430dd-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="430dd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="430dd-126">-ResourceId</span></span>
<span data-ttu-id="430dd-127">Identificatore delle risorse che rappresenta l'argomento della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="430dd-127">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="430dd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="430dd-128">-DefaultProfile</span></span>
<span data-ttu-id="430dd-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="430dd-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="430dd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="430dd-130">CommonParameters</span></span>
<span data-ttu-id="430dd-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="430dd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="430dd-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="430dd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="430dd-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="430dd-133">INPUTS</span></span>

### <span data-ttu-id="430dd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="430dd-134">System.String</span></span>
<span data-ttu-id="430dd-135">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="430dd-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="430dd-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="430dd-136">OUTPUTS</span></span>

### <span data-ttu-id="430dd-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="430dd-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="430dd-138">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="430dd-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="430dd-139">Note</span><span class="sxs-lookup"><span data-stu-id="430dd-139">NOTES</span></span>

## <span data-ttu-id="430dd-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="430dd-140">RELATED LINKS</span></span>

