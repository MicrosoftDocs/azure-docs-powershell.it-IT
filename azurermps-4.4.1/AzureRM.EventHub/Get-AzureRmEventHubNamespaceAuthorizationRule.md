---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688318"
---
# <span data-ttu-id="7da1d-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7da1d-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="7da1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7da1d-102">SYNOPSIS</span></span>
<span data-ttu-id="7da1d-103">Ottiene i dettagli di una regola di autorizzazione dello spazio dei nomi Eventubs o ottiene un elenco di regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="7da1d-103">Gets the details of an Eventubs namespace authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7da1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7da1d-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## <span data-ttu-id="7da1d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7da1d-105">DESCRIPTION</span></span>
<span data-ttu-id="7da1d-106">Il cmdlet Get-AzureRmEventHubNamespaceAuthorizationRule ottiene i dettagli di una regola di autorizzazione dello spazio dei nomi degli hub eventi specificata o un elenco di regole di autorizzazione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7da1d-106">The Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet gets either the details of a specified Event Hubs namespace authorization rule, or a list of namespace authorization rules.</span></span>
<span data-ttu-id="7da1d-107">Se viene specificato il nome della regola di autorizzazione, vengono restituiti i dettagli di una singola regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="7da1d-107">If the authorization rule name is provided, the details of a single authorization rule is returned.</span></span>
<span data-ttu-id="7da1d-108">Se non viene specificato un nome per la regola di autorizzazione, viene restituito un elenco di tutte le regole di autorizzazione nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7da1d-108">If an authorization rule name is not provided, a list of all authorization rules in the namespace is returned.</span></span>

## <span data-ttu-id="7da1d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7da1d-109">EXAMPLES</span></span>

### <span data-ttu-id="7da1d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7da1d-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="7da1d-111">Restituisce la regola \` di autorizzazione MyAuthRuleName \` nello spazio dei nomi Hub di eventi NamespaceName \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7da1d-111">Returns the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7da1d-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7da1d-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

<span data-ttu-id="7da1d-113">Restituisce la regola di autorizzazione predefinita \` RootManageSharedAccessKey \` nello spazio dei nomi Hub di eventi NamespaceName \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7da1d-113">Returns the default authorization rule \`RootManageSharedAccessKey\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7da1d-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7da1d-114">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="7da1d-115">Restituisce tutte le regole di autorizzazione nello spazio dei nomi Hub eventi NamespaceName \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7da1d-115">Returns all authorization rules in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7da1d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7da1d-116">PARAMETERS</span></span>

### <span data-ttu-id="7da1d-117">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="7da1d-117">-AuthorizationRuleName</span></span>
<span data-ttu-id="7da1d-118">Nome della regola di autorizzazione dello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="7da1d-118">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da1d-119">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7da1d-119">-NamespaceName</span></span>
<span data-ttu-id="7da1d-120">Nome dello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="7da1d-120">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="7da1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="7da1d-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7da1d-122">Resource group name.</span></span>

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

## <span data-ttu-id="7da1d-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7da1d-123">INPUTS</span></span>

### <span data-ttu-id="7da1d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7da1d-124">System.String</span></span>

## <span data-ttu-id="7da1d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7da1d-125">OUTPUTS</span></span>

### <span data-ttu-id="7da1d-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7da1d-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7da1d-127">Note</span><span class="sxs-lookup"><span data-stu-id="7da1d-127">NOTES</span></span>

## <span data-ttu-id="7da1d-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7da1d-128">RELATED LINKS</span></span>

