---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338848"
---
# <span data-ttu-id="ac877-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ac877-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="ac877-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac877-102">SYNOPSIS</span></span>
<span data-ttu-id="ac877-103">Crea una nuova regola di autorizzazione per lo spazio dei nomi specifico o la coda o l'argomento specificato in bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="ac877-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="ac877-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac877-104">SYNTAX</span></span>

### <span data-ttu-id="ac877-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac877-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac877-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac877-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac877-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac877-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac877-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac877-108">DESCRIPTION</span></span>
<span data-ttu-id="ac877-109">Il cmdlet **New-AzServiceBusAuthorizationRule** crea una nuova regola di autorizzazione per lo spazio dei nomi o la coda o l'argomento di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="ac877-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="ac877-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac877-110">EXAMPLES</span></span>

### <span data-ttu-id="ac877-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac877-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="ac877-112">Crea `AuthoRule1` con i diritti di **ascolto** e **invio** per lo spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="ac877-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="ac877-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ac877-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="ac877-114">Crea `AuthoRule1` con i diritti di **ascolto** e **invio** per la coda `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="ac877-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="ac877-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ac877-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="ac877-116">Crea `AuthoRule1` con i diritti di **ascolto** e **invio** per l'argomento `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="ac877-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="ac877-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac877-117">PARAMETERS</span></span>

### <span data-ttu-id="ac877-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac877-118">-DefaultProfile</span></span>
<span data-ttu-id="ac877-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac877-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac877-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac877-120">-Name</span></span>
<span data-ttu-id="ac877-121">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ac877-121">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac877-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ac877-122">-Namespace</span></span>
<span data-ttu-id="ac877-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ac877-123">Namespace Name</span></span>

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

### <span data-ttu-id="ac877-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="ac877-124">-Queue</span></span>
<span data-ttu-id="ac877-125">Nome coda</span><span class="sxs-lookup"><span data-stu-id="ac877-125">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac877-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac877-126">-ResourceGroupName</span></span>
<span data-ttu-id="ac877-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ac877-127">Resource Group Name</span></span>

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

### <span data-ttu-id="ac877-128">-Diritti</span><span class="sxs-lookup"><span data-stu-id="ac877-128">-Rights</span></span>
<span data-ttu-id="ac877-129">Diritti, ad esempio "ascolta", "Invia", "Gestisci"</span><span class="sxs-lookup"><span data-stu-id="ac877-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac877-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="ac877-130">-Topic</span></span>
<span data-ttu-id="ac877-131">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="ac877-131">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac877-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ac877-132">-Confirm</span></span>
<span data-ttu-id="ac877-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac877-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac877-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac877-134">-WhatIf</span></span>
<span data-ttu-id="ac877-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac877-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac877-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac877-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac877-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac877-137">CommonParameters</span></span>
<span data-ttu-id="ac877-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac877-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac877-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac877-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac877-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac877-140">INPUTS</span></span>

### <span data-ttu-id="ac877-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ac877-141">System.String</span></span>

### <span data-ttu-id="ac877-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="ac877-142">System.String[]</span></span>

## <span data-ttu-id="ac877-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac877-143">OUTPUTS</span></span>

### <span data-ttu-id="ac877-144">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ac877-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ac877-145">Note</span><span class="sxs-lookup"><span data-stu-id="ac877-145">NOTES</span></span>

## <span data-ttu-id="ac877-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac877-146">RELATED LINKS</span></span>
