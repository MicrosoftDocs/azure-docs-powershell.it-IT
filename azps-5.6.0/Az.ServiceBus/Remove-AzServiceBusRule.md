---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: 673e67b9611cfab468c1c6f83393515bd4997e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015901"
---
# <span data-ttu-id="7d172-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="7d172-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="7d172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d172-102">SYNOPSIS</span></span>
<span data-ttu-id="7d172-103">Rimuove la regola specificata di un determinato abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7d172-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="7d172-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d172-104">SYNTAX</span></span>

### <span data-ttu-id="7d172-105">RulePropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d172-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d172-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7d172-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d172-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d172-107">DESCRIPTION</span></span>
<span data-ttu-id="7d172-108">Il cmdlet **Remove-AzServiceBusRule** rimuove la regola di una sottoscrizione di un determinato argomento.</span><span class="sxs-lookup"><span data-stu-id="7d172-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="7d172-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d172-109">EXAMPLES</span></span>

### <span data-ttu-id="7d172-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d172-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="7d172-111">Rimuove la regola `SBRule` di sottoscrizione `SBSubscription` dell'argomento `SBTopic` specificato.</span><span class="sxs-lookup"><span data-stu-id="7d172-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="7d172-112">Esempio 2: InputObject - Using Variable:</span><span class="sxs-lookup"><span data-stu-id="7d172-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="7d172-113">Rimuove la regola specificata tramite il parametro $inputobject for -InputObject</span><span class="sxs-lookup"><span data-stu-id="7d172-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="7d172-114">Esempio 3: InputObject - Uso di Piping:</span><span class="sxs-lookup"><span data-stu-id="7d172-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="7d172-115">Esempio 4: ResourceId - Using Variable</span><span class="sxs-lookup"><span data-stu-id="7d172-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="7d172-116">Esempio 5: ResourceId - Uso del valore stringa</span><span class="sxs-lookup"><span data-stu-id="7d172-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="7d172-117">Rimuove la regola specificata tramite l'ID ARM nel parametro $resourceid/string per -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d172-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="7d172-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d172-118">PARAMETERS</span></span>

### <span data-ttu-id="7d172-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d172-119">-AsJob</span></span>
<span data-ttu-id="7d172-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7d172-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d172-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d172-121">-DefaultProfile</span></span>
<span data-ttu-id="7d172-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d172-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d172-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7d172-123">-Force</span></span>
<span data-ttu-id="7d172-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7d172-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7d172-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d172-125">-InputObject</span></span>
<span data-ttu-id="7d172-126">Oggetto Regola bus di servizio</span><span class="sxs-lookup"><span data-stu-id="7d172-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d172-127">-Name</span><span class="sxs-lookup"><span data-stu-id="7d172-127">-Name</span></span>
<span data-ttu-id="7d172-128">Nome regola</span><span class="sxs-lookup"><span data-stu-id="7d172-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d172-129">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7d172-129">-Namespace</span></span>
<span data-ttu-id="7d172-130">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7d172-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d172-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d172-131">-PassThru</span></span>
<span data-ttu-id="7d172-132">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7d172-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7d172-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d172-133">-ResourceGroupName</span></span>
<span data-ttu-id="7d172-134">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7d172-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d172-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d172-135">-ResourceId</span></span>
<span data-ttu-id="7d172-136">ID risorsa regola bus di servizio</span><span class="sxs-lookup"><span data-stu-id="7d172-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d172-137">-Abbonamento</span><span class="sxs-lookup"><span data-stu-id="7d172-137">-Subscription</span></span>
<span data-ttu-id="7d172-138">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="7d172-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d172-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="7d172-139">-Topic</span></span>
<span data-ttu-id="7d172-140">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="7d172-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d172-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d172-141">-Confirm</span></span>
<span data-ttu-id="7d172-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d172-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d172-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d172-143">-WhatIf</span></span>
<span data-ttu-id="7d172-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d172-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d172-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d172-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d172-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d172-146">CommonParameters</span></span>
<span data-ttu-id="7d172-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d172-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d172-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d172-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d172-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d172-149">INPUTS</span></span>

### <span data-ttu-id="7d172-150">System.String</span><span class="sxs-lookup"><span data-stu-id="7d172-150">System.String</span></span>

### <span data-ttu-id="7d172-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="7d172-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="7d172-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d172-152">OUTPUTS</span></span>

### <span data-ttu-id="7d172-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7d172-153">System.Boolean</span></span>

## <span data-ttu-id="7d172-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d172-154">NOTES</span></span>

## <span data-ttu-id="7d172-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d172-155">RELATED LINKS</span></span>
