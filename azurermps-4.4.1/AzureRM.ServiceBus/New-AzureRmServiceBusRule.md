---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 39cd0759f18c84f78a2e6a75f8e1c9b257fb9da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688233"
---
# <span data-ttu-id="99c7e-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="99c7e-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="99c7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="99c7e-103">Crea una nuova regola per una determinata sottoscrizione di argomenti.</span><span class="sxs-lookup"><span data-stu-id="99c7e-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99c7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99c7e-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="99c7e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99c7e-105">DESCRIPTION</span></span>
<span data-ttu-id="99c7e-106">Il cmdlet **New-AzureRmServiceBusRule** crea una nuova regola per la sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="99c7e-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="99c7e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99c7e-107">EXAMPLES</span></span>

### <span data-ttu-id="99c7e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99c7e-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="99c7e-109">Il cmdlet **New-AzureRmServiceBusRule** crea una nuova regola per l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="99c7e-109">The **New-AzureRmServiceBusRule** cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="99c7e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99c7e-110">PARAMETERS</span></span>

### <span data-ttu-id="99c7e-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99c7e-111">-Confirm</span></span>
<span data-ttu-id="99c7e-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99c7e-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99c7e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="99c7e-113">-Name</span></span>
<span data-ttu-id="99c7e-114">Nome regola</span><span class="sxs-lookup"><span data-stu-id="99c7e-114">Rule Name</span></span>

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

### <span data-ttu-id="99c7e-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="99c7e-115">-Namespace</span></span>
<span data-ttu-id="99c7e-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="99c7e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="99c7e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99c7e-117">-ResourceGroupName</span></span>
<span data-ttu-id="99c7e-118">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="99c7e-118">The name of the resource group</span></span>

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

### <span data-ttu-id="99c7e-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="99c7e-119">-SqlExpression</span></span>
<span data-ttu-id="99c7e-120">Espressione fillter SQL</span><span class="sxs-lookup"><span data-stu-id="99c7e-120">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="99c7e-121">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="99c7e-121">-Subscription</span></span>
<span data-ttu-id="99c7e-122">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="99c7e-122">Subscription Name</span></span>

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

### <span data-ttu-id="99c7e-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="99c7e-123">-Topic</span></span>
<span data-ttu-id="99c7e-124">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="99c7e-124">Topic Name.</span></span>

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

### <span data-ttu-id="99c7e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99c7e-125">-WhatIf</span></span>
<span data-ttu-id="99c7e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99c7e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99c7e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99c7e-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="99c7e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99c7e-128">INPUTS</span></span>

### <span data-ttu-id="99c7e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="99c7e-129">System.String</span></span>


## <span data-ttu-id="99c7e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99c7e-130">OUTPUTS</span></span>

### <span data-ttu-id="99c7e-131">Microsoft. Azure. Commands. ServiceBus. Models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="99c7e-131">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>


## <span data-ttu-id="99c7e-132">Note</span><span class="sxs-lookup"><span data-stu-id="99c7e-132">NOTES</span></span>

## <span data-ttu-id="99c7e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99c7e-133">RELATED LINKS</span></span>

