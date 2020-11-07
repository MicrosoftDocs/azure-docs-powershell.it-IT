---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: 4fb10e2bb438cbc4f40936f9f9ead5c0bb36d861
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687977"
---
# <span data-ttu-id="6e9b1-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="6e9b1-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="6e9b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e9b1-102">SYNOPSIS</span></span>
<span data-ttu-id="6e9b1-103">Aggiorna la descrizione della regola specificata per l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e9b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e9b1-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <RulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e9b1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e9b1-105">DESCRIPTION</span></span>
<span data-ttu-id="6e9b1-106">Il cmdlet **set-AzureRmServiceBusRule** aggiorna la descrizione per la regola specificata dell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="6e9b1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e9b1-107">EXAMPLES</span></span>

### <span data-ttu-id="6e9b1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6e9b1-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="6e9b1-109">Aggiorna la SqlExpression **mysqlexpression =' condition '** della regola `SBEule` della sottoscrizione `SBSubscription` in argomento `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="6e9b1-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="6e9b1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e9b1-110">PARAMETERS</span></span>

### <span data-ttu-id="6e9b1-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6e9b1-111">-Confirm</span></span>
<span data-ttu-id="6e9b1-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e9b1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e9b1-113">-InputObject</span></span>
<span data-ttu-id="6e9b1-114">Definizione regole di ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9b1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e9b1-115">-Name</span></span>
<span data-ttu-id="6e9b1-116">Nome della regola.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-116">Rule Name.</span></span>

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

### <span data-ttu-id="6e9b1-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6e9b1-117">-Namespace</span></span>
<span data-ttu-id="6e9b1-118">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-118">Namespace Name.</span></span>

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

### <span data-ttu-id="6e9b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e9b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e9b1-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6e9b1-120">The name of the resource group</span></span>

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

### <span data-ttu-id="6e9b1-121">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="6e9b1-121">-Subscription</span></span>
<span data-ttu-id="6e9b1-122">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-122">Subscription Name.</span></span>

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

### <span data-ttu-id="6e9b1-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="6e9b1-123">-Topic</span></span>
<span data-ttu-id="6e9b1-124">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-124">Topic Name.</span></span>

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

### <span data-ttu-id="6e9b1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e9b1-125">-WhatIf</span></span>
<span data-ttu-id="6e9b1-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e9b1-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e9b1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e9b1-128">-DefaultProfile</span></span>
<span data-ttu-id="6e9b1-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e9b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e9b1-130">CommonParameters</span></span>
<span data-ttu-id="6e9b1-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e9b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e9b1-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e9b1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e9b1-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e9b1-133">INPUTS</span></span>

### <span data-ttu-id="6e9b1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6e9b1-134">System.String</span></span>
<span data-ttu-id="6e9b1-135">Microsoft. Azure. Commands. ServiceBus. Models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="6e9b1-135">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="6e9b1-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e9b1-136">OUTPUTS</span></span>

### <span data-ttu-id="6e9b1-137">Microsoft. Azure. Commands. ServiceBus. Models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="6e9b1-137">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="6e9b1-138">Note</span><span class="sxs-lookup"><span data-stu-id="6e9b1-138">NOTES</span></span>

## <span data-ttu-id="6e9b1-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e9b1-139">RELATED LINKS</span></span>

