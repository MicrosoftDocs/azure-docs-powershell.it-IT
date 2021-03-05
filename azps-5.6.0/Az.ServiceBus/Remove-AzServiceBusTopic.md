---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 445108b2413673e2ce48dcbfac9f3fa0cdb45982
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993353"
---
# <span data-ttu-id="ba421-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ba421-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="ba421-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba421-102">SYNOPSIS</span></span>
<span data-ttu-id="ba421-103">Rimuove l'argomento dallo spazio dei nomi del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="ba421-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ba421-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba421-104">SYNTAX</span></span>

### <span data-ttu-id="ba421-105">TopicPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba421-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba421-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ba421-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba421-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ba421-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba421-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ba421-108">DESCRIPTION</span></span>
<span data-ttu-id="ba421-109">Il cmdlet **Remove-AzServiceBusTopic** rimuove l'argomento dallo spazio dei nomi del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="ba421-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ba421-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba421-110">EXAMPLES</span></span>

### <span data-ttu-id="ba421-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ba421-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="ba421-112">Rimuove l'argomento `SB-Topic_exampl1` dallo spazio dei `SB-Example1` nomi.</span><span class="sxs-lookup"><span data-stu-id="ba421-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="ba421-113">Esempio 2: InputObject - Using Variable:</span><span class="sxs-lookup"><span data-stu-id="ba421-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="ba421-114">Esempio 3: InputObject - Uso di Piping:</span><span class="sxs-lookup"><span data-stu-id="ba421-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="ba421-115">Esempio 4: ResourceId Using Variable:</span><span class="sxs-lookup"><span data-stu-id="ba421-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="ba421-116">Esempio 5: ResourceId Using String value</span><span class="sxs-lookup"><span data-stu-id="ba421-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="ba421-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba421-117">PARAMETERS</span></span>

### <span data-ttu-id="ba421-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba421-118">-AsJob</span></span>
<span data-ttu-id="ba421-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ba421-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba421-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba421-120">-DefaultProfile</span></span>
<span data-ttu-id="ba421-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba421-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba421-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba421-122">-InputObject</span></span>
<span data-ttu-id="ba421-123">Oggetto Argomento bus di servizio</span><span class="sxs-lookup"><span data-stu-id="ba421-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba421-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ba421-124">-Name</span></span>
<span data-ttu-id="ba421-125">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="ba421-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba421-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ba421-126">-Namespace</span></span>
<span data-ttu-id="ba421-127">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ba421-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba421-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba421-128">-PassThru</span></span>
<span data-ttu-id="ba421-129">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ba421-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ba421-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba421-130">-ResourceGroupName</span></span>
<span data-ttu-id="ba421-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ba421-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba421-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba421-132">-ResourceId</span></span>
<span data-ttu-id="ba421-133">ID risorsa argomento bus di servizio</span><span class="sxs-lookup"><span data-stu-id="ba421-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba421-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba421-134">-Confirm</span></span>
<span data-ttu-id="ba421-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba421-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba421-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba421-136">-WhatIf</span></span>
<span data-ttu-id="ba421-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba421-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba421-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba421-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba421-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba421-139">CommonParameters</span></span>
<span data-ttu-id="ba421-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba421-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba421-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba421-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba421-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="ba421-142">INPUTS</span></span>

### <span data-ttu-id="ba421-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ba421-143">System.String</span></span>

### <span data-ttu-id="ba421-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ba421-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="ba421-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba421-145">OUTPUTS</span></span>

### <span data-ttu-id="ba421-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba421-146">System.Boolean</span></span>

## <span data-ttu-id="ba421-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="ba421-147">NOTES</span></span>

## <span data-ttu-id="ba421-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba421-148">RELATED LINKS</span></span>
