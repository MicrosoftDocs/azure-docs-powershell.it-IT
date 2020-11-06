---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
ms.openlocfilehash: fdd15de19f921781e89d7e24b57e1d82632e4735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521688"
---
# <span data-ttu-id="fe276-101">New-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="fe276-101">New-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="fe276-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe276-102">SYNOPSIS</span></span>
<span data-ttu-id="fe276-103">Crea un nuovo argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="fe276-103">Creates a new Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe276-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe276-104">SYNTAX</span></span>

```
New-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe276-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe276-105">DESCRIPTION</span></span>
<span data-ttu-id="fe276-106">Crea un nuovo argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="fe276-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="fe276-107">Dopo aver creato l'argomento, un'applicazione può pubblicare gli eventi nell'endpoint dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="fe276-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="fe276-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe276-108">EXAMPLES</span></span>

### <span data-ttu-id="fe276-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fe276-109">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="fe276-110">Crea un argomento della griglia dell'evento \` Topic1 \` nella posizione geografica specificata \` westus2 \` , nel gruppo risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="fe276-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="fe276-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fe276-111">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="fe276-112">Crea un argomento della griglia dell'evento \` Topic1 \` nella posizione geografica specificata \` westus2 \` , nel gruppo di risorse \` MyResourceGroupName \` con i tag specificati "reparto" e "ambiente".</span><span class="sxs-lookup"><span data-stu-id="fe276-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="fe276-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe276-113">PARAMETERS</span></span>

### <span data-ttu-id="fe276-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fe276-114">-Location</span></span>
<span data-ttu-id="fe276-115">Posizione dell'argomento</span><span class="sxs-lookup"><span data-stu-id="fe276-115">The location of the topic</span></span>

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

### <span data-ttu-id="fe276-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe276-116">-Name</span></span>
<span data-ttu-id="fe276-117">Nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="fe276-117">The name of the topic.</span></span>

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

### <span data-ttu-id="fe276-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe276-118">-ResourceGroupName</span></span>
<span data-ttu-id="fe276-119">Gruppo di risorse in cui deve essere creato l'argomento.</span><span class="sxs-lookup"><span data-stu-id="fe276-119">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="fe276-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe276-120">-Tag</span></span>
<span data-ttu-id="fe276-121">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fe276-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="fe276-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe276-122">-Confirm</span></span>
<span data-ttu-id="fe276-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe276-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe276-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe276-124">-WhatIf</span></span>
<span data-ttu-id="fe276-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe276-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe276-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe276-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe276-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe276-127">-DefaultProfile</span></span>
<span data-ttu-id="fe276-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe276-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe276-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe276-129">CommonParameters</span></span>
<span data-ttu-id="fe276-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe276-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe276-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe276-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe276-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe276-132">INPUTS</span></span>

### <span data-ttu-id="fe276-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fe276-133">System.String</span></span>
<span data-ttu-id="fe276-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fe276-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fe276-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe276-135">OUTPUTS</span></span>

### <span data-ttu-id="fe276-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="fe276-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="fe276-137">Note</span><span class="sxs-lookup"><span data-stu-id="fe276-137">NOTES</span></span>

## <span data-ttu-id="fe276-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe276-138">RELATED LINKS</span></span>

