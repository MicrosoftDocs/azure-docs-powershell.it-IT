---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 603eb1363e15b58a324f7131dd986a7c84371a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685871"
---
# <span data-ttu-id="94dee-101">New-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="94dee-101">New-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="94dee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94dee-102">SYNOPSIS</span></span>
<span data-ttu-id="94dee-103">Crea una nuova regola di autorizzazione per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="94dee-103">Creates a new authorization rule for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94dee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94dee-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94dee-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94dee-105">DESCRIPTION</span></span>
<span data-ttu-id="94dee-106">Il cmdlet **New-AzureRmServiceBusTopicAuthorizationRule** crea una nuova regola di autorizzazione per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="94dee-106">The **New-AzureRmServiceBusTopicAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus topic.</span></span>

## <span data-ttu-id="94dee-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94dee-107">EXAMPLES</span></span>

### <span data-ttu-id="94dee-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94dee-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="94dee-109">Crea una regola `SBTopicAuthoRule1` di autorizzazione con i diritti di **ascolto** e **invio** per l'argomento `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="94dee-109">Creates authorization rule `SBTopicAuthoRule1` with **Listen** and **Send** rights for the topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="94dee-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94dee-110">PARAMETERS</span></span>

### <span data-ttu-id="94dee-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94dee-111">-ResourceGroup</span></span>
<span data-ttu-id="94dee-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94dee-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="94dee-113">-Diritti</span><span class="sxs-lookup"><span data-stu-id="94dee-113">-Rights</span></span>
<span data-ttu-id="94dee-114">I diritti; ad esempio, @ ("Listen", "Send", "Manage")</span><span class="sxs-lookup"><span data-stu-id="94dee-114">The rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94dee-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="94dee-115">-Confirm</span></span>
<span data-ttu-id="94dee-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94dee-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94dee-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94dee-117">-WhatIf</span></span>
<span data-ttu-id="94dee-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94dee-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94dee-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94dee-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94dee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94dee-120">-DefaultProfile</span></span>
<span data-ttu-id="94dee-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94dee-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94dee-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="94dee-122">-Name</span></span>
<span data-ttu-id="94dee-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="94dee-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94dee-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="94dee-124">-Namespace</span></span>
<span data-ttu-id="94dee-125">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="94dee-125">Namespace Name.</span></span>

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

### <span data-ttu-id="94dee-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="94dee-126">-Topic</span></span>
<span data-ttu-id="94dee-127">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="94dee-127">Topic Name.</span></span>

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

### <span data-ttu-id="94dee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94dee-128">CommonParameters</span></span>
<span data-ttu-id="94dee-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94dee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94dee-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94dee-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94dee-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94dee-131">INPUTS</span></span>

### <span data-ttu-id="94dee-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94dee-132">-ResourceGroup</span></span>
 <span data-ttu-id="94dee-133">System. String</span><span class="sxs-lookup"><span data-stu-id="94dee-133">System.String</span></span>
 

### <span data-ttu-id="94dee-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="94dee-134">-NamespaceName</span></span>
 <span data-ttu-id="94dee-135">System. String</span><span class="sxs-lookup"><span data-stu-id="94dee-135">System.String</span></span>
 

### <span data-ttu-id="94dee-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="94dee-136">-TopicName</span></span>
 <span data-ttu-id="94dee-137">System. String</span><span class="sxs-lookup"><span data-stu-id="94dee-137">System.String</span></span>
 

### <span data-ttu-id="94dee-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="94dee-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="94dee-139">System. String</span><span class="sxs-lookup"><span data-stu-id="94dee-139">System.String</span></span>

## <span data-ttu-id="94dee-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94dee-140">OUTPUTS</span></span>

### <span data-ttu-id="94dee-141">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="94dee-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="94dee-142">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onrules/SBTopicAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 location: West US Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="94dee-142">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="94dee-143">Note</span><span class="sxs-lookup"><span data-stu-id="94dee-143">NOTES</span></span>

## <span data-ttu-id="94dee-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94dee-144">RELATED LINKS</span></span>

