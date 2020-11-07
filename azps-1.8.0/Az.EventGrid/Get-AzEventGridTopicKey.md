---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: 3454a3aad2276384588c0ccc550a1b0ef6df7cfc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678835"
---
# <span data-ttu-id="78c99-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="78c99-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="78c99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78c99-102">SYNOPSIS</span></span>
<span data-ttu-id="78c99-103">Ottiene i tasti di scelta condivisi usati per pubblicare gli eventi in un argomento della griglia degli eventi.</span><span class="sxs-lookup"><span data-stu-id="78c99-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="78c99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78c99-104">SYNTAX</span></span>

### <span data-ttu-id="78c99-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78c99-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78c99-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78c99-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78c99-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="78c99-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78c99-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78c99-108">DESCRIPTION</span></span>
<span data-ttu-id="78c99-109">Ottiene i tasti di scelta condivisi usati per pubblicare gli eventi in un argomento della griglia degli eventi.</span><span class="sxs-lookup"><span data-stu-id="78c99-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="78c99-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78c99-110">EXAMPLES</span></span>

### <span data-ttu-id="78c99-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="78c99-111">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="78c99-112">Ottiene i tasti di scelta condivisi dell'argomento griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="78c99-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="78c99-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="78c99-113">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="78c99-114">Ottiene i tasti di scelta condivisi dell'argomento griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="78c99-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="78c99-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78c99-115">PARAMETERS</span></span>

### <span data-ttu-id="78c99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c99-116">-DefaultProfile</span></span>
<span data-ttu-id="78c99-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="78c99-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78c99-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78c99-118">-InputObject</span></span>
<span data-ttu-id="78c99-119">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="78c99-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="78c99-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="78c99-120">-Name</span></span>
<span data-ttu-id="78c99-121">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="78c99-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="78c99-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78c99-122">-ResourceGroupName</span></span>
<span data-ttu-id="78c99-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="78c99-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="78c99-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78c99-124">-ResourceId</span></span>
<span data-ttu-id="78c99-125">Identificatore delle risorse che rappresenta l'argomento della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="78c99-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="78c99-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c99-126">CommonParameters</span></span>
<span data-ttu-id="78c99-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78c99-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c99-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c99-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c99-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78c99-129">INPUTS</span></span>

### <span data-ttu-id="78c99-130">System. String</span><span class="sxs-lookup"><span data-stu-id="78c99-130">System.String</span></span>

### <span data-ttu-id="78c99-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="78c99-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="78c99-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78c99-132">OUTPUTS</span></span>

### <span data-ttu-id="78c99-133">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="78c99-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="78c99-134">Note</span><span class="sxs-lookup"><span data-stu-id="78c99-134">NOTES</span></span>

## <span data-ttu-id="78c99-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78c99-135">RELATED LINKS</span></span>
