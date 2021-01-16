---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: ab9c9401b0f8d929be1a4aa244f407957d886e4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363716"
---
# <span data-ttu-id="59a65-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="59a65-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="59a65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59a65-102">SYNOPSIS</span></span>
<span data-ttu-id="59a65-103">Rigenera la chiave di accesso condivisa per un argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="59a65-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="59a65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59a65-104">SYNTAX</span></span>

### <span data-ttu-id="59a65-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59a65-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59a65-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59a65-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59a65-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="59a65-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59a65-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59a65-108">DESCRIPTION</span></span>
<span data-ttu-id="59a65-109">Rigenera la chiave di accesso condivisa per un argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="59a65-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="59a65-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59a65-110">EXAMPLES</span></span>

### <span data-ttu-id="59a65-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59a65-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="59a65-112">Rigenerare la chiave corrispondente alla chiave \' Key1' \ of Event Grid topic \` Topic1 \` nel gruppo di \` risorse MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="59a65-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="59a65-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="59a65-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="59a65-114">Rigenerare la chiave corrispondente alla chiave \' Key1' \ of Event Grid topic \` Topic1 \` nel gruppo di \` risorse MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="59a65-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="59a65-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59a65-115">PARAMETERS</span></span>

### <span data-ttu-id="59a65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a65-116">-DefaultProfile</span></span>
<span data-ttu-id="59a65-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="59a65-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59a65-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59a65-118">-InputObject</span></span>
<span data-ttu-id="59a65-119">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="59a65-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="59a65-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="59a65-120">-KeyName</span></span>
<span data-ttu-id="59a65-121">Nome della chiave che deve essere rigenerata</span><span class="sxs-lookup"><span data-stu-id="59a65-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="59a65-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a65-122">-ResourceGroupName</span></span>
<span data-ttu-id="59a65-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="59a65-123">Resource group name.</span></span>

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

### <span data-ttu-id="59a65-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59a65-124">-ResourceId</span></span>
<span data-ttu-id="59a65-125">Identificatore delle risorse che rappresenta l'argomento della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="59a65-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="59a65-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="59a65-126">-TopicName</span></span>
<span data-ttu-id="59a65-127">Nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="59a65-127">The name of the topic.</span></span>

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

### <span data-ttu-id="59a65-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59a65-128">-Confirm</span></span>
<span data-ttu-id="59a65-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59a65-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59a65-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59a65-130">-WhatIf</span></span>
<span data-ttu-id="59a65-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59a65-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59a65-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59a65-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59a65-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a65-133">CommonParameters</span></span>
<span data-ttu-id="59a65-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a65-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a65-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59a65-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a65-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59a65-136">INPUTS</span></span>

### <span data-ttu-id="59a65-137">System. String</span><span class="sxs-lookup"><span data-stu-id="59a65-137">System.String</span></span>

### <span data-ttu-id="59a65-138">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="59a65-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="59a65-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59a65-139">OUTPUTS</span></span>

### <span data-ttu-id="59a65-140">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="59a65-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="59a65-141">Note</span><span class="sxs-lookup"><span data-stu-id="59a65-141">NOTES</span></span>

## <span data-ttu-id="59a65-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59a65-142">RELATED LINKS</span></span>
