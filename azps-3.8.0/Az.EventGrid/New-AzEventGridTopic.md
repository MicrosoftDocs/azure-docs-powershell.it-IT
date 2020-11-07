---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 21bad7c36b39acbfbcc438603a57f504aaa1a106
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865212"
---
# <span data-ttu-id="8ba3e-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="8ba3e-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="8ba3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ba3e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba3e-103">Crea un nuovo argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba3e-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="8ba3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ba3e-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ba3e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ba3e-105">DESCRIPTION</span></span>
<span data-ttu-id="8ba3e-106">Crea un nuovo argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba3e-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="8ba3e-107">Dopo aver creato l'argomento, un'applicazione può pubblicare gli eventi nell'endpoint dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="8ba3e-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="8ba3e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ba3e-108">EXAMPLES</span></span>

### <span data-ttu-id="8ba3e-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8ba3e-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="8ba3e-110">Crea un argomento della griglia dell'evento \` Topic1 \` nella posizione geografica specificata \` westus2 \` , nel gruppo risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8ba3e-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8ba3e-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8ba3e-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="8ba3e-112">Crea un argomento della griglia dell'evento \` Topic1 \` nella posizione geografica specificata \` westus2 \` , nel gruppo di risorse \` MyResourceGroupName \` con i tag specificati "reparto" e "ambiente".</span><span class="sxs-lookup"><span data-stu-id="8ba3e-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="8ba3e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ba3e-113">PARAMETERS</span></span>

### <span data-ttu-id="8ba3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba3e-114">-DefaultProfile</span></span>
<span data-ttu-id="8ba3e-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8ba3e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ba3e-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8ba3e-116">-Location</span></span>
<span data-ttu-id="8ba3e-117">Posizione dell'argomento</span><span class="sxs-lookup"><span data-stu-id="8ba3e-117">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba3e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ba3e-118">-Name</span></span>
<span data-ttu-id="8ba3e-119">Nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="8ba3e-119">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba3e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba3e-120">-ResourceGroupName</span></span>
<span data-ttu-id="8ba3e-121">Gruppo di risorse in cui deve essere creato l'argomento.</span><span class="sxs-lookup"><span data-stu-id="8ba3e-121">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba3e-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="8ba3e-122">-Tag</span></span>
<span data-ttu-id="8ba3e-123">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8ba3e-123">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba3e-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ba3e-124">-Confirm</span></span>
<span data-ttu-id="8ba3e-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ba3e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba3e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba3e-126">-WhatIf</span></span>
<span data-ttu-id="8ba3e-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ba3e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ba3e-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ba3e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba3e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba3e-129">CommonParameters</span></span>
<span data-ttu-id="8ba3e-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba3e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba3e-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba3e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba3e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ba3e-132">INPUTS</span></span>

### <span data-ttu-id="8ba3e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8ba3e-133">System.String</span></span>

### <span data-ttu-id="8ba3e-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8ba3e-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8ba3e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ba3e-135">OUTPUTS</span></span>

### <span data-ttu-id="8ba3e-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="8ba3e-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="8ba3e-137">Note</span><span class="sxs-lookup"><span data-stu-id="8ba3e-137">NOTES</span></span>

## <span data-ttu-id="8ba3e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ba3e-138">RELATED LINKS</span></span>
