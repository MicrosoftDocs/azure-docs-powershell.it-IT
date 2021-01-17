---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361154"
---
# <span data-ttu-id="f8639-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f8639-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="f8639-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8639-102">SYNOPSIS</span></span>
<span data-ttu-id="f8639-103">Crea una nuova regola di autorizzazione Hub eventi per namespace o eventhub.</span><span class="sxs-lookup"><span data-stu-id="f8639-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="f8639-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8639-104">SYNTAX</span></span>

### <span data-ttu-id="f8639-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8639-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8639-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8639-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8639-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8639-107">DESCRIPTION</span></span>
<span data-ttu-id="f8639-108">Il cmdlet New-AzEventHubAuthorizationRule crea una nuova regola di autorizzazione Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="f8639-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="f8639-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8639-109">EXAMPLES</span></span>

### <span data-ttu-id="f8639-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8639-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="f8639-111">Crea una regola \` di autorizzazione MyAuthRuleName \` concedendo i diritti Listen e Send allo spazio dei nomi MyNamespace \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f8639-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f8639-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f8639-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="f8639-113">Crea una regola \` di autorizzazione MyAuthRuleName \` concedendo i diritti di ascolto e invio all'hub dell'evento \` MyEventHubName \` nello spazio dei nomi MyNamespace \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f8639-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f8639-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8639-114">PARAMETERS</span></span>

### <span data-ttu-id="f8639-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8639-115">-DefaultProfile</span></span>
<span data-ttu-id="f8639-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8639-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8639-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f8639-117">-EventHub</span></span>
<span data-ttu-id="f8639-118">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="f8639-118">EventHub Name</span></span>

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

### <span data-ttu-id="f8639-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8639-119">-Name</span></span>
<span data-ttu-id="f8639-120">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f8639-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f8639-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8639-121">-Namespace</span></span>
<span data-ttu-id="f8639-122">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8639-122">Namespace Name</span></span>

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

### <span data-ttu-id="f8639-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8639-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8639-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f8639-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f8639-125">-Diritti</span><span class="sxs-lookup"><span data-stu-id="f8639-125">-Rights</span></span>
<span data-ttu-id="f8639-126">Diritti, ad esempio "ascolta", "Invia", "Gestisci"</span><span class="sxs-lookup"><span data-stu-id="f8639-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="f8639-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f8639-127">-Confirm</span></span>
<span data-ttu-id="f8639-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8639-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8639-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8639-129">-WhatIf</span></span>
<span data-ttu-id="f8639-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8639-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8639-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8639-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8639-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8639-132">CommonParameters</span></span>
<span data-ttu-id="f8639-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8639-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8639-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8639-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8639-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8639-135">INPUTS</span></span>

### <span data-ttu-id="f8639-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f8639-136">System.String</span></span>

### <span data-ttu-id="f8639-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="f8639-137">System.String[]</span></span>

## <span data-ttu-id="f8639-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8639-138">OUTPUTS</span></span>

### <span data-ttu-id="f8639-139">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f8639-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f8639-140">Note</span><span class="sxs-lookup"><span data-stu-id="f8639-140">NOTES</span></span>

## <span data-ttu-id="f8639-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8639-141">RELATED LINKS</span></span>
