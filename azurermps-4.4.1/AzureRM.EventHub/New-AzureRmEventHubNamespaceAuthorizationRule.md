---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: dc384ca6056ef13d5517241d550bacddf2e7d0d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521668"
---
# <span data-ttu-id="2b7fd-101">New-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2b7fd-101">New-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="2b7fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b7fd-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7fd-103">Crea una nuova regola di autorizzazione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="2b7fd-103">Creates a new authorization rule on the specified namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b7fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b7fd-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-Rights] <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2b7fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b7fd-105">DESCRIPTION</span></span>
<span data-ttu-id="2b7fd-106">Il cmdlet New-AzureRmEventHubNamespaceAuthorizationRule crea una nuova regola di autorizzazione nello spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="2b7fd-106">The New-AzureRmEventHubNamespaceAuthorizationRule cmdlet creates a new authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="2b7fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b7fd-107">EXAMPLES</span></span>

### <span data-ttu-id="2b7fd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b7fd-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="2b7fd-109">Crea la regola di autorizzazione \` MyAuthRuleName \` con i diritti di ascolto e invio, per lo spazio dei nomi Hub di eventi NamespaceName \` \` , nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="2b7fd-109">Creates the authorization rule \`MyAuthRuleName\` with Listen and Send rights, for Event Hubs namespace \`MyNamespaceName\`, in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2b7fd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b7fd-110">PARAMETERS</span></span>

### <span data-ttu-id="2b7fd-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="2b7fd-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="2b7fd-112">Nome della regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2b7fd-112">Authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7fd-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2b7fd-113">-NamespaceName</span></span>
<span data-ttu-id="2b7fd-114">Nome dello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="2b7fd-114">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7fd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b7fd-115">-ResourceGroupName</span></span>
<span data-ttu-id="2b7fd-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b7fd-116">Resource group name.</span></span>

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

### <span data-ttu-id="2b7fd-117">-Diritti</span><span class="sxs-lookup"><span data-stu-id="2b7fd-117">-Rights</span></span>
<span data-ttu-id="2b7fd-118">Diritti, ad esempio @ ("Listen", "Send", "Manage")</span><span class="sxs-lookup"><span data-stu-id="2b7fd-118">Rights;for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7fd-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b7fd-119">-Confirm</span></span>
<span data-ttu-id="2b7fd-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b7fd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b7fd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b7fd-121">-WhatIf</span></span>
<span data-ttu-id="2b7fd-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b7fd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b7fd-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b7fd-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="2b7fd-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b7fd-124">INPUTS</span></span>

### <span data-ttu-id="2b7fd-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2b7fd-125">System.String</span></span>

## <span data-ttu-id="2b7fd-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b7fd-126">OUTPUTS</span></span>

### <span data-ttu-id="2b7fd-127">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2b7fd-127">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2b7fd-128">Note</span><span class="sxs-lookup"><span data-stu-id="2b7fd-128">NOTES</span></span>

## <span data-ttu-id="2b7fd-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b7fd-129">RELATED LINKS</span></span>

