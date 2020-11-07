---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: f3d9c9029b1c87e6d58dde21eac9d41857f53ab8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854654"
---
# <span data-ttu-id="17ad7-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="17ad7-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="17ad7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="17ad7-103">Crea una nuova regola per una determinata sottoscrizione di argomenti.</span><span class="sxs-lookup"><span data-stu-id="17ad7-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="17ad7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17ad7-104">SYNTAX</span></span>

### <span data-ttu-id="17ad7-105">RulePropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17ad7-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17ad7-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="17ad7-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17ad7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17ad7-107">DESCRIPTION</span></span>
<span data-ttu-id="17ad7-108">Il cmdlet **New-AzServiceBusRule** crea una nuova regola per la sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="17ad7-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="17ad7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17ad7-109">EXAMPLES</span></span>

### <span data-ttu-id="17ad7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17ad7-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="17ad7-111">Il cmdlet New-AzServiceBusRule crea una nuova regola per l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="17ad7-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="17ad7-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="17ad7-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="17ad7-113">Il cmdlet New-AzServiceBusRule crea una nuova regola per l'abbonamento specificato con ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="17ad7-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="17ad7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17ad7-114">PARAMETERS</span></span>

### <span data-ttu-id="17ad7-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="17ad7-115">-ActionSqlExpression</span></span>
<span data-ttu-id="17ad7-116">Espressione SqlFilter azione</span><span class="sxs-lookup"><span data-stu-id="17ad7-116">Action SqlFilter Expression</span></span>

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

### <span data-ttu-id="17ad7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ad7-117">-DefaultProfile</span></span>
<span data-ttu-id="17ad7-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17ad7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17ad7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="17ad7-119">-Name</span></span>
<span data-ttu-id="17ad7-120">Nome regola</span><span class="sxs-lookup"><span data-stu-id="17ad7-120">Rule Name</span></span>

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

### <span data-ttu-id="17ad7-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17ad7-121">-Namespace</span></span>
<span data-ttu-id="17ad7-122">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17ad7-122">Namespace Name</span></span>

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

### <span data-ttu-id="17ad7-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="17ad7-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="17ad7-124">Azione richiede la pre-elaborazione</span><span class="sxs-lookup"><span data-stu-id="17ad7-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="17ad7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17ad7-125">-ResourceGroupName</span></span>
<span data-ttu-id="17ad7-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="17ad7-126">The name of the resource group</span></span>

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

### <span data-ttu-id="17ad7-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="17ad7-127">-SqlExpression</span></span>
<span data-ttu-id="17ad7-128">Espressione di filtro SQL</span><span class="sxs-lookup"><span data-stu-id="17ad7-128">Sql Filter Expression</span></span>

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

### <span data-ttu-id="17ad7-129">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="17ad7-129">-Subscription</span></span>
<span data-ttu-id="17ad7-130">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="17ad7-130">Subscription Name</span></span>

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

### <span data-ttu-id="17ad7-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="17ad7-131">-Topic</span></span>
<span data-ttu-id="17ad7-132">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="17ad7-132">Topic Name</span></span>

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

### <span data-ttu-id="17ad7-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="17ad7-133">-Confirm</span></span>
<span data-ttu-id="17ad7-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17ad7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17ad7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17ad7-135">-WhatIf</span></span>
<span data-ttu-id="17ad7-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17ad7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17ad7-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17ad7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17ad7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ad7-138">CommonParameters</span></span>
<span data-ttu-id="17ad7-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17ad7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ad7-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17ad7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ad7-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17ad7-141">INPUTS</span></span>

### <span data-ttu-id="17ad7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="17ad7-142">System.String</span></span>

## <span data-ttu-id="17ad7-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17ad7-143">OUTPUTS</span></span>

### <span data-ttu-id="17ad7-144">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="17ad7-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="17ad7-145">Note</span><span class="sxs-lookup"><span data-stu-id="17ad7-145">NOTES</span></span>

## <span data-ttu-id="17ad7-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17ad7-146">RELATED LINKS</span></span>
