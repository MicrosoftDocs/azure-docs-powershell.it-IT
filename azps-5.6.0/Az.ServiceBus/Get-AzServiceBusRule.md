---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0dc9c54b3d2a080d7bb40c8560371b31f4ad3acf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993382"
---
# <span data-ttu-id="26870-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="26870-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="26870-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26870-102">SYNOPSIS</span></span>
<span data-ttu-id="26870-103">Recupera la definizione di una regola esistente in un determinato abbonamento all'argomento.</span><span class="sxs-lookup"><span data-stu-id="26870-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="26870-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26870-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26870-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="26870-105">DESCRIPTION</span></span>
<span data-ttu-id="26870-106">Il cmdlet **Get-AzServiceBusRule** ottiene la descrizione della regola specificata nella sottoscrizione dell'argomento specificata.</span><span class="sxs-lookup"><span data-stu-id="26870-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="26870-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26870-107">EXAMPLES</span></span>

### <span data-ttu-id="26870-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26870-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="26870-109">Restituisce la descrizione della regola specificata per una sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="26870-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="26870-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="26870-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="26870-111">Restituisce un elenco di descrizioni delle regole per una sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="26870-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="26870-112">Per impostazione predefinita, viene restituita una regola 100, se si desidera restituire più di 100 regole, usare il parametro -MaxCount.</span><span class="sxs-lookup"><span data-stu-id="26870-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="26870-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="26870-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="26870-114">Restituisce l'elenco delle prime 150 descrizioni delle regole per un abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="26870-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="26870-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26870-115">PARAMETERS</span></span>

### <span data-ttu-id="26870-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26870-116">-DefaultProfile</span></span>
<span data-ttu-id="26870-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26870-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26870-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="26870-118">-MaxCount</span></span>
<span data-ttu-id="26870-119">Determinare il numero massimo di regole da restituire.</span><span class="sxs-lookup"><span data-stu-id="26870-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="26870-120">-Name</span><span class="sxs-lookup"><span data-stu-id="26870-120">-Name</span></span>
<span data-ttu-id="26870-121">Nome regola</span><span class="sxs-lookup"><span data-stu-id="26870-121">Rule Name</span></span>

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

### <span data-ttu-id="26870-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="26870-122">-Namespace</span></span>
<span data-ttu-id="26870-123">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="26870-123">Namespace Name</span></span>

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

### <span data-ttu-id="26870-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26870-124">-ResourceGroupName</span></span>
<span data-ttu-id="26870-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="26870-125">The name of the resource group</span></span>

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

### <span data-ttu-id="26870-126">-Abbonamento</span><span class="sxs-lookup"><span data-stu-id="26870-126">-Subscription</span></span>
<span data-ttu-id="26870-127">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="26870-127">Subscription Name</span></span>

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

### <span data-ttu-id="26870-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="26870-128">-Topic</span></span>
<span data-ttu-id="26870-129">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="26870-129">Topic Name</span></span>

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

### <span data-ttu-id="26870-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26870-130">CommonParameters</span></span>
<span data-ttu-id="26870-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26870-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26870-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26870-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26870-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="26870-133">INPUTS</span></span>

### <span data-ttu-id="26870-134">System.String</span><span class="sxs-lookup"><span data-stu-id="26870-134">System.String</span></span>

## <span data-ttu-id="26870-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26870-135">OUTPUTS</span></span>

### <span data-ttu-id="26870-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="26870-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="26870-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="26870-137">NOTES</span></span>

## <span data-ttu-id="26870-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26870-138">RELATED LINKS</span></span>
