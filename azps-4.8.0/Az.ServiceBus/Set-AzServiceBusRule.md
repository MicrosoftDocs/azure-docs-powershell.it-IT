---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031066"
---
# <span data-ttu-id="fee30-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="fee30-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="fee30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fee30-102">SYNOPSIS</span></span>
<span data-ttu-id="fee30-103">Aggiorna la descrizione della regola specificata per l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="fee30-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="fee30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fee30-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fee30-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fee30-105">DESCRIPTION</span></span>
<span data-ttu-id="fee30-106">Il cmdlet **set-AzServiceBusRule** aggiorna la descrizione per la regola specificata dell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="fee30-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="fee30-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fee30-107">EXAMPLES</span></span>

### <span data-ttu-id="fee30-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fee30-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="fee30-109">Aggiorna l'espressione SQL **mysqlexpression =' condition '** della regola `SBRule` della sottoscrizione `SBSubscription` in argomento `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="fee30-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="fee30-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fee30-110">PARAMETERS</span></span>

### <span data-ttu-id="fee30-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee30-111">-DefaultProfile</span></span>
<span data-ttu-id="fee30-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fee30-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fee30-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fee30-113">-InputObject</span></span>
<span data-ttu-id="fee30-114">Definizione regole di ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="fee30-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="fee30-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fee30-115">-Name</span></span>
<span data-ttu-id="fee30-116">Nome della regola.</span><span class="sxs-lookup"><span data-stu-id="fee30-116">Rule Name.</span></span>

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

### <span data-ttu-id="fee30-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fee30-117">-Namespace</span></span>
<span data-ttu-id="fee30-118">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fee30-118">Namespace Name.</span></span>

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

### <span data-ttu-id="fee30-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee30-119">-ResourceGroupName</span></span>
<span data-ttu-id="fee30-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fee30-120">The name of the resource group</span></span>

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

### <span data-ttu-id="fee30-121">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="fee30-121">-Subscription</span></span>
<span data-ttu-id="fee30-122">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fee30-122">Subscription Name.</span></span>

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

### <span data-ttu-id="fee30-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="fee30-123">-Topic</span></span>
<span data-ttu-id="fee30-124">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="fee30-124">Topic Name.</span></span>

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

### <span data-ttu-id="fee30-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fee30-125">-Confirm</span></span>
<span data-ttu-id="fee30-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fee30-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee30-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee30-127">-WhatIf</span></span>
<span data-ttu-id="fee30-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fee30-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee30-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fee30-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee30-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee30-130">CommonParameters</span></span>
<span data-ttu-id="fee30-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee30-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee30-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fee30-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee30-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fee30-133">INPUTS</span></span>

### <span data-ttu-id="fee30-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fee30-134">System.String</span></span>

### <span data-ttu-id="fee30-135">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="fee30-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="fee30-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fee30-136">OUTPUTS</span></span>

### <span data-ttu-id="fee30-137">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="fee30-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="fee30-138">Note</span><span class="sxs-lookup"><span data-stu-id="fee30-138">NOTES</span></span>

## <span data-ttu-id="fee30-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fee30-139">RELATED LINKS</span></span>
