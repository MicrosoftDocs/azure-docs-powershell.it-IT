---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 70b5ac9eb40bf6c50ebb6d09849e8185c23927e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513847"
---
# <span data-ttu-id="c657a-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c657a-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c657a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c657a-102">SYNOPSIS</span></span>
<span data-ttu-id="c657a-103">Ottiene i dettagli di una regola di autorizzazione o ottiene un elenco di regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="c657a-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c657a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c657a-104">SYNTAX</span></span>

### <span data-ttu-id="c657a-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c657a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c657a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c657a-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c657a-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="c657a-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c657a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c657a-108">DESCRIPTION</span></span>
<span data-ttu-id="c657a-109">Il cmdlet Get-AzureRmEventHubAuthorizationRule ottiene i dettagli di una regola di autorizzazione o un elenco di tutte le regole di autorizzazione per un hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="c657a-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="c657a-110">Se viene fornito il nome di una regola di autorizzazione, vengono restituiti i dettagli di tale regola di autorizzazione singola.</span><span class="sxs-lookup"><span data-stu-id="c657a-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="c657a-111">Se non viene specificato il nome di una regola di autorizzazione, viene restituito un elenco di tutte le regole di autorizzazione per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="c657a-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="c657a-112">Se il nome dell'alias di ripristino di emergenza è specificato, vengono restituiti i dettagli della regola di autorizzazione dello spazio dei nomi per l'alias configurato.</span><span class="sxs-lookup"><span data-stu-id="c657a-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="c657a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c657a-113">EXAMPLES</span></span>

### <span data-ttu-id="c657a-114">Esempio 1,0-AuthorizationRule for Namespace</span><span class="sxs-lookup"><span data-stu-id="c657a-114">Example 1.0 - AuthorizationRule for namespace</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="c657a-115">Ottiene la regola \` di autorizzazione MyAuthRuleName \` nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="c657a-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c657a-116">Esempio 1,1-AuthorizationRules for Namespace</span><span class="sxs-lookup"><span data-stu-id="c657a-116">Example 1.1 - AuthorizationRules for namespace</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="c657a-117">Ottiene un elenco di tutte le regole di autorizzazione nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="c657a-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c657a-118">Esempio 2,0-AuthorizationRule per EventHub</span><span class="sxs-lookup"><span data-stu-id="c657a-118">Example 2.0 - AuthorizationRule for EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="c657a-119">Ottiene la regola \` di autorizzazione MyAuthRuleName \` nell'hub dell'evento \` MyEventHubName \` , che è ambito dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="c657a-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c657a-120">Esempio 2,1-AuthorizationRules per EventHub</span><span class="sxs-lookup"><span data-stu-id="c657a-120">Example 2.1 - AuthorizationRules for EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="c657a-121">Ottiene le regole di autorizzazione elenco nell'hub dell'evento \` MyEventHubName \` , che è ambito dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="c657a-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c657a-122">Esempio 3,0-AuthorizationRule for alias (configurazione georecovery)</span><span class="sxs-lookup"><span data-stu-id="c657a-122">Example 3.0 - AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="c657a-123">Ottiene la regola \` di autorizzazione MyAuthRuleName \` nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="c657a-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c657a-124">Esempio 3,1-AuthorizationRules for alias (configurazione georecovery)</span><span class="sxs-lookup"><span data-stu-id="c657a-124">Example 3.1 -AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="c657a-125">Ottiene un elenco di tutte le regole di autorizzazione \` MyAuthRuleName \` nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="c657a-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="c657a-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c657a-126">PARAMETERS</span></span>

### <span data-ttu-id="c657a-127">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="c657a-127">-AliasName</span></span>
<span data-ttu-id="c657a-128">Nome alias</span><span class="sxs-lookup"><span data-stu-id="c657a-128">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c657a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c657a-129">-DefaultProfile</span></span>
<span data-ttu-id="c657a-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c657a-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c657a-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="c657a-131">-Eventhub</span></span>
<span data-ttu-id="c657a-132">Nome Eventhub</span><span class="sxs-lookup"><span data-stu-id="c657a-132">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c657a-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="c657a-133">-Name</span></span>
<span data-ttu-id="c657a-134">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c657a-134">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c657a-135">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c657a-135">-Namespace</span></span>
<span data-ttu-id="c657a-136">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c657a-136">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c657a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c657a-137">-ResourceGroupName</span></span>
<span data-ttu-id="c657a-138">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c657a-138">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c657a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c657a-139">CommonParameters</span></span>
<span data-ttu-id="c657a-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c657a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c657a-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c657a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c657a-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c657a-142">INPUTS</span></span>

### <span data-ttu-id="c657a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c657a-143">System.String</span></span>

## <span data-ttu-id="c657a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c657a-144">OUTPUTS</span></span>

### <span data-ttu-id="c657a-145">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c657a-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c657a-146">Note</span><span class="sxs-lookup"><span data-stu-id="c657a-146">NOTES</span></span>

## <span data-ttu-id="c657a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c657a-147">RELATED LINKS</span></span>
