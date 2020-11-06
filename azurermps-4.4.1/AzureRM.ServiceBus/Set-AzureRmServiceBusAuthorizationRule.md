---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 9e4612f8b688181ca54c7fa8414d28e3a444b446
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521138"
---
# <span data-ttu-id="a0974-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a0974-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="a0974-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0974-102">SYNOPSIS</span></span>
<span data-ttu-id="a0974-103">Aggiorna la descrizione della regola di autorizzazione specificata per lo spazio dei nomi o la coda o l'argomento di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="a0974-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0974-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0974-104">SYNTAX</span></span>

### <span data-ttu-id="a0974-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0974-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0974-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a0974-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0974-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a0974-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0974-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a0974-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0974-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="a0974-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0974-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0974-110">DESCRIPTION</span></span>
<span data-ttu-id="a0974-111">Il cmdlet **set-AzureRmServiceBusAuthorizationRule** aggiorna la descrizione della regola di autorizzazione specificata nello spazio dei nomi o in una coda o un argomento di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="a0974-111">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="a0974-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0974-112">EXAMPLES</span></span>

### <span data-ttu-id="a0974-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0974-113">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="a0974-114">Rimuove **Manage** dai diritti di accesso della regola di autorizzazione `AuthoRule1` nello spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="a0974-114">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="a0974-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a0974-115">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="a0974-116">Rimuove **Manage** dai diritti di accesso della regola di autorizzazione `AuthoRule1` in coda `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="a0974-116">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="a0974-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a0974-117">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="a0974-118">Rimuove **Manage** dai diritti di accesso della regola di autorizzazione `AuthoRule1` nell'argomento `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="a0974-118">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="a0974-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0974-119">PARAMETERS</span></span>

### <span data-ttu-id="a0974-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0974-120">-Confirm</span></span>
<span data-ttu-id="a0974-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0974-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0974-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0974-122">-InputObject</span></span>
<span data-ttu-id="a0974-123">Oggetto AuthorizationRule di ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="a0974-123">ServiceBus AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0974-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0974-124">-Name</span></span>
<span data-ttu-id="a0974-125">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a0974-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="a0974-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a0974-126">-Namespace</span></span>
<span data-ttu-id="a0974-127">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a0974-127">Namespace Name.</span></span>

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

### <span data-ttu-id="a0974-128">-Queue</span><span class="sxs-lookup"><span data-stu-id="a0974-128">-Queue</span></span>
<span data-ttu-id="a0974-129">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="a0974-129">Queue Name.</span></span>

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

### <span data-ttu-id="a0974-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0974-130">-ResourceGroupName</span></span>
<span data-ttu-id="a0974-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a0974-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="a0974-132">-Diritti</span><span class="sxs-lookup"><span data-stu-id="a0974-132">-Rights</span></span>
<span data-ttu-id="a0974-133">Diritti, ad esempio @ ("ascolta", "Invia", "Gestisci")</span><span class="sxs-lookup"><span data-stu-id="a0974-133">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0974-134">-Topic</span><span class="sxs-lookup"><span data-stu-id="a0974-134">-Topic</span></span>
<span data-ttu-id="a0974-135">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="a0974-135">Topic Name.</span></span>

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

### <span data-ttu-id="a0974-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0974-136">-WhatIf</span></span>
<span data-ttu-id="a0974-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0974-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0974-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0974-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0974-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0974-139">-DefaultProfile</span></span>
<span data-ttu-id="a0974-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0974-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0974-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0974-141">CommonParameters</span></span>
<span data-ttu-id="a0974-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0974-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0974-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0974-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0974-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0974-144">INPUTS</span></span>

### <span data-ttu-id="a0974-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a0974-145">System.String</span></span>
<span data-ttu-id="a0974-146">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="a0974-146">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes System.String[]</span></span>

## <span data-ttu-id="a0974-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0974-147">OUTPUTS</span></span>

### <span data-ttu-id="a0974-148">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a0974-148">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a0974-149">Note</span><span class="sxs-lookup"><span data-stu-id="a0974-149">NOTES</span></span>

## <span data-ttu-id="a0974-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0974-150">RELATED LINKS</span></span>

