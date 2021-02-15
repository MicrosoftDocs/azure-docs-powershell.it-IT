---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: da981d38f0833adc276a114c42def5d19322e0d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197854"
---
# <span data-ttu-id="fa245-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fa245-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="fa245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa245-102">SYNOPSIS</span></span>
<span data-ttu-id="fa245-103">Aggiorna la descrizione della regola di autorizzazione specificata per lo spazio dei nomi o la coda o l'argomento del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="fa245-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="fa245-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa245-104">SYNTAX</span></span>

### <span data-ttu-id="fa245-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa245-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa245-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa245-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa245-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa245-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa245-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa245-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa245-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fa245-109">DESCRIPTION</span></span>
<span data-ttu-id="fa245-110">Il cmdlet **Set-AzServiceBusAuthorizationRule** aggiorna la descrizione della regola di autorizzazione specificata nello spazio dei nomi o nell'argomento specificato per i bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="fa245-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="fa245-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa245-111">EXAMPLES</span></span>

### <span data-ttu-id="fa245-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fa245-112">Example 1</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="fa245-113">Rimuove **Gestisci dai** diritti di accesso della regola di autorizzazione nello spazio dei `AuthoRule1` `SB-Example1` nomi.</span><span class="sxs-lookup"><span data-stu-id="fa245-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="fa245-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fa245-114">Example 2</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="fa245-115">Rimuove **Gestisci dai** diritti di accesso della regola di autorizzazione in `AuthoRule1` `SBQueue` coda.</span><span class="sxs-lookup"><span data-stu-id="fa245-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="fa245-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="fa245-116">Example 3</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="fa245-117">Rimuove **Gestisci dai** diritti di accesso della regola di autorizzazione `AuthoRule1` nell'argomento. `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="fa245-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="fa245-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa245-118">PARAMETERS</span></span>

### <span data-ttu-id="fa245-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa245-119">-DefaultProfile</span></span>
<span data-ttu-id="fa245-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa245-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa245-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa245-121">-InputObject</span></span>
<span data-ttu-id="fa245-122">Oggetto ServiceBus AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fa245-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="fa245-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fa245-123">-Name</span></span>
<span data-ttu-id="fa245-124">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="fa245-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="fa245-125">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fa245-125">-Namespace</span></span>
<span data-ttu-id="fa245-126">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fa245-126">Namespace Name</span></span>

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

### <span data-ttu-id="fa245-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="fa245-127">-Queue</span></span>
<span data-ttu-id="fa245-128">Nome coda</span><span class="sxs-lookup"><span data-stu-id="fa245-128">Queue Name</span></span>

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

### <span data-ttu-id="fa245-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa245-129">-ResourceGroupName</span></span>
<span data-ttu-id="fa245-130">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fa245-130">Resource Group Name</span></span>

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

### <span data-ttu-id="fa245-131">-Rights</span><span class="sxs-lookup"><span data-stu-id="fa245-131">-Rights</span></span>
<span data-ttu-id="fa245-132">Diritti, ad esempio @("Ascoltare","Invia","Gestisci")</span><span class="sxs-lookup"><span data-stu-id="fa245-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="fa245-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="fa245-133">-Topic</span></span>
<span data-ttu-id="fa245-134">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="fa245-134">Topic Name</span></span>

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

### <span data-ttu-id="fa245-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa245-135">-Confirm</span></span>
<span data-ttu-id="fa245-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa245-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa245-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa245-137">-WhatIf</span></span>
<span data-ttu-id="fa245-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa245-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa245-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa245-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa245-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa245-140">CommonParameters</span></span>
<span data-ttu-id="fa245-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa245-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa245-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa245-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa245-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="fa245-143">INPUTS</span></span>

### <span data-ttu-id="fa245-144">System.String</span><span class="sxs-lookup"><span data-stu-id="fa245-144">System.String</span></span>

### <span data-ttu-id="fa245-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fa245-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="fa245-146">System.String[]</span><span class="sxs-lookup"><span data-stu-id="fa245-146">System.String[]</span></span>

## <span data-ttu-id="fa245-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa245-147">OUTPUTS</span></span>

### <span data-ttu-id="fa245-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fa245-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="fa245-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="fa245-149">NOTES</span></span>

## <span data-ttu-id="fa245-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa245-150">RELATED LINKS</span></span>
