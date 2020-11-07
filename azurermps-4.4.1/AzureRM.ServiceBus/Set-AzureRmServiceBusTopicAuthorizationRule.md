---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: bbc6c0119f0f8f424b508adc38b5de80cd097734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687688"
---
# <span data-ttu-id="e57d6-101">Set-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e57d6-101">Set-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="e57d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e57d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e57d6-103">Aggiorna la descrizione della regola di autorizzazione specificata per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="e57d6-103">Updates the specified authorization rule description for the given Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e57d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e57d6-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e57d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e57d6-105">DESCRIPTION</span></span>
<span data-ttu-id="e57d6-106">Il cmdlet **set-AzureRmServiceBusTopicAuthorizationRule** aggiorna la descrizione per la regola di autorizzazione specificata dell'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="e57d6-106">The **Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus topic.</span></span>

## <span data-ttu-id="e57d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e57d6-107">EXAMPLES</span></span>

### <span data-ttu-id="e57d6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e57d6-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="e57d6-109">Aggiunge **Manage** ai diritti di accesso della regola di autorizzazione `SBTopicAuthoRule1` in argomento `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="e57d6-109">Adds **Manage** to the access rights of the authorization rule `SBTopicAuthoRule1` on topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="e57d6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e57d6-110">PARAMETERS</span></span>

### <span data-ttu-id="e57d6-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e57d6-111">-ResourceGroup</span></span>
<span data-ttu-id="e57d6-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e57d6-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="e57d6-113">-Diritti</span><span class="sxs-lookup"><span data-stu-id="e57d6-113">-Rights</span></span>
<span data-ttu-id="e57d6-114">Diritti ad esempio, @ ("Listen", "Send", "Manage").</span><span class="sxs-lookup"><span data-stu-id="e57d6-114">Rights; for example, @("Listen","Send","Manage").</span></span> <span data-ttu-id="e57d6-115">Obbligatorio se non è specificato **-AuthruleObj** .</span><span class="sxs-lookup"><span data-stu-id="e57d6-115">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57d6-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e57d6-116">-Confirm</span></span>
<span data-ttu-id="e57d6-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e57d6-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57d6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e57d6-118">-WhatIf</span></span>
<span data-ttu-id="e57d6-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e57d6-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e57d6-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e57d6-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57d6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57d6-121">-DefaultProfile</span></span>
<span data-ttu-id="e57d6-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e57d6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e57d6-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="e57d6-123">-InputObj</span></span>
<span data-ttu-id="e57d6-124">Oggetto AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="e57d6-124">ServiceBus Topic AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57d6-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e57d6-125">-Name</span></span>
<span data-ttu-id="e57d6-126">AuthorizationRule nome-obbligatorio se ' AuthruleObj ' non specificato.</span><span class="sxs-lookup"><span data-stu-id="e57d6-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

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

### <span data-ttu-id="e57d6-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e57d6-127">-Namespace</span></span>
<span data-ttu-id="e57d6-128">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e57d6-128">Namespace Name.</span></span>

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

### <span data-ttu-id="e57d6-129">-Topic</span><span class="sxs-lookup"><span data-stu-id="e57d6-129">-Topic</span></span>
<span data-ttu-id="e57d6-130">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="e57d6-130">Topic Name.</span></span>

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

### <span data-ttu-id="e57d6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57d6-131">CommonParameters</span></span>
<span data-ttu-id="e57d6-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e57d6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57d6-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e57d6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57d6-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e57d6-134">INPUTS</span></span>

### <span data-ttu-id="e57d6-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e57d6-135">-ResourceGroup</span></span>
 <span data-ttu-id="e57d6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e57d6-136">System.String</span></span>

### <span data-ttu-id="e57d6-137">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e57d6-137">-NamespaceName</span></span>
 <span data-ttu-id="e57d6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e57d6-138">System.String</span></span>

### <span data-ttu-id="e57d6-139">-TopicName</span><span class="sxs-lookup"><span data-stu-id="e57d6-139">-TopicName</span></span>
 <span data-ttu-id="e57d6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e57d6-140">System.String</span></span>

### <span data-ttu-id="e57d6-141">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="e57d6-141">-AuthRuleObj</span></span>
 <span data-ttu-id="e57d6-142">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e57d6-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e57d6-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e57d6-143">OUTPUTS</span></span>

### <span data-ttu-id="e57d6-144">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e57d6-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="e57d6-145">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/Authorization Rules/SBTopicAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 location: West US Tags: Rights: {Listen, Send, Manage}</span><span class="sxs-lookup"><span data-stu-id="e57d6-145">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization Rules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send, Manage}</span></span>

## <span data-ttu-id="e57d6-146">Note</span><span class="sxs-lookup"><span data-stu-id="e57d6-146">NOTES</span></span>

## <span data-ttu-id="e57d6-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e57d6-147">RELATED LINKS</span></span>

