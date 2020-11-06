---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 5d3f9212fcaf55d6506723b6c29ed1da0d676bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512984"
---
# <span data-ttu-id="880a3-101">Get-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="880a3-101">Get-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="880a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="880a3-102">SYNOPSIS</span></span>
<span data-ttu-id="880a3-103">Ottiene la descrizione di una regola di autorizzazione specificata per una determinata coda di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="880a3-103">Gets the description of a specified authorization rule for a given Service Bus queue.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="880a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="880a3-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="880a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="880a3-105">DESCRIPTION</span></span>
<span data-ttu-id="880a3-106">Il cmdlet **Get-AzureRmServiceBusQueueAuthorizationRule** ottiene la descrizione di una regola di autorizzazione specificata nella coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="880a3-106">The **Get-AzureRmServiceBusQueueAuthorizationRule** cmdlet gets the description of a specified authorization rule on the given Service Bus queue.</span></span>

## <span data-ttu-id="880a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="880a3-107">EXAMPLES</span></span>

### <span data-ttu-id="880a3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="880a3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="880a3-109">Restituisce la descrizione della regola di autorizzazione specificata per una determinata coda di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="880a3-109">Returns the specified authorization rule description for a given Service Bus queue.</span></span>

## <span data-ttu-id="880a3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="880a3-110">PARAMETERS</span></span>

### <span data-ttu-id="880a3-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="880a3-111">-ResourceGroup</span></span>
<span data-ttu-id="880a3-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="880a3-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="880a3-113">-DefaultProfile</span></span>
<span data-ttu-id="880a3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="880a3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="880a3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="880a3-115">-Name</span></span>
<span data-ttu-id="880a3-116">EventHub AuthorizationRule nome.</span><span class="sxs-lookup"><span data-stu-id="880a3-116">EventHub AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880a3-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="880a3-117">-Namespace</span></span>
<span data-ttu-id="880a3-118">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="880a3-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880a3-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="880a3-119">-Queue</span></span>
<span data-ttu-id="880a3-120">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="880a3-120">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880a3-121">CommonParameters</span></span>
<span data-ttu-id="880a3-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="880a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880a3-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="880a3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880a3-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="880a3-124">INPUTS</span></span>

### <span data-ttu-id="880a3-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="880a3-125">-ResourceGroup</span></span>
 <span data-ttu-id="880a3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="880a3-126">System.String</span></span>
 

### <span data-ttu-id="880a3-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="880a3-127">-NamespaceName</span></span>
 <span data-ttu-id="880a3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="880a3-128">System.String</span></span>
 

### <span data-ttu-id="880a3-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="880a3-129">-QueueName</span></span>
 <span data-ttu-id="880a3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="880a3-130">System.String</span></span>
 

### <span data-ttu-id="880a3-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="880a3-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="880a3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="880a3-132">System.String</span></span>

## <span data-ttu-id="880a3-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="880a3-133">OUTPUTS</span></span>

### <span data-ttu-id="880a3-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="880a3-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="880a3-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onrules/SBAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules Name: SBAuthoRule1 location: West US Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="880a3-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="880a3-136">Note</span><span class="sxs-lookup"><span data-stu-id="880a3-136">NOTES</span></span>

## <span data-ttu-id="880a3-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="880a3-137">RELATED LINKS</span></span>

