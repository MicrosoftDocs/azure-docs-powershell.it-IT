---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: 12064269e3a8c2e424bbd0e15888968c679784e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961661"
---
# <span data-ttu-id="f3ea2-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="f3ea2-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="f3ea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ea2-103">Crea una nuova regola per una determinata sottoscrizione dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="f3ea2-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="f3ea2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3ea2-104">SYNTAX</span></span>

### <span data-ttu-id="f3ea2-105">RulePropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3ea2-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3ea2-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f3ea2-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3ea2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f3ea2-107">DESCRIPTION</span></span>
<span data-ttu-id="f3ea2-108">Il cmdlet **New-AzServiceBusRule** crea una nuova regola per la sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="f3ea2-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="f3ea2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3ea2-109">EXAMPLES</span></span>

### <span data-ttu-id="f3ea2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f3ea2-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="f3ea2-111">Il cmdlet New-AzServiceBusRule crea una nuova regola per la Sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="f3ea2-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="f3ea2-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f3ea2-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="f3ea2-113">Il New-AzServiceBusRule cmdlet crea una nuova regola per la sottoscrizione specificata con ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="f3ea2-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="f3ea2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3ea2-114">PARAMETERS</span></span>

### <span data-ttu-id="f3ea2-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="f3ea2-115">-ActionSqlExpression</span></span>
<span data-ttu-id="f3ea2-116">Espressione SqlFilter per azioni</span><span class="sxs-lookup"><span data-stu-id="f3ea2-116">Action SqlFilter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ea2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ea2-117">-DefaultProfile</span></span>
<span data-ttu-id="f3ea2-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ea2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3ea2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f3ea2-119">-Name</span></span>
<span data-ttu-id="f3ea2-120">Nome regola</span><span class="sxs-lookup"><span data-stu-id="f3ea2-120">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ea2-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3ea2-121">-Namespace</span></span>
<span data-ttu-id="f3ea2-122">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3ea2-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ea2-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="f3ea2-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="f3ea2-124">L'azione richiede la pre-elaborazione</span><span class="sxs-lookup"><span data-stu-id="f3ea2-124">Action Requires Preprocessing</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ea2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ea2-125">-ResourceGroupName</span></span>
<span data-ttu-id="f3ea2-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f3ea2-126">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ea2-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="f3ea2-127">-SqlExpression</span></span>
<span data-ttu-id="f3ea2-128">Espressione filtro Sql</span><span class="sxs-lookup"><span data-stu-id="f3ea2-128">Sql Filter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ea2-129">-Abbonamento</span><span class="sxs-lookup"><span data-stu-id="f3ea2-129">-Subscription</span></span>
<span data-ttu-id="f3ea2-130">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="f3ea2-130">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ea2-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="f3ea2-131">-Topic</span></span>
<span data-ttu-id="f3ea2-132">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="f3ea2-132">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ea2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3ea2-133">-Confirm</span></span>
<span data-ttu-id="f3ea2-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3ea2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ea2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ea2-135">-WhatIf</span></span>
<span data-ttu-id="f3ea2-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3ea2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3ea2-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3ea2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ea2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ea2-138">CommonParameters</span></span>
<span data-ttu-id="f3ea2-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ea2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ea2-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ea2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ea2-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="f3ea2-141">INPUTS</span></span>

### <span data-ttu-id="f3ea2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f3ea2-142">System.String</span></span>

## <span data-ttu-id="f3ea2-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3ea2-143">OUTPUTS</span></span>

### <span data-ttu-id="f3ea2-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="f3ea2-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="f3ea2-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="f3ea2-145">NOTES</span></span>

## <span data-ttu-id="f3ea2-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3ea2-146">RELATED LINKS</span></span>
