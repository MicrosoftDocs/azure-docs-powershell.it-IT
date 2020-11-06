---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: f4f28ee3f07127803e6187f00565ee8d4caf3084
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521677"
---
# <span data-ttu-id="7e0a2-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="7e0a2-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="7e0a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0a2-103">Ottiene i dettagli della chiave primaria della regola di autorizzazione degli hub di eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="7e0a2-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e0a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e0a2-104">SYNTAX</span></span>

### <span data-ttu-id="7e0a2-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e0a2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> -Namespace <String> -Name <String>
```

### <span data-ttu-id="7e0a2-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e0a2-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String> -Name <String>
```

## <span data-ttu-id="7e0a2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e0a2-107">DESCRIPTION</span></span>
<span data-ttu-id="7e0a2-108">Il cmdlet Get-AzureRmEventHubKey restituisce le caratteristiche connectionStrings primarie e secondarie e i dettagli delle chiavi della regola di autorizzazione degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="7e0a2-108">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="7e0a2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e0a2-109">EXAMPLES</span></span>

### <span data-ttu-id="7e0a2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e0a2-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="7e0a2-111">Ottiene i dettagli delle caratteristiche connectionStrings primarie e secondarie e delle chiavi per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="7e0a2-111">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="7e0a2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e0a2-112">PARAMETERS</span></span>

### <span data-ttu-id="7e0a2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e0a2-113">-ResourceGroupName</span></span>
<span data-ttu-id="7e0a2-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7e0a2-114">Resource group name.</span></span>

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

### <span data-ttu-id="7e0a2-115">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7e0a2-115">-EventHub</span></span>
<span data-ttu-id="7e0a2-116">Nome EventHub.</span><span class="sxs-lookup"><span data-stu-id="7e0a2-116">EventHub Name.</span></span>

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

### <span data-ttu-id="7e0a2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e0a2-117">-Name</span></span>
<span data-ttu-id="7e0a2-118">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="7e0a2-118">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7e0a2-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7e0a2-119">-Namespace</span></span>
<span data-ttu-id="7e0a2-120">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7e0a2-120">Namespace Name.</span></span>

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

## <span data-ttu-id="7e0a2-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e0a2-121">INPUTS</span></span>

### <span data-ttu-id="7e0a2-122">System. String</span><span class="sxs-lookup"><span data-stu-id="7e0a2-122">System.String</span></span>

## <span data-ttu-id="7e0a2-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e0a2-123">OUTPUTS</span></span>

### <span data-ttu-id="7e0a2-124">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="7e0a2-124">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="7e0a2-125">Note</span><span class="sxs-lookup"><span data-stu-id="7e0a2-125">NOTES</span></span>

## <span data-ttu-id="7e0a2-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e0a2-126">RELATED LINKS</span></span>

