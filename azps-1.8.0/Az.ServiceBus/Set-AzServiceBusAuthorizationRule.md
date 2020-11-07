---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e9ab4d4d2fb2c60561d85582f2dda922ba9eaae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677111"
---
# <span data-ttu-id="084d8-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="084d8-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="084d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="084d8-102">SYNOPSIS</span></span>
<span data-ttu-id="084d8-103">Aggiorna la descrizione della regola di autorizzazione specificata per lo spazio dei nomi o la coda o l'argomento di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="084d8-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="084d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="084d8-104">SYNTAX</span></span>

### <span data-ttu-id="084d8-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="084d8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="084d8-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="084d8-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="084d8-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="084d8-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="084d8-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="084d8-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="084d8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="084d8-109">DESCRIPTION</span></span>
<span data-ttu-id="084d8-110">Il cmdlet **set-AzServiceBusAuthorizationRule** aggiorna la descrizione della regola di autorizzazione specificata nello spazio dei nomi o in una coda o un argomento di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="084d8-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="084d8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="084d8-111">EXAMPLES</span></span>

### <span data-ttu-id="084d8-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="084d8-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="084d8-113">Rimuove **Manage** dai diritti di accesso della regola di autorizzazione `AuthoRule1` nello spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="084d8-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="084d8-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="084d8-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="084d8-115">Rimuove **Manage** dai diritti di accesso della regola di autorizzazione `AuthoRule1` in coda `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="084d8-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="084d8-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="084d8-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="084d8-117">Rimuove **Manage** dai diritti di accesso della regola di autorizzazione `AuthoRule1` nell'argomento `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="084d8-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="084d8-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="084d8-118">PARAMETERS</span></span>

### <span data-ttu-id="084d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084d8-119">-DefaultProfile</span></span>
<span data-ttu-id="084d8-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="084d8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="084d8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="084d8-121">-InputObject</span></span>
<span data-ttu-id="084d8-122">Oggetto AuthorizationRule di ServiceBus</span><span class="sxs-lookup"><span data-stu-id="084d8-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="084d8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="084d8-123">-Name</span></span>
<span data-ttu-id="084d8-124">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="084d8-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="084d8-125">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="084d8-125">-Namespace</span></span>
<span data-ttu-id="084d8-126">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="084d8-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="084d8-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="084d8-127">-Queue</span></span>
<span data-ttu-id="084d8-128">Nome coda</span><span class="sxs-lookup"><span data-stu-id="084d8-128">Queue Name</span></span>

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

### <span data-ttu-id="084d8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="084d8-129">-ResourceGroupName</span></span>
<span data-ttu-id="084d8-130">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="084d8-130">Resource Group Name</span></span>

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

### <span data-ttu-id="084d8-131">-Diritti</span><span class="sxs-lookup"><span data-stu-id="084d8-131">-Rights</span></span>
<span data-ttu-id="084d8-132">Diritti, ad esempio @ ("ascolta", "Invia", "Gestisci")</span><span class="sxs-lookup"><span data-stu-id="084d8-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="084d8-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="084d8-133">-Topic</span></span>
<span data-ttu-id="084d8-134">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="084d8-134">Topic Name</span></span>

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

### <span data-ttu-id="084d8-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="084d8-135">-Confirm</span></span>
<span data-ttu-id="084d8-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="084d8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="084d8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084d8-137">-WhatIf</span></span>
<span data-ttu-id="084d8-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="084d8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="084d8-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="084d8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="084d8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084d8-140">CommonParameters</span></span>
<span data-ttu-id="084d8-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="084d8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084d8-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="084d8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084d8-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="084d8-143">INPUTS</span></span>

### <span data-ttu-id="084d8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="084d8-144">System.String</span></span>

### <span data-ttu-id="084d8-145">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="084d8-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="084d8-146">System. String []</span><span class="sxs-lookup"><span data-stu-id="084d8-146">System.String[]</span></span>

## <span data-ttu-id="084d8-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="084d8-147">OUTPUTS</span></span>

### <span data-ttu-id="084d8-148">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="084d8-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="084d8-149">Note</span><span class="sxs-lookup"><span data-stu-id="084d8-149">NOTES</span></span>

## <span data-ttu-id="084d8-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="084d8-150">RELATED LINKS</span></span>
