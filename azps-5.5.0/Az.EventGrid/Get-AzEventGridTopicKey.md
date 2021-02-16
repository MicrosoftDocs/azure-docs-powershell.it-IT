---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194423"
---
# <span data-ttu-id="0ed8f-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="0ed8f-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="0ed8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ed8f-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed8f-103">Ottiene le chiavi di accesso condivise usate per pubblicare eventi in un argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="0ed8f-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="0ed8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ed8f-104">SYNTAX</span></span>

### <span data-ttu-id="0ed8f-105">TopicNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0ed8f-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ed8f-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ed8f-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ed8f-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ed8f-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ed8f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0ed8f-108">DESCRIPTION</span></span>
<span data-ttu-id="0ed8f-109">Ottiene le chiavi di accesso condivise usate per pubblicare eventi in un argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="0ed8f-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="0ed8f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ed8f-110">EXAMPLES</span></span>

### <span data-ttu-id="0ed8f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0ed8f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="0ed8f-112">Ottiene le chiavi di accesso condivise dell'argomento Griglia eventi \` Argomento1 \` nel gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="0ed8f-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0ed8f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0ed8f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="0ed8f-114">Ottiene le chiavi di accesso condivise dell'argomento Griglia eventi \` Argomento1 \` nel gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="0ed8f-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0ed8f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ed8f-115">PARAMETERS</span></span>

### <span data-ttu-id="0ed8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed8f-116">-DefaultProfile</span></span>
<span data-ttu-id="0ed8f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0ed8f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ed8f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ed8f-118">-InputObject</span></span>
<span data-ttu-id="0ed8f-119">Oggetto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="0ed8f-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="0ed8f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0ed8f-120">-Name</span></span>
<span data-ttu-id="0ed8f-121">Nome dell'argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="0ed8f-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="0ed8f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed8f-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ed8f-123">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ed8f-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="0ed8f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ed8f-124">-ResourceId</span></span>
<span data-ttu-id="0ed8f-125">Identificatore di risorsa che rappresenta l'argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="0ed8f-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="0ed8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed8f-126">CommonParameters</span></span>
<span data-ttu-id="0ed8f-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ed8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed8f-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0ed8f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed8f-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="0ed8f-129">INPUTS</span></span>

### <span data-ttu-id="0ed8f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0ed8f-130">System.String</span></span>

### <span data-ttu-id="0ed8f-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="0ed8f-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="0ed8f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ed8f-132">OUTPUTS</span></span>

### <span data-ttu-id="0ed8f-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="0ed8f-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="0ed8f-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="0ed8f-134">NOTES</span></span>

## <span data-ttu-id="0ed8f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ed8f-135">RELATED LINKS</span></span>
