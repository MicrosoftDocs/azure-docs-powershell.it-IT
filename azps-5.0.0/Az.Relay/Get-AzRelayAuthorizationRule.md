---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310074"
---
# <span data-ttu-id="58904-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="58904-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="58904-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58904-102">SYNOPSIS</span></span>
<span data-ttu-id="58904-103">Ottiene la descrizione di una regola di autorizzazione specificata per un determinato entità di inoltro (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="58904-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="58904-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58904-104">SYNTAX</span></span>

### <span data-ttu-id="58904-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58904-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58904-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="58904-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58904-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="58904-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58904-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58904-108">DESCRIPTION</span></span>
<span data-ttu-id="58904-109">Il cmdlet **Get-AzRelayAuthorizationRule** ottiene la descrizione della regola di autorizzazione specificata nelle entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="58904-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="58904-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58904-110">EXAMPLES</span></span>

### <span data-ttu-id="58904-111">Esempio 1: spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="58904-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="58904-112">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="58904-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="58904-113">Esempio 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="58904-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="58904-114">Restituisce la descrizione della regola di autorizzazione specificata per un determinato WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="58904-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="58904-115">Esempio 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="58904-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="58904-116">Restituisce la descrizione della regola di autorizzazione specificata per un determinato HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="58904-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="58904-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58904-117">PARAMETERS</span></span>

### <span data-ttu-id="58904-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58904-118">-DefaultProfile</span></span>
<span data-ttu-id="58904-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58904-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58904-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="58904-120">-HybridConnection</span></span>
<span data-ttu-id="58904-121">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="58904-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="58904-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="58904-122">-Name</span></span>
<span data-ttu-id="58904-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="58904-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="58904-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="58904-124">-Namespace</span></span>
<span data-ttu-id="58904-125">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="58904-125">Namespace Name.</span></span>

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

### <span data-ttu-id="58904-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58904-126">-ResourceGroupName</span></span>
<span data-ttu-id="58904-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58904-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="58904-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="58904-128">-WcfRelay</span></span>
<span data-ttu-id="58904-129">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="58904-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="58904-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58904-130">CommonParameters</span></span>
<span data-ttu-id="58904-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58904-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58904-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58904-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58904-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58904-133">INPUTS</span></span>

### <span data-ttu-id="58904-134">System. String</span><span class="sxs-lookup"><span data-stu-id="58904-134">System.String</span></span>

## <span data-ttu-id="58904-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58904-135">OUTPUTS</span></span>

### <span data-ttu-id="58904-136">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="58904-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="58904-137">Note</span><span class="sxs-lookup"><span data-stu-id="58904-137">NOTES</span></span>

## <span data-ttu-id="58904-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58904-138">RELATED LINKS</span></span>
