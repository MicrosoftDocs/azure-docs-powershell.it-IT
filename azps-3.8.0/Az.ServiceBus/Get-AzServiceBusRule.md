---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: f4899d55919f8b3c08b36babc448f1594f4ac4c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021693"
---
# <span data-ttu-id="9f8cc-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="9f8cc-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="9f8cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f8cc-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8cc-103">Crea una nuova regola per una determinata sottoscrizione di argomenti.</span><span class="sxs-lookup"><span data-stu-id="9f8cc-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="9f8cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f8cc-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f8cc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f8cc-105">DESCRIPTION</span></span>
<span data-ttu-id="9f8cc-106">Il cmdlet **Get-AzServiceBusRule** ottiene la descrizione della regola specificata nell'abbonamento specificato di topic.</span><span class="sxs-lookup"><span data-stu-id="9f8cc-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="9f8cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f8cc-107">EXAMPLES</span></span>

### <span data-ttu-id="9f8cc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9f8cc-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="9f8cc-109">Restituisce la descrizione della regola specificata per un abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="9f8cc-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="9f8cc-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9f8cc-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="9f8cc-111">Restituisce un elenco di descrizioni delle regole per un abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="9f8cc-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="9f8cc-112">Per impostazione predefinita verrà restituita la regola 100, se più di 100 regola da restituire, usare il parametro-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="9f8cc-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="9f8cc-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9f8cc-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="9f8cc-114">Restituisce l'elenco delle prime descrizioni delle regole di 150 per un abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="9f8cc-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="9f8cc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f8cc-115">PARAMETERS</span></span>

### <span data-ttu-id="9f8cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f8cc-116">-DefaultProfile</span></span>
<span data-ttu-id="9f8cc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f8cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f8cc-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9f8cc-118">-MaxCount</span></span>
<span data-ttu-id="9f8cc-119">Determinare il numero massimo di regole da restituire.</span><span class="sxs-lookup"><span data-stu-id="9f8cc-119">Determine the maximum number of Rules to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f8cc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f8cc-120">-Name</span></span>
<span data-ttu-id="9f8cc-121">Nome regola</span><span class="sxs-lookup"><span data-stu-id="9f8cc-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f8cc-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f8cc-122">-Namespace</span></span>
<span data-ttu-id="9f8cc-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f8cc-123">Namespace Name</span></span>

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

### <span data-ttu-id="9f8cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f8cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="9f8cc-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9f8cc-125">The name of the resource group</span></span>

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

### <span data-ttu-id="9f8cc-126">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="9f8cc-126">-Subscription</span></span>
<span data-ttu-id="9f8cc-127">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="9f8cc-127">Subscription Name</span></span>

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

### <span data-ttu-id="9f8cc-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="9f8cc-128">-Topic</span></span>
<span data-ttu-id="9f8cc-129">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="9f8cc-129">Topic Name</span></span>

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

### <span data-ttu-id="9f8cc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8cc-130">CommonParameters</span></span>
<span data-ttu-id="9f8cc-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f8cc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8cc-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f8cc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8cc-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f8cc-133">INPUTS</span></span>

### <span data-ttu-id="9f8cc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9f8cc-134">System.String</span></span>

## <span data-ttu-id="9f8cc-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f8cc-135">OUTPUTS</span></span>

### <span data-ttu-id="9f8cc-136">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="9f8cc-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="9f8cc-137">Note</span><span class="sxs-lookup"><span data-stu-id="9f8cc-137">NOTES</span></span>

## <span data-ttu-id="9f8cc-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f8cc-138">RELATED LINKS</span></span>
