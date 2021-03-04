---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: 2caf2ccfe0d3428515812aa2dfeafc1237f820f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981597"
---
# <span data-ttu-id="3e410-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="3e410-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="3e410-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e410-102">SYNOPSIS</span></span>
<span data-ttu-id="3e410-103">Aggiorna la descrizione della regola specificata per l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="3e410-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="3e410-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e410-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e410-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e410-105">DESCRIPTION</span></span>
<span data-ttu-id="3e410-106">Il **cmdlet Set-AzServiceBusRule** aggiorna la descrizione della regola specificata della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="3e410-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="3e410-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e410-107">EXAMPLES</span></span>

### <span data-ttu-id="3e410-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e410-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="3e410-109">Aggiorna l'espressione **sql mysqlexpression='condizione'** della `SBRule` regola della sottoscrizione in `SBSubscription` Topic `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="3e410-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="3e410-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e410-110">PARAMETERS</span></span>

### <span data-ttu-id="3e410-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e410-111">-DefaultProfile</span></span>
<span data-ttu-id="3e410-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e410-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e410-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e410-113">-InputObject</span></span>
<span data-ttu-id="3e410-114">Definizione delle regole ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="3e410-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e410-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3e410-115">-Name</span></span>
<span data-ttu-id="3e410-116">Nome regola.</span><span class="sxs-lookup"><span data-stu-id="3e410-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e410-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3e410-117">-Namespace</span></span>
<span data-ttu-id="3e410-118">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3e410-118">Namespace Name.</span></span>

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

### <span data-ttu-id="3e410-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e410-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e410-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3e410-120">The name of the resource group</span></span>

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

### <span data-ttu-id="3e410-121">-Abbonamento</span><span class="sxs-lookup"><span data-stu-id="3e410-121">-Subscription</span></span>
<span data-ttu-id="3e410-122">Nome abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3e410-122">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e410-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="3e410-123">-Topic</span></span>
<span data-ttu-id="3e410-124">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="3e410-124">Topic Name.</span></span>

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

### <span data-ttu-id="3e410-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e410-125">-Confirm</span></span>
<span data-ttu-id="3e410-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e410-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e410-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e410-127">-WhatIf</span></span>
<span data-ttu-id="3e410-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e410-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e410-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e410-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e410-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e410-130">CommonParameters</span></span>
<span data-ttu-id="3e410-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e410-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e410-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e410-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e410-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e410-133">INPUTS</span></span>

### <span data-ttu-id="3e410-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3e410-134">System.String</span></span>

### <span data-ttu-id="3e410-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3e410-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="3e410-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e410-136">OUTPUTS</span></span>

### <span data-ttu-id="3e410-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3e410-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="3e410-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e410-138">NOTES</span></span>

## <span data-ttu-id="3e410-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e410-139">RELATED LINKS</span></span>
