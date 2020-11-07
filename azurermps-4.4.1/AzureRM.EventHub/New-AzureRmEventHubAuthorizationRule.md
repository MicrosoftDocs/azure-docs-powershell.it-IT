---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3085479125219450368322ddb64fee4c06cdce2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686839"
---
# <span data-ttu-id="2885f-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2885f-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="2885f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2885f-102">SYNOPSIS</span></span>
<span data-ttu-id="2885f-103">Crea una nuova regola di autorizzazione Hub eventi per namespace o eventhub.</span><span class="sxs-lookup"><span data-stu-id="2885f-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2885f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2885f-104">SYNTAX</span></span>

### <span data-ttu-id="2885f-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2885f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 -Rights <String[]> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2885f-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2885f-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> -Rights <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2885f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2885f-107">DESCRIPTION</span></span>
<span data-ttu-id="2885f-108">Il cmdlet New-AzureRmEventHubAuthorizationRule crea una nuova regola di autorizzazione Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="2885f-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="2885f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2885f-109">EXAMPLES</span></span>

### <span data-ttu-id="2885f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2885f-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="2885f-111">Crea una regola \` di autorizzazione MyAuthRuleName \` concedendo i diritti Listen e Send allo spazio dei nomi MyNamespace \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="2885f-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2885f-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2885f-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="2885f-113">Crea una regola \` di autorizzazione MyAuthRuleName \` concedendo i diritti di ascolto e invio all'hub dell'evento \` MyEventHubName \` nello spazio dei nomi MyNamespace \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="2885f-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2885f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2885f-114">PARAMETERS</span></span>

### <span data-ttu-id="2885f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2885f-115">-ResourceGroupName</span></span>
<span data-ttu-id="2885f-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2885f-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2885f-117">-Diritti</span><span class="sxs-lookup"><span data-stu-id="2885f-117">-Rights</span></span>
<span data-ttu-id="2885f-118">Diritti ad esempio @ ("Listen", "Send", "Manage").</span><span class="sxs-lookup"><span data-stu-id="2885f-118">Rights; for example @("Listen","Send","Manage").</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2885f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2885f-119">-Confirm</span></span>
<span data-ttu-id="2885f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2885f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2885f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2885f-121">-WhatIf</span></span>
<span data-ttu-id="2885f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2885f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2885f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2885f-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2885f-124">-EventHub</span><span class="sxs-lookup"><span data-stu-id="2885f-124">-EventHub</span></span>
<span data-ttu-id="2885f-125">Nome EventHub.</span><span class="sxs-lookup"><span data-stu-id="2885f-125">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2885f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2885f-126">-Name</span></span>
<span data-ttu-id="2885f-127">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="2885f-127">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2885f-128">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2885f-128">-Namespace</span></span>
<span data-ttu-id="2885f-129">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="2885f-129">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="2885f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2885f-130">INPUTS</span></span>

### <span data-ttu-id="2885f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2885f-131">System.String</span></span>

## <span data-ttu-id="2885f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2885f-132">OUTPUTS</span></span>

### <span data-ttu-id="2885f-133">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2885f-133">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2885f-134">Note</span><span class="sxs-lookup"><span data-stu-id="2885f-134">NOTES</span></span>

## <span data-ttu-id="2885f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2885f-135">RELATED LINKS</span></span>

