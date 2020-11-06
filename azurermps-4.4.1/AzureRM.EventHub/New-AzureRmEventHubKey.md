---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3bd06ea2534298ba81cd546e8fa6e8de02fa5928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521667"
---
# <span data-ttu-id="aad54-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="aad54-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="aad54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aad54-102">SYNOPSIS</span></span>
<span data-ttu-id="aad54-103">Crea una nuova chiave primaria o secondaria per la regola di autorizzazione Hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="aad54-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aad54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aad54-104">SYNTAX</span></span>

### <span data-ttu-id="aad54-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aad54-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> -Namespace <String> -Name <String> -RegenerateKey <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="aad54-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="aad54-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> [-Namespace <String>] -EventHub <String> -Name <String>
 -RegenerateKey <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="aad54-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aad54-107">DESCRIPTION</span></span>
<span data-ttu-id="aad54-108">Il cmdlet New-AzureRmEventHubKey rigenera la chiave SAS primaria o secondaria per la regola di autorizzazione Hub eventi specificata.</span><span class="sxs-lookup"><span data-stu-id="aad54-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="aad54-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aad54-109">EXAMPLES</span></span>

### <span data-ttu-id="aad54-110">Esempio 1,1</span><span class="sxs-lookup"><span data-stu-id="aad54-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="aad54-111">Rigenera la chiave primaria per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="aad54-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="aad54-112">Esempio 1,2</span><span class="sxs-lookup"><span data-stu-id="aad54-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="aad54-113">Rigenera la chiave primaria per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="aad54-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="aad54-114">Esempio 2,1</span><span class="sxs-lookup"><span data-stu-id="aad54-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="aad54-115">Esempio 2,2</span><span class="sxs-lookup"><span data-stu-id="aad54-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="aad54-116">Rigenera la chiave secondaria per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="aad54-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="aad54-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aad54-117">PARAMETERS</span></span>

### <span data-ttu-id="aad54-118">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="aad54-118">-RegenerateKey</span></span>
<span data-ttu-id="aad54-119">Chiave per la rigenerazione: \` PrimaryKey \` o \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="aad54-119">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad54-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aad54-120">-Confirm</span></span>
<span data-ttu-id="aad54-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad54-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aad54-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aad54-122">-WhatIf</span></span>
<span data-ttu-id="aad54-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aad54-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aad54-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aad54-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aad54-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="aad54-125">-EventHub</span></span>
<span data-ttu-id="aad54-126">Nome EventHub.</span><span class="sxs-lookup"><span data-stu-id="aad54-126">EventHub Name.</span></span>

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

### <span data-ttu-id="aad54-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="aad54-127">-Name</span></span>
<span data-ttu-id="aad54-128">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="aad54-128">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="aad54-129">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aad54-129">-Namespace</span></span>
<span data-ttu-id="aad54-130">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="aad54-130">Namespace Name.</span></span>

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

### <span data-ttu-id="aad54-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad54-131">-ResourceGroupName</span></span>
<span data-ttu-id="aad54-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aad54-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="aad54-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aad54-133">INPUTS</span></span>

### <span data-ttu-id="aad54-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aad54-134">System.String</span></span>

## <span data-ttu-id="aad54-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aad54-135">OUTPUTS</span></span>

### <span data-ttu-id="aad54-136">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="aad54-136">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="aad54-137">Note</span><span class="sxs-lookup"><span data-stu-id="aad54-137">NOTES</span></span>

## <span data-ttu-id="aad54-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aad54-138">RELATED LINKS</span></span>

