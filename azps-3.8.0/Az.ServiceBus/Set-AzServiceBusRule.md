---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019041"
---
# <span data-ttu-id="9fa69-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="9fa69-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="9fa69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fa69-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa69-103">Aggiorna la descrizione della regola specificata per l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="9fa69-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="9fa69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fa69-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fa69-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fa69-105">DESCRIPTION</span></span>
<span data-ttu-id="9fa69-106">Il cmdlet **set-AzServiceBusRule** aggiorna la descrizione per la regola specificata dell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="9fa69-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="9fa69-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fa69-107">EXAMPLES</span></span>

### <span data-ttu-id="9fa69-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9fa69-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="9fa69-109">Aggiorna l'espressione SQL **mysqlexpression =' condition '** della regola `SBRule` della sottoscrizione `SBSubscription` in argomento `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="9fa69-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="9fa69-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fa69-110">PARAMETERS</span></span>

### <span data-ttu-id="9fa69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa69-111">-DefaultProfile</span></span>
<span data-ttu-id="9fa69-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa69-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fa69-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fa69-113">-InputObject</span></span>
<span data-ttu-id="9fa69-114">Definizione regole di ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="9fa69-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="9fa69-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9fa69-115">-Name</span></span>
<span data-ttu-id="9fa69-116">Nome della regola.</span><span class="sxs-lookup"><span data-stu-id="9fa69-116">Rule Name.</span></span>

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

### <span data-ttu-id="9fa69-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9fa69-117">-Namespace</span></span>
<span data-ttu-id="9fa69-118">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9fa69-118">Namespace Name.</span></span>

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

### <span data-ttu-id="9fa69-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa69-119">-ResourceGroupName</span></span>
<span data-ttu-id="9fa69-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9fa69-120">The name of the resource group</span></span>

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

### <span data-ttu-id="9fa69-121">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="9fa69-121">-Subscription</span></span>
<span data-ttu-id="9fa69-122">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9fa69-122">Subscription Name.</span></span>

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

### <span data-ttu-id="9fa69-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="9fa69-123">-Topic</span></span>
<span data-ttu-id="9fa69-124">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="9fa69-124">Topic Name.</span></span>

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

### <span data-ttu-id="9fa69-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9fa69-125">-Confirm</span></span>
<span data-ttu-id="9fa69-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fa69-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fa69-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fa69-127">-WhatIf</span></span>
<span data-ttu-id="9fa69-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fa69-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fa69-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fa69-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fa69-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa69-130">CommonParameters</span></span>
<span data-ttu-id="9fa69-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa69-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa69-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa69-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa69-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fa69-133">INPUTS</span></span>

### <span data-ttu-id="9fa69-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9fa69-134">System.String</span></span>

### <span data-ttu-id="9fa69-135">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="9fa69-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="9fa69-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fa69-136">OUTPUTS</span></span>

### <span data-ttu-id="9fa69-137">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="9fa69-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="9fa69-138">Note</span><span class="sxs-lookup"><span data-stu-id="9fa69-138">NOTES</span></span>

## <span data-ttu-id="9fa69-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fa69-139">RELATED LINKS</span></span>
