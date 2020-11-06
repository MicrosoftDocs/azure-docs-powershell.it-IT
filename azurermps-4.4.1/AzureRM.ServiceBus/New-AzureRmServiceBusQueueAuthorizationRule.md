---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 098c61be4eaf405d3c3a031601b48f20de1e234a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510316"
---
# <span data-ttu-id="99ec3-101">New-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="99ec3-101">New-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="99ec3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="99ec3-103">Crea una nuova regola di autorizzazione per la coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="99ec3-103">Creates a new authorization rule for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99ec3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99ec3-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99ec3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="99ec3-106">Il cmdlet **New-AzureRmServiceBusQueueAuthorizationRule** crea una nuova regola di autorizzazione per la coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="99ec3-106">The **New-AzureRmServiceBusQueueAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus queue.</span></span>

## <span data-ttu-id="99ec3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99ec3-107">EXAMPLES</span></span>

### <span data-ttu-id="99ec3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99ec3-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="99ec3-109">Crea una regola `SBAuthoRule1` di autorizzazione con i diritti di **ascolto e invio** per la coda `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="99ec3-109">Creates authorization rule `SBAuthoRule1` with **Listen and Send** rights for the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="99ec3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99ec3-110">PARAMETERS</span></span>

### <span data-ttu-id="99ec3-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99ec3-111">-ResourceGroup</span></span>
<span data-ttu-id="99ec3-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99ec3-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="99ec3-113">-Diritti</span><span class="sxs-lookup"><span data-stu-id="99ec3-113">-Rights</span></span>
<span data-ttu-id="99ec3-114">Specifica i diritti; Per esempio</span><span class="sxs-lookup"><span data-stu-id="99ec3-114">Specifies the rights; for example,</span></span>  
<span data-ttu-id="99ec3-115">@ ("Ascolta", "Invia", "Gestisci")</span><span class="sxs-lookup"><span data-stu-id="99ec3-115">@("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="99ec3-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99ec3-116">-Confirm</span></span>
<span data-ttu-id="99ec3-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99ec3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99ec3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99ec3-118">-WhatIf</span></span>
<span data-ttu-id="99ec3-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99ec3-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ec3-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99ec3-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99ec3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ec3-121">-DefaultProfile</span></span>
<span data-ttu-id="99ec3-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99ec3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99ec3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="99ec3-123">-Name</span></span>
<span data-ttu-id="99ec3-124">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="99ec3-124">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="99ec3-125">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="99ec3-125">-Namespace</span></span>
<span data-ttu-id="99ec3-126">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="99ec3-126">Namespace Name.</span></span>

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

### <span data-ttu-id="99ec3-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="99ec3-127">-Queue</span></span>
<span data-ttu-id="99ec3-128">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="99ec3-128">Queue Name.</span></span>

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

### <span data-ttu-id="99ec3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ec3-129">CommonParameters</span></span>
<span data-ttu-id="99ec3-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ec3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ec3-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99ec3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ec3-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99ec3-132">INPUTS</span></span>

### <span data-ttu-id="99ec3-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99ec3-133">-ResourceGroup</span></span>
 <span data-ttu-id="99ec3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="99ec3-134">System.String</span></span>
 

### <span data-ttu-id="99ec3-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="99ec3-135">-NamespaceName</span></span>
 <span data-ttu-id="99ec3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="99ec3-136">System.String</span></span>
 

### <span data-ttu-id="99ec3-137">-QueueName</span><span class="sxs-lookup"><span data-stu-id="99ec3-137">-QueueName</span></span>
 <span data-ttu-id="99ec3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="99ec3-138">System.String</span></span>
 

### <span data-ttu-id="99ec3-139">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="99ec3-139">-AuthorizationRuleName</span></span>
 <span data-ttu-id="99ec3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="99ec3-140">System.String</span></span>

## <span data-ttu-id="99ec3-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99ec3-141">OUTPUTS</span></span>

### <span data-ttu-id="99ec3-142">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="99ec3-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="99ec3-143">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onrules/SBAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules Name: SBAuthoRule1 location: West US Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="99ec3-143">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="99ec3-144">Note</span><span class="sxs-lookup"><span data-stu-id="99ec3-144">NOTES</span></span>

## <span data-ttu-id="99ec3-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99ec3-145">RELATED LINKS</span></span>

