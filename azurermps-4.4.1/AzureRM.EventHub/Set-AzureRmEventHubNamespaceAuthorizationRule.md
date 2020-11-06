---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522136"
---
# <span data-ttu-id="9f318-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9f318-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="9f318-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f318-102">SYNOPSIS</span></span>
<span data-ttu-id="9f318-103">Aggiorna la regola di autorizzazione nello spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="9f318-103">Updates the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f318-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f318-104">SYNTAX</span></span>

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9f318-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f318-105">DESCRIPTION</span></span>
<span data-ttu-id="9f318-106">Il cmdlet Set-AzureRmEventHubNamespaceAuthorizationRule aggiorna la regola di autorizzazione nello spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="9f318-106">The Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet updates the authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="9f318-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f318-107">EXAMPLES</span></span>

### <span data-ttu-id="9f318-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9f318-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="9f318-109">Aggiorna la regola \` di autorizzazione MyAuthRuleName \` per concedere la gestione dei diritti.</span><span class="sxs-lookup"><span data-stu-id="9f318-109">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights.</span></span>

## <span data-ttu-id="9f318-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f318-110">PARAMETERS</span></span>

### <span data-ttu-id="9f318-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="9f318-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="9f318-112">Nome della regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="9f318-112">The authorization rule name.</span></span>
<span data-ttu-id="9f318-113">Obbligatorio se non è specificato-AuthruleObj.</span><span class="sxs-lookup"><span data-stu-id="9f318-113">Required if -AuthruleObj is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f318-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="9f318-114">-AuthRuleObj</span></span>
<span data-ttu-id="9f318-115">Oggetto regola di autorizzazione dello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="9f318-115">The Event Hubs namespace authorization rule object.</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f318-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9f318-116">-NamespaceName</span></span>
<span data-ttu-id="9f318-117">Nome dello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="9f318-117">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="9f318-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f318-118">-ResourceGroupName</span></span>
<span data-ttu-id="9f318-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9f318-119">Resource group name.</span></span>

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

### <span data-ttu-id="9f318-120">-Diritti</span><span class="sxs-lookup"><span data-stu-id="9f318-120">-Rights</span></span>
<span data-ttu-id="9f318-121">Obbligatorio se non è specificato-AuthruleObj.</span><span class="sxs-lookup"><span data-stu-id="9f318-121">Required if -AuthruleObj is not specified.</span></span>
<span data-ttu-id="9f318-122">Diritti ad esempio, @ ("Listen", "Send", "Manage")</span><span class="sxs-lookup"><span data-stu-id="9f318-122">Rights; for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f318-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9f318-123">-Confirm</span></span>
<span data-ttu-id="9f318-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f318-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f318-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f318-125">-WhatIf</span></span>
<span data-ttu-id="9f318-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f318-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f318-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f318-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="9f318-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f318-128">INPUTS</span></span>

### <span data-ttu-id="9f318-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9f318-129">System.String</span></span>

## <span data-ttu-id="9f318-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f318-130">OUTPUTS</span></span>

### <span data-ttu-id="9f318-131">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9f318-131">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9f318-132">Note</span><span class="sxs-lookup"><span data-stu-id="9f318-132">NOTES</span></span>

## <span data-ttu-id="9f318-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f318-133">RELATED LINKS</span></span>

