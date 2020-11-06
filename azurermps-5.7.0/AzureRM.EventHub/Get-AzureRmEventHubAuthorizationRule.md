---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d162122b82f592472fb31f1087db29faedf08cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520457"
---
# <span data-ttu-id="d4448-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d4448-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="d4448-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4448-102">SYNOPSIS</span></span>
<span data-ttu-id="d4448-103">Ottiene i dettagli di una regola di autorizzazione o ottiene un elenco di regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="d4448-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4448-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4448-104">SYNTAX</span></span>

### <span data-ttu-id="d4448-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4448-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4448-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4448-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4448-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4448-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4448-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4448-108">DESCRIPTION</span></span>
<span data-ttu-id="d4448-109">Il cmdlet Get-AzureRmEventHubAuthorizationRule ottiene i dettagli di una regola di autorizzazione o un elenco di tutte le regole di autorizzazione per un hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="d4448-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="d4448-110">Se viene fornito il nome di una regola di autorizzazione, vengono restituiti i dettagli di tale regola di autorizzazione singola.</span><span class="sxs-lookup"><span data-stu-id="d4448-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="d4448-111">Se non viene specificato il nome di una regola di autorizzazione, viene restituito un elenco di tutte le regole di autorizzazione per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="d4448-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="d4448-112">Se il nome dell'alias di ripristino di emergenza è specificato, vengono restituiti i dettagli della regola di autorizzazione dello spazio dei nomi per l'alias configurato.</span><span class="sxs-lookup"><span data-stu-id="d4448-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span> 

## <span data-ttu-id="d4448-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4448-113">EXAMPLES</span></span>

### <span data-ttu-id="d4448-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d4448-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="d4448-115">Ottiene la regola \` di autorizzazione MyAuthRuleName \` nell'hub dell'evento \` MyEventHubName \` , che è ambito dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="d4448-115">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="d4448-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d4448-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="d4448-117">Ottiene un elenco di tutte le regole di autorizzazione nell'hub dell'evento \` MyEventHubName \` , che è ambito dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="d4448-117">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="d4448-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d4448-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="d4448-119">Ottiene la regola \` di autorizzazione MyAuthRuleName \` nello spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="d4448-119">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="d4448-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4448-120">PARAMETERS</span></span>

### <span data-ttu-id="d4448-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="d4448-121">-AliasName</span></span>
<span data-ttu-id="d4448-122">Nome alias</span><span class="sxs-lookup"><span data-stu-id="d4448-122">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4448-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4448-123">-DefaultProfile</span></span>
<span data-ttu-id="d4448-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4448-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4448-125">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="d4448-125">-Eventhub</span></span>
<span data-ttu-id="d4448-126">Nome Eventhub</span><span class="sxs-lookup"><span data-stu-id="d4448-126">Eventhub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4448-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4448-127">-Name</span></span>
<span data-ttu-id="d4448-128">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d4448-128">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4448-129">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d4448-129">-Namespace</span></span>
<span data-ttu-id="d4448-130">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d4448-130">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4448-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4448-131">-ResourceGroupName</span></span>
<span data-ttu-id="d4448-132">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d4448-132">Resource Group Name</span></span>

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

### <span data-ttu-id="d4448-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4448-133">CommonParameters</span></span>
<span data-ttu-id="d4448-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4448-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d4448-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4448-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4448-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4448-136">INPUTS</span></span>

### <span data-ttu-id="d4448-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d4448-137">System.String</span></span>


## <span data-ttu-id="d4448-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4448-138">OUTPUTS</span></span>

### <span data-ttu-id="d4448-139">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d4448-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="d4448-140">Note</span><span class="sxs-lookup"><span data-stu-id="d4448-140">NOTES</span></span>

## <span data-ttu-id="d4448-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4448-141">RELATED LINKS</span></span>
