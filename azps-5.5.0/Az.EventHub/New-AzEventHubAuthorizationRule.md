---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180686"
---
# <span data-ttu-id="d09ae-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d09ae-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="d09ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d09ae-102">SYNOPSIS</span></span>
<span data-ttu-id="d09ae-103">Crea una nuova regola di autorizzazione Hub eventi per lo spazio dei nomi o eventhub.</span><span class="sxs-lookup"><span data-stu-id="d09ae-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="d09ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d09ae-104">SYNTAX</span></span>

### <span data-ttu-id="d09ae-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d09ae-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d09ae-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d09ae-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d09ae-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d09ae-107">DESCRIPTION</span></span>
<span data-ttu-id="d09ae-108">Il New-AzEventHubAuthorizationRule cmdlet crea una nuova regola di autorizzazione Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="d09ae-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="d09ae-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d09ae-109">EXAMPLES</span></span>

### <span data-ttu-id="d09ae-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d09ae-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="d09ae-111">Crea una regola di autorizzazione MyAuthRuleName concedendo i diritti di ascolto e invio allo spazio dei nomi MyResourceName, con il gruppo di \` \` risorse \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="d09ae-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d09ae-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d09ae-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="d09ae-113">Crea una regola di autorizzazione MyAuthRuleName concedendo i diritti di ascolto e invio all'hub eventi MyEventHubName nello spazio dei nomi MyResourceName, con il gruppo di \` \` risorse \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="d09ae-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d09ae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d09ae-114">PARAMETERS</span></span>

### <span data-ttu-id="d09ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d09ae-115">-DefaultProfile</span></span>
<span data-ttu-id="d09ae-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d09ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d09ae-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d09ae-117">-EventHub</span></span>
<span data-ttu-id="d09ae-118">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="d09ae-118">EventHub Name</span></span>

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

### <span data-ttu-id="d09ae-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d09ae-119">-Name</span></span>
<span data-ttu-id="d09ae-120">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="d09ae-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="d09ae-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d09ae-121">-Namespace</span></span>
<span data-ttu-id="d09ae-122">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d09ae-122">Namespace Name</span></span>

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

### <span data-ttu-id="d09ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d09ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="d09ae-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d09ae-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d09ae-125">-Rights</span><span class="sxs-lookup"><span data-stu-id="d09ae-125">-Rights</span></span>
<span data-ttu-id="d09ae-126">Diritti, ad esempio "Ascolta", "Invia","Gestisci"</span><span class="sxs-lookup"><span data-stu-id="d09ae-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="d09ae-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d09ae-127">-Confirm</span></span>
<span data-ttu-id="d09ae-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d09ae-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d09ae-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d09ae-129">-WhatIf</span></span>
<span data-ttu-id="d09ae-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d09ae-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d09ae-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d09ae-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d09ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d09ae-132">CommonParameters</span></span>
<span data-ttu-id="d09ae-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d09ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d09ae-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d09ae-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d09ae-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="d09ae-135">INPUTS</span></span>

### <span data-ttu-id="d09ae-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d09ae-136">System.String</span></span>

### <span data-ttu-id="d09ae-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d09ae-137">System.String[]</span></span>

## <span data-ttu-id="d09ae-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d09ae-138">OUTPUTS</span></span>

### <span data-ttu-id="d09ae-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d09ae-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d09ae-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="d09ae-140">NOTES</span></span>

## <span data-ttu-id="d09ae-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d09ae-141">RELATED LINKS</span></span>
