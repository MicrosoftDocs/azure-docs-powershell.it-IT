---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: ef71b8ce2f90fb6275c3bd658289f4e32579cd69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004157"
---
# <span data-ttu-id="acbf8-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="acbf8-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="acbf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acbf8-102">SYNOPSIS</span></span>
<span data-ttu-id="acbf8-103">Aggiorna la regola di autorizzazione specificata in un hub eventi.</span><span class="sxs-lookup"><span data-stu-id="acbf8-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="acbf8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acbf8-104">SYNTAX</span></span>

### <span data-ttu-id="acbf8-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="acbf8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acbf8-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="acbf8-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acbf8-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="acbf8-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acbf8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="acbf8-108">DESCRIPTION</span></span>
<span data-ttu-id="acbf8-109">Il Set-AzEventHubAuthorizationRule cmdlet aggiorna la regola di autorizzazione specificata nell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="acbf8-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="acbf8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acbf8-110">EXAMPLES</span></span>

### <span data-ttu-id="acbf8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="acbf8-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="acbf8-112">Aggiorna la regola di autorizzazione MyAuthRuleName per concedere i diritti di gestione per \` l'hub eventi MyEventHubName, con ambito dallo spazio dei nomi \` \` \` \` MyAuthName. \`</span><span class="sxs-lookup"><span data-stu-id="acbf8-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="acbf8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acbf8-113">PARAMETERS</span></span>

### <span data-ttu-id="acbf8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbf8-114">-DefaultProfile</span></span>
<span data-ttu-id="acbf8-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acbf8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acbf8-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="acbf8-116">-EventHub</span></span>
<span data-ttu-id="acbf8-117">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="acbf8-117">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbf8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acbf8-118">-InputObject</span></span>
<span data-ttu-id="acbf8-119">Oggetto AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="acbf8-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acbf8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="acbf8-120">-Name</span></span>
<span data-ttu-id="acbf8-121">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="acbf8-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="acbf8-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="acbf8-122">-Namespace</span></span>
<span data-ttu-id="acbf8-123">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="acbf8-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbf8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acbf8-124">-ResourceGroupName</span></span>
<span data-ttu-id="acbf8-125">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="acbf8-125">Resource Group Name</span></span>

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

### <span data-ttu-id="acbf8-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="acbf8-126">-Rights</span></span>
<span data-ttu-id="acbf8-127">Diritti, ad esempio @("Ascoltare","Invia","Gestisci")</span><span class="sxs-lookup"><span data-stu-id="acbf8-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbf8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acbf8-128">-Confirm</span></span>
<span data-ttu-id="acbf8-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acbf8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acbf8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acbf8-130">-WhatIf</span></span>
<span data-ttu-id="acbf8-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acbf8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acbf8-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acbf8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acbf8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbf8-133">CommonParameters</span></span>
<span data-ttu-id="acbf8-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acbf8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbf8-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acbf8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbf8-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="acbf8-136">INPUTS</span></span>

### <span data-ttu-id="acbf8-137">System.String</span><span class="sxs-lookup"><span data-stu-id="acbf8-137">System.String</span></span>

### <span data-ttu-id="acbf8-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="acbf8-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="acbf8-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="acbf8-139">System.String[]</span></span>

## <span data-ttu-id="acbf8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acbf8-140">OUTPUTS</span></span>

### <span data-ttu-id="acbf8-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="acbf8-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="acbf8-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="acbf8-142">NOTES</span></span>

## <span data-ttu-id="acbf8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acbf8-143">RELATED LINKS</span></span>
