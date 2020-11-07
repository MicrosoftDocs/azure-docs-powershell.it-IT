---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 2b4ddf625e5565de0d345a5477d3ba368dcb186b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687263"
---
# <span data-ttu-id="2acf5-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2acf5-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="2acf5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2acf5-102">SYNOPSIS</span></span>
<span data-ttu-id="2acf5-103">Aggiorna la descrizione della regola di autorizzazione specificata per lo spazio dei nomi o la coda o l'argomento di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="2acf5-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2acf5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2acf5-104">SYNTAX</span></span>

### <span data-ttu-id="2acf5-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2acf5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2acf5-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2acf5-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2acf5-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2acf5-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2acf5-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2acf5-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2acf5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2acf5-109">DESCRIPTION</span></span>
<span data-ttu-id="2acf5-110">Il cmdlet **set-AzureRmServiceBusAuthorizationRule** aggiorna la descrizione della regola di autorizzazione specificata nello spazio dei nomi o in una coda o un argomento di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="2acf5-110">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="2acf5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2acf5-111">EXAMPLES</span></span>

### <span data-ttu-id="2acf5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2acf5-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="2acf5-113">Rimuove **Manage** dai diritti di accesso della regola di autorizzazione `AuthoRule1` nello spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="2acf5-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="2acf5-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2acf5-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="2acf5-115">Rimuove **Manage** dai diritti di accesso della regola di autorizzazione `AuthoRule1` in coda `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="2acf5-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="2acf5-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2acf5-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="2acf5-117">Rimuove **Manage** dai diritti di accesso della regola di autorizzazione `AuthoRule1` nell'argomento `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="2acf5-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="2acf5-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2acf5-118">PARAMETERS</span></span>

### <span data-ttu-id="2acf5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2acf5-119">-DefaultProfile</span></span>
<span data-ttu-id="2acf5-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2acf5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2acf5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2acf5-121">-InputObject</span></span>
<span data-ttu-id="2acf5-122">Oggetto AuthorizationRule di ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2acf5-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="2acf5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2acf5-123">-Name</span></span>
<span data-ttu-id="2acf5-124">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2acf5-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="2acf5-125">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2acf5-125">-Namespace</span></span>
<span data-ttu-id="2acf5-126">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2acf5-126">Namespace Name</span></span>

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

### <span data-ttu-id="2acf5-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="2acf5-127">-Queue</span></span>
<span data-ttu-id="2acf5-128">Nome coda</span><span class="sxs-lookup"><span data-stu-id="2acf5-128">Queue Name</span></span>

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

### <span data-ttu-id="2acf5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2acf5-129">-ResourceGroupName</span></span>
<span data-ttu-id="2acf5-130">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="2acf5-130">Resource Group Name</span></span>

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

### <span data-ttu-id="2acf5-131">-Diritti</span><span class="sxs-lookup"><span data-stu-id="2acf5-131">-Rights</span></span>
<span data-ttu-id="2acf5-132">Diritti, ad esempio @ ("ascolta", "Invia", "Gestisci")</span><span class="sxs-lookup"><span data-stu-id="2acf5-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="2acf5-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="2acf5-133">-Topic</span></span>
<span data-ttu-id="2acf5-134">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="2acf5-134">Topic Name</span></span>

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

### <span data-ttu-id="2acf5-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2acf5-135">-Confirm</span></span>
<span data-ttu-id="2acf5-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2acf5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2acf5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2acf5-137">-WhatIf</span></span>
<span data-ttu-id="2acf5-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2acf5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2acf5-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2acf5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2acf5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2acf5-140">CommonParameters</span></span>
<span data-ttu-id="2acf5-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2acf5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2acf5-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2acf5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2acf5-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2acf5-143">INPUTS</span></span>

### <span data-ttu-id="2acf5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2acf5-144">System.String</span></span>

### <span data-ttu-id="2acf5-145">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2acf5-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="2acf5-146">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2acf5-146">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2acf5-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="2acf5-147">System.String[]</span></span>

## <span data-ttu-id="2acf5-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2acf5-148">OUTPUTS</span></span>

### <span data-ttu-id="2acf5-149">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2acf5-149">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2acf5-150">Note</span><span class="sxs-lookup"><span data-stu-id="2acf5-150">NOTES</span></span>

## <span data-ttu-id="2acf5-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2acf5-151">RELATED LINKS</span></span>
