---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: bed3165eee350f55470c0cbca575226e77ec9d71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000638"
---
# <span data-ttu-id="3dff3-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3dff3-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="3dff3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dff3-102">SYNOPSIS</span></span>
<span data-ttu-id="3dff3-103">Ottiene la descrizione di una regola di autorizzazione specificata per un'entità di inoltro specificata (Spazio dei nomi/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3dff3-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3dff3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dff3-104">SYNTAX</span></span>

### <span data-ttu-id="3dff3-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3dff3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dff3-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3dff3-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dff3-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3dff3-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dff3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3dff3-108">DESCRIPTION</span></span>
<span data-ttu-id="3dff3-109">Il cmdlet **Get-AzRelayAuthorizationRule** ottiene la descrizione della regola di autorizzazione specificata nelle entità di inoltro (Spazio dei nomi/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3dff3-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3dff3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dff3-110">EXAMPLES</span></span>

### <span data-ttu-id="3dff3-111">Esempio 1: Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3dff3-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="3dff3-112">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="3dff3-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="3dff3-113">Esempio 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3dff3-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="3dff3-114">Restituisce la descrizione della regola di autorizzazione specificata per un dato WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="3dff3-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="3dff3-115">Esempio 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3dff3-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="3dff3-116">Restituisce la descrizione della regola di autorizzazione specificata per un dato HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="3dff3-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="3dff3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dff3-117">PARAMETERS</span></span>

### <span data-ttu-id="3dff3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dff3-118">-DefaultProfile</span></span>
<span data-ttu-id="3dff3-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dff3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dff3-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3dff3-120">-HybridConnection</span></span>
<span data-ttu-id="3dff3-121">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="3dff3-121">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dff3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3dff3-122">-Name</span></span>
<span data-ttu-id="3dff3-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="3dff3-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dff3-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3dff3-124">-Namespace</span></span>
<span data-ttu-id="3dff3-125">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3dff3-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dff3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dff3-126">-ResourceGroupName</span></span>
<span data-ttu-id="3dff3-127">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3dff3-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="3dff3-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3dff3-128">-WcfRelay</span></span>
<span data-ttu-id="3dff3-129">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="3dff3-129">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dff3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dff3-130">CommonParameters</span></span>
<span data-ttu-id="3dff3-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dff3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dff3-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dff3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dff3-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="3dff3-133">INPUTS</span></span>

### <span data-ttu-id="3dff3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3dff3-134">System.String</span></span>

## <span data-ttu-id="3dff3-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dff3-135">OUTPUTS</span></span>

### <span data-ttu-id="3dff3-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3dff3-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="3dff3-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="3dff3-137">NOTES</span></span>

## <span data-ttu-id="3dff3-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dff3-138">RELATED LINKS</span></span>
