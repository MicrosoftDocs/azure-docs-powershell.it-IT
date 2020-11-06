---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: e8bcb3688aec6d718c192e4dac4b6b4632eba059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520764"
---
# <span data-ttu-id="57d2b-101">Get-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="57d2b-101">Get-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="57d2b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="57d2b-103">Restituisce la descrizione della descrizione della regola di autorizzazione specificata per l'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="57d2b-103">Returns the description of the specified authorization rule description for the given topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57d2b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57d2b-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57d2b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57d2b-105">DESCRIPTION</span></span>
<span data-ttu-id="57d2b-106">Il cmdlet **Get-AzureRmServiceBusTopicAuthorizationRule** ottiene la descrizione della regola di autorizzazione specificata nell'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="57d2b-106">The **Get-AzureRmServiceBusTopicAuthorizationRule** cmdlet gets the description of the specified authorization rule on the given Service Bus topic.</span></span>

## <span data-ttu-id="57d2b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57d2b-107">EXAMPLES</span></span>

### <span data-ttu-id="57d2b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="57d2b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_example1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="57d2b-109">Restituisce la descrizione della regola di autorizzazione specificata per l'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="57d2b-109">Returns the description of the specified authorization rule for the given topic.</span></span>

## <span data-ttu-id="57d2b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57d2b-110">PARAMETERS</span></span>

### <span data-ttu-id="57d2b-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="57d2b-111">-ResourceGroup</span></span>
<span data-ttu-id="57d2b-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57d2b-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="57d2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d2b-113">-DefaultProfile</span></span>
<span data-ttu-id="57d2b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57d2b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57d2b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="57d2b-115">-Name</span></span>
<span data-ttu-id="57d2b-116">Argomento AuthorizationRule nome.</span><span class="sxs-lookup"><span data-stu-id="57d2b-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="57d2b-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="57d2b-117">-Namespace</span></span>
<span data-ttu-id="57d2b-118">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="57d2b-118">Namespace Name.</span></span>

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

### <span data-ttu-id="57d2b-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="57d2b-119">-Topic</span></span>
<span data-ttu-id="57d2b-120">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="57d2b-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57d2b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d2b-121">CommonParameters</span></span>
<span data-ttu-id="57d2b-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57d2b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d2b-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d2b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d2b-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57d2b-124">INPUTS</span></span>

### <span data-ttu-id="57d2b-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="57d2b-125">-ResourceGroup</span></span>
 <span data-ttu-id="57d2b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="57d2b-126">System.String</span></span>
 

### <span data-ttu-id="57d2b-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="57d2b-127">-NamespaceName</span></span>
 <span data-ttu-id="57d2b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="57d2b-128">System.String</span></span>
 

### <span data-ttu-id="57d2b-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="57d2b-129">-TopicName</span></span>
 <span data-ttu-id="57d2b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="57d2b-130">System.String</span></span>
 

### <span data-ttu-id="57d2b-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="57d2b-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="57d2b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="57d2b-132">System.String</span></span>

## <span data-ttu-id="57d2b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57d2b-133">OUTPUTS</span></span>

### <span data-ttu-id="57d2b-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="57d2b-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="57d2b-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onrules/SBTopicAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 location: West US Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="57d2b-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="57d2b-136">Note</span><span class="sxs-lookup"><span data-stu-id="57d2b-136">NOTES</span></span>

## <span data-ttu-id="57d2b-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57d2b-137">RELATED LINKS</span></span>

