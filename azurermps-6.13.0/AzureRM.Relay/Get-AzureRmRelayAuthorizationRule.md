---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 13de3f05879234a0db1af34517d37172c2a5a6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687775"
---
# <span data-ttu-id="bd47f-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bd47f-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="bd47f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd47f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd47f-103">Ottiene la descrizione di una regola di autorizzazione specificata per un determinato entità di inoltro (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="bd47f-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd47f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd47f-104">SYNTAX</span></span>

### <span data-ttu-id="bd47f-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bd47f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd47f-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd47f-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd47f-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd47f-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd47f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd47f-108">DESCRIPTION</span></span>
<span data-ttu-id="bd47f-109">Il cmdlet **Get-AzureRmRelayAuthorizationRule** ottiene la descrizione della regola di autorizzazione specificata nelle entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="bd47f-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="bd47f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd47f-110">EXAMPLES</span></span>

### <span data-ttu-id="bd47f-111">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bd47f-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="bd47f-112">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="bd47f-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="bd47f-113">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="bd47f-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="bd47f-114">Restituisce la descrizione della regola di autorizzazione specificata per un determinato WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="bd47f-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="bd47f-115">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="bd47f-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="bd47f-116">Restituisce la descrizione della regola di autorizzazione specificata per un determinato HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="bd47f-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="bd47f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd47f-117">PARAMETERS</span></span>

### <span data-ttu-id="bd47f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd47f-118">-DefaultProfile</span></span>
<span data-ttu-id="bd47f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd47f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd47f-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="bd47f-120">-HybridConnection</span></span>
<span data-ttu-id="bd47f-121">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="bd47f-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="bd47f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd47f-122">-Name</span></span>
<span data-ttu-id="bd47f-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="bd47f-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="bd47f-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bd47f-124">-Namespace</span></span>
<span data-ttu-id="bd47f-125">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="bd47f-125">Namespace Name.</span></span>

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

### <span data-ttu-id="bd47f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd47f-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd47f-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bd47f-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="bd47f-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="bd47f-128">-WcfRelay</span></span>
<span data-ttu-id="bd47f-129">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="bd47f-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="bd47f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd47f-130">CommonParameters</span></span>
<span data-ttu-id="bd47f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd47f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bd47f-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd47f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd47f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd47f-133">INPUTS</span></span>

### <span data-ttu-id="bd47f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bd47f-134">System.String</span></span>


## <span data-ttu-id="bd47f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd47f-135">OUTPUTS</span></span>

### <span data-ttu-id="bd47f-136">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="bd47f-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="bd47f-137">Note</span><span class="sxs-lookup"><span data-stu-id="bd47f-137">NOTES</span></span>

## <span data-ttu-id="bd47f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd47f-138">RELATED LINKS</span></span>