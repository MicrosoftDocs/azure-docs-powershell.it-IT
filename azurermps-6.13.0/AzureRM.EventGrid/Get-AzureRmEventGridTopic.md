---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 2d18e923e14caf4c0048575465e9f52fb14596f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509231"
---
# <span data-ttu-id="8dd0e-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="8dd0e-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="8dd0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8dd0e-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd0e-103">Ottiene i dettagli di un argomento della griglia di eventi o ottiene un elenco di tutti gli argomenti della griglia degli eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dd0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dd0e-104">SYNTAX</span></span>

### <span data-ttu-id="8dd0e-105">ResourceGroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8dd0e-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8dd0e-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dd0e-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd0e-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dd0e-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8dd0e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dd0e-108">DESCRIPTION</span></span>
<span data-ttu-id="8dd0e-109">Il cmdlet Get-AzureRmEventGridTopic ottiene i dettagli di un argomento della griglia di eventi specificato o un elenco di tutti gli argomenti della griglia eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="8dd0e-110">Se viene fornito il nome dell'argomento, vengono restituiti i dettagli di un singolo argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="8dd0e-111">Se il nome dell'argomento non è disponibile, viene restituito un elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="8dd0e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dd0e-112">EXAMPLES</span></span>

### <span data-ttu-id="8dd0e-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8dd0e-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="8dd0e-114">Ottiene i dettagli dell'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8dd0e-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8dd0e-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8dd0e-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="8dd0e-116">Ottiene i dettagli dell'argomento della griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8dd0e-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8dd0e-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8dd0e-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="8dd0e-118">Elenca tutti gli argomenti della griglia degli eventi nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8dd0e-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8dd0e-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="8dd0e-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="8dd0e-120">Elencare tutti gli argomenti della griglia degli eventi nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="8dd0e-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8dd0e-121">PARAMETERS</span></span>

### <span data-ttu-id="8dd0e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd0e-122">-DefaultProfile</span></span>
<span data-ttu-id="8dd0e-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8dd0e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dd0e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8dd0e-124">-Name</span></span>
<span data-ttu-id="8dd0e-125">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-125">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="8dd0e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd0e-126">-ResourceGroupName</span></span>
<span data-ttu-id="8dd0e-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="8dd0e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dd0e-128">-ResourceId</span></span>
<span data-ttu-id="8dd0e-129">Identificatore delle risorse che rappresenta l'argomento della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="8dd0e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd0e-130">CommonParameters</span></span>
<span data-ttu-id="8dd0e-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd0e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd0e-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd0e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd0e-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8dd0e-133">INPUTS</span></span>

### <span data-ttu-id="8dd0e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8dd0e-134">System.String</span></span>

## <span data-ttu-id="8dd0e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dd0e-135">OUTPUTS</span></span>

### <span data-ttu-id="8dd0e-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="8dd0e-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="8dd0e-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="8dd0e-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="8dd0e-138">Note</span><span class="sxs-lookup"><span data-stu-id="8dd0e-138">NOTES</span></span>

## <span data-ttu-id="8dd0e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dd0e-139">RELATED LINKS</span></span>
