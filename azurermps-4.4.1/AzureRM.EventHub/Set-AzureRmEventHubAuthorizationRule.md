---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e4600b44943170256d2c8ef999496d2160e369ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519182"
---
# <span data-ttu-id="f2dc0-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f2dc0-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="f2dc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="f2dc0-103">Aggiorna la regola di autorizzazione specificata in un hub eventi.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2dc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2dc0-104">SYNTAX</span></span>

### <span data-ttu-id="f2dc0-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2dc0-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f2dc0-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f2dc0-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f2dc0-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f2dc0-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String>
 -InputObject <AuthorizationRuleAttributes> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f2dc0-108">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f2dc0-108">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String> -Rights <String[]> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="f2dc0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2dc0-109">DESCRIPTION</span></span>
<span data-ttu-id="f2dc0-110">Il cmdlet Set-AzureRmEventHubAuthorizationRule aggiorna la regola di autorizzazione specificata nell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-110">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="f2dc0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2dc0-111">EXAMPLES</span></span>

### <span data-ttu-id="f2dc0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f2dc0-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="f2dc0-113">Aggiorna la regola di autorizzazione \` MyAuthRuleName \` per concedere la gestione dei diritti per l'hub dell'evento \` MyEventHubName \` , ambito dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="f2dc0-113">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="f2dc0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2dc0-114">PARAMETERS</span></span>

### <span data-ttu-id="f2dc0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2dc0-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2dc0-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-116">Resource group name.</span></span>

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

### <span data-ttu-id="f2dc0-117">-Diritti</span><span class="sxs-lookup"><span data-stu-id="f2dc0-117">-Rights</span></span>
<span data-ttu-id="f2dc0-118">Obbligatorio se "AuthruleObj" non è specificato.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-118">Required if 'AuthruleObj' not specified.</span></span>
<span data-ttu-id="f2dc0-119">Diritti ad esempio, @ ("Listen", "Send", "Manage")</span><span class="sxs-lookup"><span data-stu-id="f2dc0-119">Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2dc0-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f2dc0-120">-Confirm</span></span>
<span data-ttu-id="f2dc0-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2dc0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2dc0-122">-WhatIf</span></span>
<span data-ttu-id="f2dc0-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2dc0-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2dc0-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f2dc0-125">-EventHub</span></span>
<span data-ttu-id="f2dc0-126">Nome EventHub.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-126">EventHub Name.</span></span>

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

### <span data-ttu-id="f2dc0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2dc0-127">-InputObject</span></span>
<span data-ttu-id="f2dc0-128">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="f2dc0-128">{{Fill InputObject Description}}</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2dc0-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2dc0-129">-Name</span></span>
<span data-ttu-id="f2dc0-130">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-130">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f2dc0-131">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f2dc0-131">-Namespace</span></span>
<span data-ttu-id="f2dc0-132">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f2dc0-132">Namespace Name.</span></span>

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

## <span data-ttu-id="f2dc0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2dc0-133">INPUTS</span></span>

### <span data-ttu-id="f2dc0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f2dc0-134">System.String</span></span>

## <span data-ttu-id="f2dc0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2dc0-135">OUTPUTS</span></span>

### <span data-ttu-id="f2dc0-136">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f2dc0-136">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f2dc0-137">Note</span><span class="sxs-lookup"><span data-stu-id="f2dc0-137">NOTES</span></span>

## <span data-ttu-id="f2dc0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2dc0-138">RELATED LINKS</span></span>

