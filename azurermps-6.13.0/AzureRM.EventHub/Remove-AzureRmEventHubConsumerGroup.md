---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 2ef6227acf398b228d6ca5ffe4fad3d39ec75723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515364"
---
# <span data-ttu-id="97574-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="97574-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="97574-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97574-102">SYNOPSIS</span></span>
<span data-ttu-id="97574-103">Elimina il gruppo di utenti hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="97574-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97574-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97574-104">SYNTAX</span></span>

### <span data-ttu-id="97574-105">ConsumergroupPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97574-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97574-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="97574-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97574-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97574-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97574-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97574-108">DESCRIPTION</span></span>
<span data-ttu-id="97574-109">Il cmdlet Remove-AzureRmEventHubConsumerGroup rimuove ed Elimina il gruppo di utenti specificato dall'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="97574-109">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="97574-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97574-110">EXAMPLES</span></span>

### <span data-ttu-id="97574-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97574-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="97574-112">Elimina il gruppo Consumer \` MyConsumerGroupName \` dall'hub eventi \` MyEventHubName \` , ambito dello \` \` spazio dei nomi MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="97574-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="97574-113">Esempio 2,1-InputObject-using Variable</span><span class="sxs-lookup"><span data-stu-id="97574-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="97574-114">Esempio 2,2-InputObject-using piping</span><span class="sxs-lookup"><span data-stu-id="97574-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup <params> | Remove-AzureRmEventHubConsumerGroup
```

### <span data-ttu-id="97574-115">Esempio 3,1-ResourceId con vairable</span><span class="sxs-lookup"><span data-stu-id="97574-115">Example 3.1 - ResourceId Using Vairable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="97574-116">Esempio 3,2-ResourceId using String</span><span class="sxs-lookup"><span data-stu-id="97574-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="97574-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97574-117">PARAMETERS</span></span>

### <span data-ttu-id="97574-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97574-118">-AsJob</span></span>
<span data-ttu-id="97574-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="97574-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97574-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97574-120">-DefaultProfile</span></span>
<span data-ttu-id="97574-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97574-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97574-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="97574-122">-EventHub</span></span>
<span data-ttu-id="97574-123">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="97574-123">EventHub Name</span></span>

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

### <span data-ttu-id="97574-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97574-124">-InputObject</span></span>
<span data-ttu-id="97574-125">Oggetto ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="97574-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="97574-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="97574-126">-Name</span></span>
<span data-ttu-id="97574-127">Nome ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="97574-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="97574-128">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="97574-128">-Namespace</span></span>
<span data-ttu-id="97574-129">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="97574-129">Namespace Name</span></span>

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

### <span data-ttu-id="97574-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97574-130">-PassThru</span></span>
<span data-ttu-id="97574-131">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="97574-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="97574-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97574-132">-ResourceGroupName</span></span>
<span data-ttu-id="97574-133">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="97574-133">Resource Group Name</span></span>

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

### <span data-ttu-id="97574-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97574-134">-ResourceId</span></span>
<span data-ttu-id="97574-135">ID risorsa ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="97574-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="97574-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97574-136">-Confirm</span></span>
<span data-ttu-id="97574-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97574-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97574-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97574-138">-WhatIf</span></span>
<span data-ttu-id="97574-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97574-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97574-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97574-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97574-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97574-141">CommonParameters</span></span>
<span data-ttu-id="97574-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97574-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97574-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97574-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97574-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97574-144">INPUTS</span></span>

### <span data-ttu-id="97574-145">System. String</span><span class="sxs-lookup"><span data-stu-id="97574-145">System.String</span></span>

### <span data-ttu-id="97574-146">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="97574-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>
<span data-ttu-id="97574-147">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="97574-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="97574-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97574-148">OUTPUTS</span></span>

### <span data-ttu-id="97574-149">System. void</span><span class="sxs-lookup"><span data-stu-id="97574-149">System.Void</span></span>

## <span data-ttu-id="97574-150">Note</span><span class="sxs-lookup"><span data-stu-id="97574-150">NOTES</span></span>

## <span data-ttu-id="97574-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97574-151">RELATED LINKS</span></span>
