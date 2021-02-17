---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: ab9c9401b0f8d929be1a4aa244f407957d886e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188494"
---
# <span data-ttu-id="92c93-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="92c93-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="92c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92c93-102">SYNOPSIS</span></span>
<span data-ttu-id="92c93-103">Rigenera la chiave di accesso condiviso per un argomento della griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="92c93-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="92c93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92c93-104">SYNTAX</span></span>

### <span data-ttu-id="92c93-105">TopicNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92c93-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92c93-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92c93-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92c93-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="92c93-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92c93-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="92c93-108">DESCRIPTION</span></span>
<span data-ttu-id="92c93-109">Rigenera la chiave di accesso condiviso per un argomento della griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="92c93-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="92c93-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92c93-110">EXAMPLES</span></span>

### <span data-ttu-id="92c93-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="92c93-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="92c93-112">Rigenerare la chiave corrispondente a key key1'\ dell'argomento Griglia eventi Topic1 nel gruppo di \' \` risorse \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="92c93-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="92c93-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="92c93-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="92c93-114">Rigenerare la chiave corrispondente a key key1'\ dell'argomento Griglia eventi Topic1 nel gruppo di \' \` risorse \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="92c93-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="92c93-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92c93-115">PARAMETERS</span></span>

### <span data-ttu-id="92c93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92c93-116">-DefaultProfile</span></span>
<span data-ttu-id="92c93-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="92c93-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92c93-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92c93-118">-InputObject</span></span>
<span data-ttu-id="92c93-119">Oggetto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="92c93-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="92c93-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="92c93-120">-KeyName</span></span>
<span data-ttu-id="92c93-121">Il nome della chiave che deve essere rigenerata</span><span class="sxs-lookup"><span data-stu-id="92c93-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="92c93-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92c93-122">-ResourceGroupName</span></span>
<span data-ttu-id="92c93-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="92c93-123">Resource group name.</span></span>

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

### <span data-ttu-id="92c93-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92c93-124">-ResourceId</span></span>
<span data-ttu-id="92c93-125">Identificatore di risorsa che rappresenta l'argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="92c93-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="92c93-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="92c93-126">-TopicName</span></span>
<span data-ttu-id="92c93-127">Nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="92c93-127">The name of the topic.</span></span>

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

### <span data-ttu-id="92c93-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92c93-128">-Confirm</span></span>
<span data-ttu-id="92c93-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92c93-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92c93-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92c93-130">-WhatIf</span></span>
<span data-ttu-id="92c93-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92c93-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92c93-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92c93-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92c93-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92c93-133">CommonParameters</span></span>
<span data-ttu-id="92c93-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92c93-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92c93-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92c93-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92c93-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="92c93-136">INPUTS</span></span>

### <span data-ttu-id="92c93-137">System.String</span><span class="sxs-lookup"><span data-stu-id="92c93-137">System.String</span></span>

### <span data-ttu-id="92c93-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="92c93-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="92c93-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92c93-139">OUTPUTS</span></span>

### <span data-ttu-id="92c93-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="92c93-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="92c93-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="92c93-141">NOTES</span></span>

## <span data-ttu-id="92c93-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92c93-142">RELATED LINKS</span></span>
