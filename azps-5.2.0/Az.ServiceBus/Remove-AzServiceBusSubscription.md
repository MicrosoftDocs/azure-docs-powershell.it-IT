---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: dd0dfb633fd48f2f747d6f4c0eb3471745b40da1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345739"
---
# <span data-ttu-id="01766-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="01766-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="01766-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01766-102">SYNOPSIS</span></span>
<span data-ttu-id="01766-103">Rimuove la sottoscrizione a un argomento dallo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="01766-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="01766-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01766-104">SYNTAX</span></span>

### <span data-ttu-id="01766-105">SubscriptionPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01766-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01766-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="01766-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01766-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="01766-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01766-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01766-108">DESCRIPTION</span></span>
<span data-ttu-id="01766-109">Il cmdlet **Remove-AzServiceBusSubscription** rimuove la sottoscrizione a un argomento dallo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="01766-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="01766-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01766-110">EXAMPLES</span></span>

### <span data-ttu-id="01766-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="01766-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="01766-112">Rimuove la sottoscrizione `SB-TopicSubscription-Example1` all'argomento `SB-Topic_exampl1` nello spazio dei nomi Service Bus specificato `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="01766-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="01766-113">Esempio 2: InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="01766-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="01766-114">Esempio 3: InputObject-using piping:</span><span class="sxs-lookup"><span data-stu-id="01766-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="01766-115">Esempio 4: ResourceId-using Variable:</span><span class="sxs-lookup"><span data-stu-id="01766-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="01766-116">Esempio 5: ResourceId-using Value String:</span><span class="sxs-lookup"><span data-stu-id="01766-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="01766-117">Rimuove l'abbonamento fornito tramite ID ARM in $resourceid parametro/String for-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01766-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="01766-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01766-118">PARAMETERS</span></span>

### <span data-ttu-id="01766-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01766-119">-AsJob</span></span>
<span data-ttu-id="01766-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="01766-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01766-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01766-121">-DefaultProfile</span></span>
<span data-ttu-id="01766-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01766-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01766-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01766-123">-InputObject</span></span>
<span data-ttu-id="01766-124">Oggetto abbonamento a Service Bus</span><span class="sxs-lookup"><span data-stu-id="01766-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="01766-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="01766-125">-Name</span></span>
<span data-ttu-id="01766-126">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="01766-126">Subscription Name</span></span>

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

### <span data-ttu-id="01766-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="01766-127">-Namespace</span></span>
<span data-ttu-id="01766-128">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="01766-128">Namespace Name</span></span>

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

### <span data-ttu-id="01766-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01766-129">-PassThru</span></span>
<span data-ttu-id="01766-130">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="01766-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="01766-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01766-131">-ResourceGroupName</span></span>
<span data-ttu-id="01766-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="01766-132">The name of the resource group</span></span>

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

### <span data-ttu-id="01766-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01766-133">-ResourceId</span></span>
<span data-ttu-id="01766-134">ID risorsa abbonamento bus di servizio</span><span class="sxs-lookup"><span data-stu-id="01766-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="01766-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="01766-135">-Topic</span></span>
<span data-ttu-id="01766-136">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="01766-136">Topic Name</span></span>

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

### <span data-ttu-id="01766-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="01766-137">-Confirm</span></span>
<span data-ttu-id="01766-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01766-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01766-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01766-139">-WhatIf</span></span>
<span data-ttu-id="01766-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01766-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01766-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01766-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01766-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01766-142">CommonParameters</span></span>
<span data-ttu-id="01766-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01766-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01766-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01766-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01766-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01766-145">INPUTS</span></span>

### <span data-ttu-id="01766-146">System. String</span><span class="sxs-lookup"><span data-stu-id="01766-146">System.String</span></span>

### <span data-ttu-id="01766-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="01766-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="01766-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01766-148">OUTPUTS</span></span>

### <span data-ttu-id="01766-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01766-149">System.Boolean</span></span>

## <span data-ttu-id="01766-150">Note</span><span class="sxs-lookup"><span data-stu-id="01766-150">NOTES</span></span>

## <span data-ttu-id="01766-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01766-151">RELATED LINKS</span></span>
