---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 1423c0c0c67b12b1cb2fcb6bf682d3ed60aae9c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993354"
---
# <span data-ttu-id="469b9-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="469b9-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="469b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="469b9-102">SYNOPSIS</span></span>
<span data-ttu-id="469b9-103">Rimuove la sottoscrizione di un argomento dallo spazio dei nomi dei bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="469b9-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="469b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="469b9-104">SYNTAX</span></span>

### <span data-ttu-id="469b9-105">SubscriptionPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="469b9-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="469b9-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="469b9-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="469b9-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="469b9-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="469b9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="469b9-108">DESCRIPTION</span></span>
<span data-ttu-id="469b9-109">Il cmdlet **Remove-AzServiceBusSubscription** rimuove la sottoscrizione a un argomento dallo spazio dei nomi del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="469b9-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="469b9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="469b9-110">EXAMPLES</span></span>

### <span data-ttu-id="469b9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="469b9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="469b9-112">Rimuove la sottoscrizione `SB-TopicSubscription-Example1` all'argomento `SB-Topic_exampl1` nello spazio dei nomi del bus di servizio `SB-Example1` specificato.</span><span class="sxs-lookup"><span data-stu-id="469b9-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="469b9-113">Esempio 2: InputObject - Using Variable:</span><span class="sxs-lookup"><span data-stu-id="469b9-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="469b9-114">Esempio 3: InputObject - Uso di Piping:</span><span class="sxs-lookup"><span data-stu-id="469b9-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="469b9-115">Esempio 4: ResourceId - Uso della variabile:</span><span class="sxs-lookup"><span data-stu-id="469b9-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="469b9-116">Esempio 5: ResourceId - Uso del valore stringa:</span><span class="sxs-lookup"><span data-stu-id="469b9-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="469b9-117">Rimuove la sottoscrizione specificata tramite l'ID ARM nel parametro $resourceid/string per -ResourceId</span><span class="sxs-lookup"><span data-stu-id="469b9-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="469b9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="469b9-118">PARAMETERS</span></span>

### <span data-ttu-id="469b9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="469b9-119">-AsJob</span></span>
<span data-ttu-id="469b9-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="469b9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="469b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="469b9-121">-DefaultProfile</span></span>
<span data-ttu-id="469b9-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="469b9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="469b9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="469b9-123">-InputObject</span></span>
<span data-ttu-id="469b9-124">Oggetto sottoscrizione bus di servizio</span><span class="sxs-lookup"><span data-stu-id="469b9-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="469b9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="469b9-125">-Name</span></span>
<span data-ttu-id="469b9-126">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="469b9-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="469b9-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="469b9-127">-Namespace</span></span>
<span data-ttu-id="469b9-128">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="469b9-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="469b9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="469b9-129">-PassThru</span></span>
<span data-ttu-id="469b9-130">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="469b9-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="469b9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="469b9-131">-ResourceGroupName</span></span>
<span data-ttu-id="469b9-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="469b9-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="469b9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="469b9-133">-ResourceId</span></span>
<span data-ttu-id="469b9-134">ID risorsa sottoscrizione bus di servizio</span><span class="sxs-lookup"><span data-stu-id="469b9-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="469b9-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="469b9-135">-Topic</span></span>
<span data-ttu-id="469b9-136">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="469b9-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="469b9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="469b9-137">-Confirm</span></span>
<span data-ttu-id="469b9-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="469b9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="469b9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="469b9-139">-WhatIf</span></span>
<span data-ttu-id="469b9-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="469b9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="469b9-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="469b9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="469b9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469b9-142">CommonParameters</span></span>
<span data-ttu-id="469b9-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="469b9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469b9-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="469b9-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469b9-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="469b9-145">INPUTS</span></span>

### <span data-ttu-id="469b9-146">System.String</span><span class="sxs-lookup"><span data-stu-id="469b9-146">System.String</span></span>

### <span data-ttu-id="469b9-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="469b9-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="469b9-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="469b9-148">OUTPUTS</span></span>

### <span data-ttu-id="469b9-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="469b9-149">System.Boolean</span></span>

## <span data-ttu-id="469b9-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="469b9-150">NOTES</span></span>

## <span data-ttu-id="469b9-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="469b9-151">RELATED LINKS</span></span>
