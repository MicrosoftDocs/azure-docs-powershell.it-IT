---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: badbb8c392e053b1f8d994164183bd593843629e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516631"
---
# <span data-ttu-id="62936-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="62936-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="62936-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62936-102">SYNOPSIS</span></span>
<span data-ttu-id="62936-103">Rigenera la chiave di accesso condivisa per un argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="62936-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62936-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62936-104">SYNTAX</span></span>

### <span data-ttu-id="62936-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62936-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62936-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62936-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62936-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="62936-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62936-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62936-108">DESCRIPTION</span></span>
<span data-ttu-id="62936-109">Rigenera la chiave di accesso condivisa per un argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="62936-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="62936-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62936-110">EXAMPLES</span></span>

### <span data-ttu-id="62936-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62936-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="62936-112">Rigenerare la chiave corrispondente alla chiave \' Key1' \ of Event Grid topic \` Topic1 \` nel gruppo di \` risorse MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="62936-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="62936-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="62936-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="62936-114">Rigenerare la chiave corrispondente alla chiave \' Key1' \ of Event Grid topic \` Topic1 \` nel gruppo di \` risorse MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="62936-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="62936-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62936-115">PARAMETERS</span></span>

### <span data-ttu-id="62936-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62936-116">-DefaultProfile</span></span>
<span data-ttu-id="62936-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="62936-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62936-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62936-118">-InputObject</span></span>
<span data-ttu-id="62936-119">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="62936-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="62936-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="62936-120">-KeyName</span></span>
<span data-ttu-id="62936-121">Nome della chiave che deve essere rigenerata</span><span class="sxs-lookup"><span data-stu-id="62936-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62936-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62936-122">-ResourceGroupName</span></span>
<span data-ttu-id="62936-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62936-123">Resource group name.</span></span>

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

### <span data-ttu-id="62936-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62936-124">-ResourceId</span></span>
<span data-ttu-id="62936-125">Identificatore delle risorse che rappresenta l'argomento della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="62936-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="62936-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="62936-126">-TopicName</span></span>
<span data-ttu-id="62936-127">Nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="62936-127">The name of the topic.</span></span>

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

### <span data-ttu-id="62936-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62936-128">-Confirm</span></span>
<span data-ttu-id="62936-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62936-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62936-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62936-130">-WhatIf</span></span>
<span data-ttu-id="62936-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62936-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62936-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62936-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62936-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62936-133">CommonParameters</span></span>
<span data-ttu-id="62936-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62936-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62936-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62936-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62936-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62936-136">INPUTS</span></span>

### <span data-ttu-id="62936-137">System. String</span><span class="sxs-lookup"><span data-stu-id="62936-137">System.String</span></span>

### <span data-ttu-id="62936-138">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="62936-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="62936-139">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="62936-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="62936-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62936-140">OUTPUTS</span></span>

### <span data-ttu-id="62936-141">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="62936-141">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="62936-142">Note</span><span class="sxs-lookup"><span data-stu-id="62936-142">NOTES</span></span>

## <span data-ttu-id="62936-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62936-143">RELATED LINKS</span></span>
