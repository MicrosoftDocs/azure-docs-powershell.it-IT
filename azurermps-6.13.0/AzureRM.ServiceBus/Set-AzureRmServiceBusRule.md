---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: cb6200156b68524119df86e24d812b97bcd250e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514800"
---
# <span data-ttu-id="bcb41-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="bcb41-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="bcb41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcb41-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb41-103">Aggiorna la descrizione della regola specificata per l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="bcb41-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcb41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcb41-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcb41-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcb41-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb41-106">Il cmdlet **set-AzureRmServiceBusRule** aggiorna la descrizione per la regola specificata dell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="bcb41-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="bcb41-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcb41-107">EXAMPLES</span></span>

### <span data-ttu-id="bcb41-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bcb41-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="bcb41-109">Aggiorna la SqlExpression **mysqlexpression =' condition '** della regola `SBEule` della sottoscrizione `SBSubscription` in argomento `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="bcb41-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="bcb41-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcb41-110">PARAMETERS</span></span>

### <span data-ttu-id="bcb41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb41-111">-DefaultProfile</span></span>
<span data-ttu-id="bcb41-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb41-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcb41-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcb41-113">-InputObject</span></span>
<span data-ttu-id="bcb41-114">Definizione regole di ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="bcb41-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="bcb41-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcb41-115">-Name</span></span>
<span data-ttu-id="bcb41-116">Nome della regola.</span><span class="sxs-lookup"><span data-stu-id="bcb41-116">Rule Name.</span></span>

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

### <span data-ttu-id="bcb41-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bcb41-117">-Namespace</span></span>
<span data-ttu-id="bcb41-118">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="bcb41-118">Namespace Name.</span></span>

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

### <span data-ttu-id="bcb41-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb41-119">-ResourceGroupName</span></span>
<span data-ttu-id="bcb41-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="bcb41-120">The name of the resource group</span></span>

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

### <span data-ttu-id="bcb41-121">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="bcb41-121">-Subscription</span></span>
<span data-ttu-id="bcb41-122">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bcb41-122">Subscription Name.</span></span>

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

### <span data-ttu-id="bcb41-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="bcb41-123">-Topic</span></span>
<span data-ttu-id="bcb41-124">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="bcb41-124">Topic Name.</span></span>

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

### <span data-ttu-id="bcb41-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bcb41-125">-Confirm</span></span>
<span data-ttu-id="bcb41-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcb41-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcb41-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcb41-127">-WhatIf</span></span>
<span data-ttu-id="bcb41-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcb41-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcb41-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcb41-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcb41-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb41-130">CommonParameters</span></span>
<span data-ttu-id="bcb41-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb41-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb41-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb41-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb41-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcb41-133">INPUTS</span></span>

### <span data-ttu-id="bcb41-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bcb41-134">System.String</span></span>

### <span data-ttu-id="bcb41-135">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="bcb41-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="bcb41-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcb41-136">OUTPUTS</span></span>

### <span data-ttu-id="bcb41-137">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="bcb41-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="bcb41-138">Note</span><span class="sxs-lookup"><span data-stu-id="bcb41-138">NOTES</span></span>

## <span data-ttu-id="bcb41-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcb41-139">RELATED LINKS</span></span>
