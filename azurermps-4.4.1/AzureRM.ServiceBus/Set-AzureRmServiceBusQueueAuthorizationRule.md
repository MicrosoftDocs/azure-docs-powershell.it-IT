---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 166b47a231b2ca6fc2cf74137212e60123f25445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521132"
---
# <span data-ttu-id="091f9-101">Set-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="091f9-101">Set-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="091f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="091f9-102">SYNOPSIS</span></span>
<span data-ttu-id="091f9-103">Aggiorna la descrizione della regola di autorizzazione specificata per la coda di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="091f9-103">Updates the specified authorization rule description for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="091f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="091f9-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> [-NamespaceName] <String>
 [-QueueName] <String> [-AuthRuleObj] <SharedAccessAuthorizationRuleAttributes>
 [[-AuthorizationRuleName] <String>] [[-Rights] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="091f9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="091f9-105">DESCRIPTION</span></span>
<span data-ttu-id="091f9-106">Il cmdlet **set-AzureRmServiceBusQueueAuthorizationRule** aggiorna la descrizione per la regola di autorizzazione specificata della coda di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="091f9-106">The **Set-AzureRmServiceBusQueueAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus queue.</span></span>

## <span data-ttu-id="091f9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="091f9-107">EXAMPLES</span></span>

### <span data-ttu-id="091f9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="091f9-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="091f9-109">Aggiunge **Manage** ai diritti di accesso della regola `SBAuthoRule1` di autorizzazione della coda `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="091f9-109">Adds **Manage** to the access rights of the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="091f9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="091f9-110">PARAMETERS</span></span>

### <span data-ttu-id="091f9-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="091f9-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="091f9-112">Nome della regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="091f9-112">The authorization rule name.</span></span> <span data-ttu-id="091f9-113">Obbligatorio se non è specificato **-AuthruleObj** .</span><span class="sxs-lookup"><span data-stu-id="091f9-113">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="091f9-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="091f9-114">-AuthRuleObj</span></span>
<span data-ttu-id="091f9-115">Oggetto regola di autorizzazione coda bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="091f9-115">The Service Bus queue authorization rule object.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="091f9-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="091f9-116">-NamespaceName</span></span>
<span data-ttu-id="091f9-117">Nome dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="091f9-117">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="091f9-118">-QueueName</span><span class="sxs-lookup"><span data-stu-id="091f9-118">-QueueName</span></span>
<span data-ttu-id="091f9-119">Nome della coda di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="091f9-119">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="091f9-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="091f9-120">-ResourceGroup</span></span>
<span data-ttu-id="091f9-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="091f9-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="091f9-122">-Diritti</span><span class="sxs-lookup"><span data-stu-id="091f9-122">-Rights</span></span>
<span data-ttu-id="091f9-123">I diritti; ad esempio @ ("Listen", "Send", "Manage").</span><span class="sxs-lookup"><span data-stu-id="091f9-123">The rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="091f9-124">Obbligatorio se "AuthruleObj" non è specificato.</span><span class="sxs-lookup"><span data-stu-id="091f9-124">Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="091f9-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="091f9-125">-Confirm</span></span>
<span data-ttu-id="091f9-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="091f9-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091f9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="091f9-127">-WhatIf</span></span>
<span data-ttu-id="091f9-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="091f9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="091f9-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="091f9-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091f9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="091f9-130">CommonParameters</span></span>
<span data-ttu-id="091f9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="091f9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="091f9-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="091f9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="091f9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="091f9-133">INPUTS</span></span>

### <span data-ttu-id="091f9-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="091f9-134">-ResourceGroup</span></span>
 <span data-ttu-id="091f9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="091f9-135">System.String</span></span>

### <span data-ttu-id="091f9-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="091f9-136">-NamespaceName</span></span>
 <span data-ttu-id="091f9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="091f9-137">System.String</span></span>

### <span data-ttu-id="091f9-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="091f9-138">-QueueName</span></span>
 <span data-ttu-id="091f9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="091f9-139">System.String</span></span>

### <span data-ttu-id="091f9-140">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="091f9-140">-AuthRuleObj</span></span>
 <span data-ttu-id="091f9-141">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="091f9-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="091f9-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="091f9-142">OUTPUTS</span></span>

### <span data-ttu-id="091f9-143">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="091f9-143">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="091f9-144">Note</span><span class="sxs-lookup"><span data-stu-id="091f9-144">NOTES</span></span>

## <span data-ttu-id="091f9-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="091f9-145">RELATED LINKS</span></span>

