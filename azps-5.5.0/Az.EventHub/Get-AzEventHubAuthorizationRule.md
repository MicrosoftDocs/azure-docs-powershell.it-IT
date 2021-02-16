---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204131"
---
# <span data-ttu-id="6d0d5-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6d0d5-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="6d0d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d0d5-102">SYNOPSIS</span></span>
<span data-ttu-id="6d0d5-103">Recupera i dettagli di una regola di autorizzazione o ottiene un elenco di regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="6d0d5-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="6d0d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d0d5-104">SYNTAX</span></span>

### <span data-ttu-id="6d0d5-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d0d5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d0d5-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d0d5-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d0d5-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d0d5-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d0d5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d0d5-108">DESCRIPTION</span></span>
<span data-ttu-id="6d0d5-109">Il Get-AzEventHubAuthorizationRule cmdlet di autorizzazione ottiene i dettagli di una regola di autorizzazione oppure un elenco di tutte le regole di autorizzazione per un hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="6d0d5-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="6d0d5-110">Se viene fornito il nome di una regola di autorizzazione, vengono restituiti i dettagli di quella singola regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="6d0d5-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="6d0d5-111">Se non viene fornito il nome di una regola di autorizzazione, viene restituito un elenco di tutte le regole di autorizzazione per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="6d0d5-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="6d0d5-112">Se è specificato il nome dell'alias di ripristino di emergenza, vengono restituiti i dettagli della regola di autorizzazione dello spazio dei nomi per l'alias configurato.</span><span class="sxs-lookup"><span data-stu-id="6d0d5-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="6d0d5-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d0d5-113">EXAMPLES</span></span>

### <span data-ttu-id="6d0d5-114">Esempio 1: AuthorizationRule per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6d0d5-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="6d0d5-115">Ottiene la regola di autorizzazione \` MyAuthRuleName \` nello spazio dei nomi \` MyHostName. \`</span><span class="sxs-lookup"><span data-stu-id="6d0d5-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="6d0d5-116">Esempio 2: AuthorizationRules per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6d0d5-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="6d0d5-117">Ottiene un elenco di tutte le regole di autorizzazione nello spazio \` dei nomi MyHostName. \`</span><span class="sxs-lookup"><span data-stu-id="6d0d5-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="6d0d5-118">Esempio 3: AuthorizationRule per EventHub</span><span class="sxs-lookup"><span data-stu-id="6d0d5-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="6d0d5-119">Ottiene la regola di autorizzazione \` MyAuthRuleName \` nell'hub eventi MyEventHubName, il cui ambito è indicato dallo spazio dei nomi \` \` \` MyHubName. \`</span><span class="sxs-lookup"><span data-stu-id="6d0d5-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="6d0d5-120">Esempio 4: AuthorizationRules per EventHub</span><span class="sxs-lookup"><span data-stu-id="6d0d5-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="6d0d5-121">Ottiene le regole di autorizzazione dell'elenco nell'hub eventi MyEventHubName, il cui ambito è indicato dallo spazio dei nomi \` \` \` MyHubName. \`</span><span class="sxs-lookup"><span data-stu-id="6d0d5-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="6d0d5-122">Esempio 5: AuthorizationRule per l'alias (Configurazione georecovery)</span><span class="sxs-lookup"><span data-stu-id="6d0d5-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="6d0d5-123">Ottiene la regola di autorizzazione \` MyAuthRuleName \` nello spazio dei nomi \` MyHostName. \`</span><span class="sxs-lookup"><span data-stu-id="6d0d5-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="6d0d5-124">Esempio 6: AuthorizationRules per l'alias (Configurazione georecovery)</span><span class="sxs-lookup"><span data-stu-id="6d0d5-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="6d0d5-125">Ottiene un elenco di tutte le regole di autorizzazione \` MyAuthRuleName \` nello spazio dei nomi \` MyHostName. \`</span><span class="sxs-lookup"><span data-stu-id="6d0d5-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="6d0d5-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d0d5-126">PARAMETERS</span></span>

### <span data-ttu-id="6d0d5-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="6d0d5-127">-AliasName</span></span>
<span data-ttu-id="6d0d5-128">Nome alias</span><span class="sxs-lookup"><span data-stu-id="6d0d5-128">Alias Name</span></span>

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

### <span data-ttu-id="6d0d5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d0d5-129">-DefaultProfile</span></span>
<span data-ttu-id="6d0d5-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d0d5-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d0d5-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="6d0d5-131">-Eventhub</span></span>
<span data-ttu-id="6d0d5-132">Nome Eventhub</span><span class="sxs-lookup"><span data-stu-id="6d0d5-132">Eventhub Name</span></span>

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

### <span data-ttu-id="6d0d5-133">-Name</span><span class="sxs-lookup"><span data-stu-id="6d0d5-133">-Name</span></span>
<span data-ttu-id="6d0d5-134">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="6d0d5-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="6d0d5-135">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6d0d5-135">-Namespace</span></span>
<span data-ttu-id="6d0d5-136">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6d0d5-136">Namespace Name</span></span>

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

### <span data-ttu-id="6d0d5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d0d5-137">-ResourceGroupName</span></span>
<span data-ttu-id="6d0d5-138">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6d0d5-138">Resource Group Name</span></span>

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

### <span data-ttu-id="6d0d5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d0d5-139">CommonParameters</span></span>
<span data-ttu-id="6d0d5-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d0d5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d0d5-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d0d5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d0d5-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d0d5-142">INPUTS</span></span>

### <span data-ttu-id="6d0d5-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6d0d5-143">System.String</span></span>

## <span data-ttu-id="6d0d5-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d0d5-144">OUTPUTS</span></span>

### <span data-ttu-id="6d0d5-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6d0d5-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6d0d5-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d0d5-146">NOTES</span></span>

## <span data-ttu-id="6d0d5-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d0d5-147">RELATED LINKS</span></span>
