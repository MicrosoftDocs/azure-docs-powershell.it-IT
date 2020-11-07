---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a980edd1833b37b358f86d2e3ccb6a9efc8d836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686582"
---
# <span data-ttu-id="91213-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="91213-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="91213-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91213-102">SYNOPSIS</span></span>
<span data-ttu-id="91213-103">Elimina la regola di autorizzazione specificata nello spazio dei nomi dell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="91213-103">Deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91213-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91213-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="91213-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91213-105">DESCRIPTION</span></span>
<span data-ttu-id="91213-106">Il cmdlet Remove-AzureRmEventHubNamespaceAuthorizationRule rimuove ed elimina la regola di autorizzazione specificata nello spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="91213-106">The Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet removes and deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

## <span data-ttu-id="91213-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91213-107">EXAMPLES</span></span>

### <span data-ttu-id="91213-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="91213-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="91213-109">Rimuove la regola \` di autorizzazione MyAuthRuleName \` dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="91213-109">Removes the authorization rule \`MyAuthRuleName\` from the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="91213-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91213-110">PARAMETERS</span></span>

### <span data-ttu-id="91213-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="91213-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="91213-112">Nome della regola di autorizzazione dello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="91213-112">The Event Hubs namespace authorization rule name.</span></span>

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

### <span data-ttu-id="91213-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="91213-113">-NamespaceName</span></span>
<span data-ttu-id="91213-114">Nome dello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="91213-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="91213-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91213-115">-ResourceGroupName</span></span>
<span data-ttu-id="91213-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="91213-116">Resource group name.</span></span>

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

### <span data-ttu-id="91213-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91213-117">-Confirm</span></span>
<span data-ttu-id="91213-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91213-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91213-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91213-119">-WhatIf</span></span>
<span data-ttu-id="91213-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91213-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91213-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91213-121">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="91213-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91213-122">INPUTS</span></span>

### <span data-ttu-id="91213-123">System. String</span><span class="sxs-lookup"><span data-stu-id="91213-123">System.String</span></span>

## <span data-ttu-id="91213-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91213-124">OUTPUTS</span></span>

### <span data-ttu-id="91213-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91213-125">System.Boolean</span></span>

## <span data-ttu-id="91213-126">Note</span><span class="sxs-lookup"><span data-stu-id="91213-126">NOTES</span></span>

## <span data-ttu-id="91213-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91213-127">RELATED LINKS</span></span>

