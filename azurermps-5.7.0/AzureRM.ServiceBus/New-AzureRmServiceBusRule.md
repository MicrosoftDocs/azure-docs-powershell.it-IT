---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 22e54316bd38907c1ab22e3b2c35e1b6949b0034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686681"
---
# <span data-ttu-id="4b57a-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="4b57a-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="4b57a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b57a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b57a-103">Crea una nuova regola per una determinata sottoscrizione di argomenti.</span><span class="sxs-lookup"><span data-stu-id="4b57a-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b57a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b57a-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b57a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b57a-105">DESCRIPTION</span></span>
<span data-ttu-id="4b57a-106">Il cmdlet **New-AzureRmServiceBusRule** crea una nuova regola per la sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="4b57a-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="4b57a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b57a-107">EXAMPLES</span></span>

### <span data-ttu-id="4b57a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b57a-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="4b57a-109">Il cmdlet New-AzureRmServiceBusRule crea una nuova regola per l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="4b57a-109">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="4b57a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b57a-110">PARAMETERS</span></span>

### <span data-ttu-id="4b57a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b57a-111">-DefaultProfile</span></span>
<span data-ttu-id="4b57a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b57a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b57a-113">-Name</span></span>
<span data-ttu-id="4b57a-114">Nome regola</span><span class="sxs-lookup"><span data-stu-id="4b57a-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b57a-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4b57a-115">-Namespace</span></span>
<span data-ttu-id="4b57a-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4b57a-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b57a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b57a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b57a-118">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4b57a-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b57a-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="4b57a-119">-SqlExpression</span></span>
<span data-ttu-id="4b57a-120">Espressione fillter SQL</span><span class="sxs-lookup"><span data-stu-id="4b57a-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b57a-121">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="4b57a-121">-Subscription</span></span>
<span data-ttu-id="4b57a-122">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="4b57a-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b57a-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="4b57a-123">-Topic</span></span>
<span data-ttu-id="4b57a-124">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="4b57a-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b57a-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b57a-125">-Confirm</span></span>
<span data-ttu-id="4b57a-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b57a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b57a-127">-WhatIf</span></span>
<span data-ttu-id="4b57a-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b57a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b57a-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b57a-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b57a-130">CommonParameters</span></span>
<span data-ttu-id="4b57a-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b57a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b57a-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b57a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b57a-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b57a-133">INPUTS</span></span>

### <span data-ttu-id="4b57a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4b57a-134">System.String</span></span>

## <span data-ttu-id="4b57a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b57a-135">OUTPUTS</span></span>

### <span data-ttu-id="4b57a-136">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="4b57a-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="4b57a-137">Note</span><span class="sxs-lookup"><span data-stu-id="4b57a-137">NOTES</span></span>

## <span data-ttu-id="4b57a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b57a-138">RELATED LINKS</span></span>

