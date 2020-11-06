---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 439d4ea871d70fa830bb5a0f327cbc0f75d137df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521663"
---
# <span data-ttu-id="ea482-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ea482-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="ea482-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea482-102">SYNOPSIS</span></span>
<span data-ttu-id="ea482-103">Rimuove la regola di autorizzazione dell'hub eventi specificata.</span><span class="sxs-lookup"><span data-stu-id="ea482-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea482-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea482-104">SYNTAX</span></span>

### <span data-ttu-id="ea482-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea482-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ea482-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea482-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ea482-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea482-107">DESCRIPTION</span></span>
<span data-ttu-id="ea482-108">Il cmdlet Remove-AzureRmEventHubAuthorizationRule rimuove ed elimina la regola di autorizzazione specificata dall'hub dell'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="ea482-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="ea482-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea482-109">EXAMPLES</span></span>

### <span data-ttu-id="ea482-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea482-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="ea482-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ea482-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="ea482-112">Rimuove la regola \` di autorizzazione MyAuthRuleName \` dall'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="ea482-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="ea482-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea482-113">PARAMETERS</span></span>

### <span data-ttu-id="ea482-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea482-114">-ResourceGroupName</span></span>
<span data-ttu-id="ea482-115">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ea482-115">Resource group name.</span></span>

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

### <span data-ttu-id="ea482-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ea482-116">-Confirm</span></span>
<span data-ttu-id="ea482-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea482-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea482-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea482-118">-WhatIf</span></span>
<span data-ttu-id="ea482-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea482-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea482-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea482-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea482-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ea482-121">-EventHub</span></span>
<span data-ttu-id="ea482-122">Nome EventHub.</span><span class="sxs-lookup"><span data-stu-id="ea482-122">EventHub Name.</span></span>

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

### <span data-ttu-id="ea482-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ea482-123">-Force</span></span>
<span data-ttu-id="ea482-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ea482-124">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea482-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea482-125">-Name</span></span>
<span data-ttu-id="ea482-126">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ea482-126">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="ea482-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ea482-127">-Namespace</span></span>
<span data-ttu-id="ea482-128">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ea482-128">Namespace Name.</span></span>

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

### <span data-ttu-id="ea482-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea482-129">-PassThru</span></span>
<span data-ttu-id="ea482-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ea482-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="ea482-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea482-131">INPUTS</span></span>

### <span data-ttu-id="ea482-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ea482-132">System.String</span></span>

## <span data-ttu-id="ea482-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea482-133">OUTPUTS</span></span>

### <span data-ttu-id="ea482-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea482-134">System.Boolean</span></span>

## <span data-ttu-id="ea482-135">Note</span><span class="sxs-lookup"><span data-stu-id="ea482-135">NOTES</span></span>

## <span data-ttu-id="ea482-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea482-136">RELATED LINKS</span></span>

