---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: 8f5f1ae36355f1f8d76476e5eee69f63187847ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992709"
---
# <span data-ttu-id="a3862-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a3862-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="a3862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3862-102">SYNOPSIS</span></span>
<span data-ttu-id="a3862-103">Elimina il gruppo consumer hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="a3862-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="a3862-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3862-104">SYNTAX</span></span>

### <span data-ttu-id="a3862-105">ConsumergroupPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a3862-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3862-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a3862-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3862-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3862-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3862-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a3862-108">DESCRIPTION</span></span>
<span data-ttu-id="a3862-109">Il cmdlet Remove-AzEventHubConsumerGroup rimuove ed elimina il gruppo consumer specificato dall'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="a3862-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="a3862-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3862-110">EXAMPLES</span></span>

### <span data-ttu-id="a3862-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3862-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="a3862-112">Elimina il gruppo consumer \` MyConsumerGroupName dall'hub eventi MyEventHubName, con ambito allo spazio \` \` dei nomi \` \` \` MyHubName.</span><span class="sxs-lookup"><span data-stu-id="a3862-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="a3862-113">Esempio 2: InputObject - Using Variable</span><span class="sxs-lookup"><span data-stu-id="a3862-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="a3862-114">Esempio 3: InputObject - Uso di Piping</span><span class="sxs-lookup"><span data-stu-id="a3862-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="a3862-115">Esempio 4: ResourceId Using Variable</span><span class="sxs-lookup"><span data-stu-id="a3862-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="a3862-116">Esempio 5: ResourceId Using string</span><span class="sxs-lookup"><span data-stu-id="a3862-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="a3862-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3862-117">PARAMETERS</span></span>

### <span data-ttu-id="a3862-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3862-118">-AsJob</span></span>
<span data-ttu-id="a3862-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a3862-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3862-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3862-120">-DefaultProfile</span></span>
<span data-ttu-id="a3862-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3862-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3862-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a3862-122">-EventHub</span></span>
<span data-ttu-id="a3862-123">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="a3862-123">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3862-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3862-124">-InputObject</span></span>
<span data-ttu-id="a3862-125">Oggetto ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a3862-125">ConsumerGroup Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes
Parameter Sets: ConsumergroupInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3862-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a3862-126">-Name</span></span>
<span data-ttu-id="a3862-127">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="a3862-127">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3862-128">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a3862-128">-Namespace</span></span>
<span data-ttu-id="a3862-129">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a3862-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3862-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3862-130">-PassThru</span></span>
<span data-ttu-id="a3862-131">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a3862-131">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3862-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3862-132">-ResourceGroupName</span></span>
<span data-ttu-id="a3862-133">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a3862-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3862-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3862-134">-ResourceId</span></span>
<span data-ttu-id="a3862-135">ID risorsa ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a3862-135">ConsumerGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3862-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3862-136">-Confirm</span></span>
<span data-ttu-id="a3862-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3862-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3862-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3862-138">-WhatIf</span></span>
<span data-ttu-id="a3862-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3862-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3862-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3862-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3862-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3862-141">CommonParameters</span></span>
<span data-ttu-id="a3862-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3862-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3862-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3862-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3862-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="a3862-144">INPUTS</span></span>

### <span data-ttu-id="a3862-145">System.String</span><span class="sxs-lookup"><span data-stu-id="a3862-145">System.String</span></span>

### <span data-ttu-id="a3862-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="a3862-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="a3862-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3862-147">OUTPUTS</span></span>

### <span data-ttu-id="a3862-148">System.Void</span><span class="sxs-lookup"><span data-stu-id="a3862-148">System.Void</span></span>

## <span data-ttu-id="a3862-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="a3862-149">NOTES</span></span>

## <span data-ttu-id="a3862-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3862-150">RELATED LINKS</span></span>
