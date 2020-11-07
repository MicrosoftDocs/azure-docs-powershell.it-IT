---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 07cc93cb75c7e6eab57fa03e663de700ee676432
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861517"
---
# <span data-ttu-id="ec146-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ec146-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="ec146-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec146-102">SYNOPSIS</span></span>
<span data-ttu-id="ec146-103">Ottiene i dettagli di una regola di autorizzazione o ottiene un elenco di regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ec146-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="ec146-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec146-104">SYNTAX</span></span>

### <span data-ttu-id="ec146-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec146-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec146-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec146-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec146-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec146-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec146-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec146-108">DESCRIPTION</span></span>
<span data-ttu-id="ec146-109">Il cmdlet Get-AzEventHubAuthorizationRule ottiene i dettagli di una regola di autorizzazione o un elenco di tutte le regole di autorizzazione per un hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="ec146-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="ec146-110">Se viene fornito il nome di una regola di autorizzazione, vengono restituiti i dettagli di tale regola di autorizzazione singola.</span><span class="sxs-lookup"><span data-stu-id="ec146-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="ec146-111">Se non viene specificato il nome di una regola di autorizzazione, viene restituito un elenco di tutte le regole di autorizzazione per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="ec146-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="ec146-112">Se il nome dell'alias di ripristino di emergenza è specificato, vengono restituiti i dettagli della regola di autorizzazione dello spazio dei nomi per l'alias configurato.</span><span class="sxs-lookup"><span data-stu-id="ec146-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="ec146-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec146-113">EXAMPLES</span></span>

### <span data-ttu-id="ec146-114">Esempio 1,0-AuthorizationRule for Namespace</span><span class="sxs-lookup"><span data-stu-id="ec146-114">Example 1.0 - AuthorizationRule for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="ec146-115">Ottiene la regola \` di autorizzazione MyAuthRuleName \` nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="ec146-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="ec146-116">Esempio 1,1-AuthorizationRules for Namespace</span><span class="sxs-lookup"><span data-stu-id="ec146-116">Example 1.1 - AuthorizationRules for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="ec146-117">Ottiene un elenco di tutte le regole di autorizzazione nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="ec146-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="ec146-118">Esempio 2,0-AuthorizationRule per EventHub</span><span class="sxs-lookup"><span data-stu-id="ec146-118">Example 2.0 - AuthorizationRule for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="ec146-119">Ottiene la regola \` di autorizzazione MyAuthRuleName \` nell'hub dell'evento \` MyEventHubName \` , che è ambito dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="ec146-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="ec146-120">Esempio 2,1-AuthorizationRules per EventHub</span><span class="sxs-lookup"><span data-stu-id="ec146-120">Example 2.1 - AuthorizationRules for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="ec146-121">Ottiene le regole di autorizzazione elenco nell'hub dell'evento \` MyEventHubName \` , che è ambito dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="ec146-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="ec146-122">Esempio 3,0-AuthorizationRule for alias (configurazione georecovery)</span><span class="sxs-lookup"><span data-stu-id="ec146-122">Example 3.0 - AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="ec146-123">Ottiene la regola \` di autorizzazione MyAuthRuleName \` nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="ec146-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="ec146-124">Esempio 3,1-AuthorizationRules for alias (configurazione georecovery)</span><span class="sxs-lookup"><span data-stu-id="ec146-124">Example 3.1 -AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="ec146-125">Ottiene un elenco di tutte le regole di autorizzazione \` MyAuthRuleName \` nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="ec146-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="ec146-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec146-126">PARAMETERS</span></span>

### <span data-ttu-id="ec146-127">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="ec146-127">-AliasName</span></span>
<span data-ttu-id="ec146-128">Nome alias</span><span class="sxs-lookup"><span data-stu-id="ec146-128">Alias Name</span></span>

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

### <span data-ttu-id="ec146-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec146-129">-DefaultProfile</span></span>
<span data-ttu-id="ec146-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec146-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec146-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="ec146-131">-Eventhub</span></span>
<span data-ttu-id="ec146-132">Nome Eventhub</span><span class="sxs-lookup"><span data-stu-id="ec146-132">Eventhub Name</span></span>

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

### <span data-ttu-id="ec146-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec146-133">-Name</span></span>
<span data-ttu-id="ec146-134">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ec146-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="ec146-135">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ec146-135">-Namespace</span></span>
<span data-ttu-id="ec146-136">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ec146-136">Namespace Name</span></span>

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

### <span data-ttu-id="ec146-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec146-137">-ResourceGroupName</span></span>
<span data-ttu-id="ec146-138">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ec146-138">Resource Group Name</span></span>

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

### <span data-ttu-id="ec146-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec146-139">CommonParameters</span></span>
<span data-ttu-id="ec146-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec146-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec146-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec146-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec146-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec146-142">INPUTS</span></span>

### <span data-ttu-id="ec146-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ec146-143">System.String</span></span>

## <span data-ttu-id="ec146-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec146-144">OUTPUTS</span></span>

### <span data-ttu-id="ec146-145">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ec146-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ec146-146">Note</span><span class="sxs-lookup"><span data-stu-id="ec146-146">NOTES</span></span>

## <span data-ttu-id="ec146-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec146-147">RELATED LINKS</span></span>
