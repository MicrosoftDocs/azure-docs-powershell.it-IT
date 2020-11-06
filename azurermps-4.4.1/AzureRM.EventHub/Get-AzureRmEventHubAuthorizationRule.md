---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521680"
---
# <span data-ttu-id="65119-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="65119-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="65119-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65119-102">SYNOPSIS</span></span>
<span data-ttu-id="65119-103">Ottiene i dettagli di una regola di autorizzazione o ottiene un elenco di regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="65119-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65119-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65119-104">SYNTAX</span></span>

### <span data-ttu-id="65119-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="65119-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### <span data-ttu-id="65119-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="65119-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## <span data-ttu-id="65119-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65119-107">DESCRIPTION</span></span>
<span data-ttu-id="65119-108">Il cmdlet Get-AzureRmEventHubAuthorizationRule ottiene i dettagli di una regola di autorizzazione o un elenco di tutte le regole di autorizzazione per un hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="65119-108">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="65119-109">Se viene fornito il nome di una regola di autorizzazione, vengono restituiti i dettagli di tale regola di autorizzazione singola.</span><span class="sxs-lookup"><span data-stu-id="65119-109">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="65119-110">Se non viene specificato il nome di una regola di autorizzazione, viene restituito un elenco di tutte le regole di autorizzazione per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="65119-110">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>

## <span data-ttu-id="65119-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65119-111">EXAMPLES</span></span>

### <span data-ttu-id="65119-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="65119-112">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="65119-113">Ottiene la regola \` di autorizzazione MyAuthRuleName \` nell'hub dell'evento \` MyEventHubName \` , che è ambito dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="65119-113">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="65119-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="65119-114">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="65119-115">Ottiene un elenco di tutte le regole di autorizzazione nell'hub dell'evento \` MyEventHubName \` , che è ambito dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="65119-115">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="65119-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65119-116">PARAMETERS</span></span>

### <span data-ttu-id="65119-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65119-117">-ResourceGroupName</span></span>
<span data-ttu-id="65119-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="65119-118">Resource group name.</span></span>

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

### <span data-ttu-id="65119-119">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="65119-119">-Eventhub</span></span>
<span data-ttu-id="65119-120">Nome Eventhub.</span><span class="sxs-lookup"><span data-stu-id="65119-120">Eventhub Name.</span></span>

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

### <span data-ttu-id="65119-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="65119-121">-Name</span></span>
<span data-ttu-id="65119-122">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="65119-122">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65119-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="65119-123">-Namespace</span></span>
<span data-ttu-id="65119-124">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="65119-124">Namespace Name.</span></span>

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

## <span data-ttu-id="65119-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65119-125">INPUTS</span></span>

### <span data-ttu-id="65119-126">System. String</span><span class="sxs-lookup"><span data-stu-id="65119-126">System.String</span></span>

## <span data-ttu-id="65119-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65119-127">OUTPUTS</span></span>

### <span data-ttu-id="65119-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="65119-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="65119-129">Note</span><span class="sxs-lookup"><span data-stu-id="65119-129">NOTES</span></span>

## <span data-ttu-id="65119-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65119-130">RELATED LINKS</span></span>

