---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473921"
---
# <span data-ttu-id="0d891-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="0d891-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="0d891-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d891-102">SYNOPSIS</span></span>
<span data-ttu-id="0d891-103">Ottiene i tasti di scelta condivisi usati per pubblicare gli eventi in un argomento della griglia degli eventi.</span><span class="sxs-lookup"><span data-stu-id="0d891-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="0d891-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d891-104">SYNTAX</span></span>

### <span data-ttu-id="0d891-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0d891-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d891-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d891-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d891-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d891-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d891-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d891-108">DESCRIPTION</span></span>
<span data-ttu-id="0d891-109">Ottiene i tasti di scelta condivisi usati per pubblicare gli eventi in un argomento della griglia degli eventi.</span><span class="sxs-lookup"><span data-stu-id="0d891-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="0d891-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d891-110">EXAMPLES</span></span>

### <span data-ttu-id="0d891-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d891-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="0d891-112">Ottiene i tasti di scelta condivisi dell'argomento griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0d891-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0d891-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0d891-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="0d891-114">Ottiene i tasti di scelta condivisi dell'argomento griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0d891-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0d891-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d891-115">PARAMETERS</span></span>

### <span data-ttu-id="0d891-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d891-116">-DefaultProfile</span></span>
<span data-ttu-id="0d891-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0d891-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d891-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d891-118">-InputObject</span></span>
<span data-ttu-id="0d891-119">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="0d891-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="0d891-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d891-120">-Name</span></span>
<span data-ttu-id="0d891-121">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="0d891-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="0d891-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d891-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d891-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d891-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="0d891-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d891-124">-ResourceId</span></span>
<span data-ttu-id="0d891-125">Identificatore delle risorse che rappresenta l'argomento della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0d891-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="0d891-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d891-126">CommonParameters</span></span>
<span data-ttu-id="0d891-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d891-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d891-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d891-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d891-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d891-129">INPUTS</span></span>

### <span data-ttu-id="0d891-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0d891-130">System.String</span></span>

### <span data-ttu-id="0d891-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="0d891-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="0d891-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d891-132">OUTPUTS</span></span>

### <span data-ttu-id="0d891-133">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="0d891-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="0d891-134">Note</span><span class="sxs-lookup"><span data-stu-id="0d891-134">NOTES</span></span>

## <span data-ttu-id="0d891-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d891-135">RELATED LINKS</span></span>
