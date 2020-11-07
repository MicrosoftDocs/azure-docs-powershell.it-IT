---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: 3163ba513dea00a052f7042d7575f107421c0a6b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674477"
---
# <span data-ttu-id="a4001-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="a4001-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="a4001-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4001-102">SYNOPSIS</span></span>
<span data-ttu-id="a4001-103">Rigenera la chiave di accesso condivisa per un argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4001-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="a4001-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4001-104">SYNTAX</span></span>

### <span data-ttu-id="a4001-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4001-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4001-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4001-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4001-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4001-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4001-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4001-108">DESCRIPTION</span></span>
<span data-ttu-id="a4001-109">Rigenera la chiave di accesso condivisa per un argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4001-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="a4001-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4001-110">EXAMPLES</span></span>

### <span data-ttu-id="a4001-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4001-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="a4001-112">Rigenerare la chiave corrispondente alla chiave \' Key1' \ of Event Grid topic \` Topic1 \` nel gruppo di \` risorse MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a4001-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a4001-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a4001-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="a4001-114">Rigenerare la chiave corrispondente alla chiave \' Key1' \ of Event Grid topic \` Topic1 \` nel gruppo di \` risorse MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a4001-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a4001-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4001-115">PARAMETERS</span></span>

### <span data-ttu-id="a4001-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4001-116">-DefaultProfile</span></span>
<span data-ttu-id="a4001-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a4001-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4001-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4001-118">-InputObject</span></span>
<span data-ttu-id="a4001-119">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a4001-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a4001-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="a4001-120">-KeyName</span></span>
<span data-ttu-id="a4001-121">Nome della chiave che deve essere rigenerata</span><span class="sxs-lookup"><span data-stu-id="a4001-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="a4001-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4001-122">-ResourceGroupName</span></span>
<span data-ttu-id="a4001-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4001-123">Resource group name.</span></span>

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

### <span data-ttu-id="a4001-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4001-124">-ResourceId</span></span>
<span data-ttu-id="a4001-125">Identificatore delle risorse che rappresenta l'argomento della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a4001-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="a4001-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a4001-126">-TopicName</span></span>
<span data-ttu-id="a4001-127">Nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="a4001-127">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4001-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4001-128">-Confirm</span></span>
<span data-ttu-id="a4001-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4001-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4001-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4001-130">-WhatIf</span></span>
<span data-ttu-id="a4001-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4001-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4001-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4001-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4001-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4001-133">CommonParameters</span></span>
<span data-ttu-id="a4001-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4001-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4001-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4001-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4001-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4001-136">INPUTS</span></span>

### <span data-ttu-id="a4001-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a4001-137">System.String</span></span>

### <span data-ttu-id="a4001-138">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a4001-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a4001-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4001-139">OUTPUTS</span></span>

### <span data-ttu-id="a4001-140">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a4001-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="a4001-141">Note</span><span class="sxs-lookup"><span data-stu-id="a4001-141">NOTES</span></span>

## <span data-ttu-id="a4001-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4001-142">RELATED LINKS</span></span>
