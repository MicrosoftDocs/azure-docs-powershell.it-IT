---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: fde71fed26c074efa705d0b1dc181dfb46bae44e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957150"
---
# <span data-ttu-id="473dd-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="473dd-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="473dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="473dd-102">SYNOPSIS</span></span>
<span data-ttu-id="473dd-103">Crea una nuova regola di autorizzazione Hub eventi per lo spazio dei nomi o eventhub.</span><span class="sxs-lookup"><span data-stu-id="473dd-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="473dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="473dd-104">SYNTAX</span></span>

### <span data-ttu-id="473dd-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="473dd-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="473dd-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="473dd-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="473dd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="473dd-107">DESCRIPTION</span></span>
<span data-ttu-id="473dd-108">Il cmdlet New-AzEventHubAuthorizationRule crea una nuova regola di autorizzazione Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="473dd-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="473dd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="473dd-109">EXAMPLES</span></span>

### <span data-ttu-id="473dd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="473dd-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="473dd-111">Crea una regola di autorizzazione MyAuthRuleName concedendo i diritti di ascolto e invio allo spazio dei nomi MyResourceName, con il gruppo di \` \` risorse \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="473dd-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="473dd-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="473dd-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="473dd-113">Crea una regola di autorizzazione MyAuthRuleName concedendo i diritti di ascolto e invio all'hub eventi MyEventHubName nello spazio dei nomi MyResourceName, con il gruppo di \` \` risorse \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="473dd-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="473dd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="473dd-114">PARAMETERS</span></span>

### <span data-ttu-id="473dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473dd-115">-DefaultProfile</span></span>
<span data-ttu-id="473dd-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="473dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="473dd-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="473dd-117">-EventHub</span></span>
<span data-ttu-id="473dd-118">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="473dd-118">EventHub Name</span></span>

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

### <span data-ttu-id="473dd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="473dd-119">-Name</span></span>
<span data-ttu-id="473dd-120">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="473dd-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="473dd-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="473dd-121">-Namespace</span></span>
<span data-ttu-id="473dd-122">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="473dd-122">Namespace Name</span></span>

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

### <span data-ttu-id="473dd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="473dd-123">-ResourceGroupName</span></span>
<span data-ttu-id="473dd-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="473dd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="473dd-125">-Rights</span><span class="sxs-lookup"><span data-stu-id="473dd-125">-Rights</span></span>
<span data-ttu-id="473dd-126">Diritti, ad esempio "Ascolta", "Invia","Gestisci"</span><span class="sxs-lookup"><span data-stu-id="473dd-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="473dd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="473dd-127">-Confirm</span></span>
<span data-ttu-id="473dd-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="473dd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="473dd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="473dd-129">-WhatIf</span></span>
<span data-ttu-id="473dd-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="473dd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="473dd-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="473dd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="473dd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473dd-132">CommonParameters</span></span>
<span data-ttu-id="473dd-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="473dd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473dd-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="473dd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473dd-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="473dd-135">INPUTS</span></span>

### <span data-ttu-id="473dd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="473dd-136">System.String</span></span>

### <span data-ttu-id="473dd-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="473dd-137">System.String[]</span></span>

## <span data-ttu-id="473dd-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="473dd-138">OUTPUTS</span></span>

### <span data-ttu-id="473dd-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="473dd-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="473dd-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="473dd-140">NOTES</span></span>

## <span data-ttu-id="473dd-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="473dd-141">RELATED LINKS</span></span>
