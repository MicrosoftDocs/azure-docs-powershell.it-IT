---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: b8b2b9f6bb8a082647a14285a907465e8e12348f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516480"
---
# <span data-ttu-id="4e27a-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="4e27a-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="4e27a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e27a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e27a-103">Rimuove la sottoscrizione a un argomento dallo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="4e27a-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e27a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e27a-104">SYNTAX</span></span>

### <span data-ttu-id="4e27a-105">SubscriptionPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4e27a-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e27a-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4e27a-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzureRmServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e27a-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4e27a-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzureRmServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e27a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e27a-108">DESCRIPTION</span></span>
<span data-ttu-id="4e27a-109">Il cmdlet **Remove-AzureRmServiceBusSubscription** rimuove la sottoscrizione a un argomento dallo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="4e27a-109">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="4e27a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e27a-110">EXAMPLES</span></span>

### <span data-ttu-id="4e27a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e27a-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="4e27a-112">Rimuove la sottoscrizione `SB-TopicSubscription-Example1` all'argomento `SB-Topic_exampl1` nello spazio dei nomi Service Bus specificato `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="4e27a-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="4e27a-113">Esempio 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="4e27a-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusSubscription <params>
PS C:\> Remove-AzureRmServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="4e27a-114">Esempio 2,2-InputObject-using piping:</span><span class="sxs-lookup"><span data-stu-id="4e27a-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzureRmServiceBusSubscription <params> |Remove-AzureRmServiceBusSubscription
```

### <span data-ttu-id="4e27a-115">Esempio 3,1-ResourceId-using Variable:</span><span class="sxs-lookup"><span data-stu-id="4e27a-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusSubscription <params>
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="4e27a-116">Esempio 3,2-ResourceId-using Value String:</span><span class="sxs-lookup"><span data-stu-id="4e27a-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="4e27a-117">Rimuove l'abbonamento fornito tramite ID ARM in $resourceid parametro/String for-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e27a-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="4e27a-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e27a-118">PARAMETERS</span></span>

### <span data-ttu-id="4e27a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e27a-119">-AsJob</span></span>
<span data-ttu-id="4e27a-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4e27a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e27a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e27a-121">-DefaultProfile</span></span>
<span data-ttu-id="4e27a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e27a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e27a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e27a-123">-InputObject</span></span>
<span data-ttu-id="4e27a-124">Oggetto abbonamento a Service Bus</span><span class="sxs-lookup"><span data-stu-id="4e27a-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="4e27a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e27a-125">-Name</span></span>
<span data-ttu-id="4e27a-126">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="4e27a-126">Subscription Name</span></span>

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

### <span data-ttu-id="4e27a-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e27a-127">-Namespace</span></span>
<span data-ttu-id="4e27a-128">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e27a-128">Namespace Name</span></span>

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

### <span data-ttu-id="4e27a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e27a-129">-PassThru</span></span>
<span data-ttu-id="4e27a-130">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="4e27a-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4e27a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e27a-131">-ResourceGroupName</span></span>
<span data-ttu-id="4e27a-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4e27a-132">The name of the resource group</span></span>

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

### <span data-ttu-id="4e27a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e27a-133">-ResourceId</span></span>
<span data-ttu-id="4e27a-134">ID risorsa abbonamento bus di servizio</span><span class="sxs-lookup"><span data-stu-id="4e27a-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="4e27a-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="4e27a-135">-Topic</span></span>
<span data-ttu-id="4e27a-136">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="4e27a-136">Topic Name</span></span>

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

### <span data-ttu-id="4e27a-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e27a-137">-Confirm</span></span>
<span data-ttu-id="4e27a-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e27a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e27a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e27a-139">-WhatIf</span></span>
<span data-ttu-id="4e27a-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e27a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e27a-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e27a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e27a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e27a-142">CommonParameters</span></span>
<span data-ttu-id="4e27a-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e27a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e27a-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e27a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e27a-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e27a-145">INPUTS</span></span>

### <span data-ttu-id="4e27a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4e27a-146">System.String</span></span>

### <span data-ttu-id="4e27a-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="4e27a-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>
<span data-ttu-id="4e27a-148">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4e27a-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4e27a-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e27a-149">OUTPUTS</span></span>

### <span data-ttu-id="4e27a-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4e27a-150">System.Boolean</span></span>

## <span data-ttu-id="4e27a-151">Note</span><span class="sxs-lookup"><span data-stu-id="4e27a-151">NOTES</span></span>

## <span data-ttu-id="4e27a-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e27a-152">RELATED LINKS</span></span>
