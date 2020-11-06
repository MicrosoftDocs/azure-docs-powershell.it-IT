---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 53a46e9c78544919c325f63b8bc8ccf9fd457f31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516092"
---
# <span data-ttu-id="2ce82-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2ce82-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="2ce82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ce82-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce82-103">Ottiene la descrizione di una regola di autorizzazione specificata per un determinato entità di inoltro (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="2ce82-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ce82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ce82-104">SYNTAX</span></span>

### <span data-ttu-id="2ce82-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ce82-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ce82-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ce82-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ce82-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ce82-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ce82-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ce82-108">DESCRIPTION</span></span>
<span data-ttu-id="2ce82-109">Il cmdlet **Get-AzureRmRelayAuthorizationRule** ottiene la descrizione della regola di autorizzazione specificata nelle entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="2ce82-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2ce82-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ce82-110">EXAMPLES</span></span>

### <span data-ttu-id="2ce82-111">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2ce82-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="2ce82-112">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="2ce82-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="2ce82-113">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2ce82-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

<span data-ttu-id="2ce82-114">Restituisce la descrizione della regola di autorizzazione specificata per un determinato WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="2ce82-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="2ce82-115">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2ce82-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="2ce82-116">Restituisce la descrizione della regola di autorizzazione specificata per un determinato HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="2ce82-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="2ce82-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ce82-117">PARAMETERS</span></span>

### <span data-ttu-id="2ce82-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2ce82-118">-HybridConnection</span></span>
<span data-ttu-id="2ce82-119">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="2ce82-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="2ce82-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ce82-120">-Name</span></span>
<span data-ttu-id="2ce82-121">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="2ce82-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2ce82-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2ce82-122">-Namespace</span></span>
<span data-ttu-id="2ce82-123">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="2ce82-123">Namespace Name.</span></span>

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

### <span data-ttu-id="2ce82-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ce82-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ce82-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2ce82-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="2ce82-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2ce82-126">-WcfRelay</span></span>
<span data-ttu-id="2ce82-127">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="2ce82-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="2ce82-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce82-128">-DefaultProfile</span></span>
<span data-ttu-id="2ce82-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ce82-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ce82-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce82-130">CommonParameters</span></span>
<span data-ttu-id="2ce82-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce82-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce82-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ce82-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce82-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ce82-133">INPUTS</span></span>

### <span data-ttu-id="2ce82-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ce82-134">-ResourceGroupName</span></span>
 <span data-ttu-id="2ce82-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2ce82-135">System.String</span></span> 

### <span data-ttu-id="2ce82-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2ce82-136">-NamespaceName</span></span>
 <span data-ttu-id="2ce82-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2ce82-137">System.String</span></span> 
 

### <span data-ttu-id="2ce82-138">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="2ce82-138">-HybridConnectionsName</span></span>
 <span data-ttu-id="2ce82-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2ce82-139">System.String</span></span> 

### <span data-ttu-id="2ce82-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="2ce82-140">-WcfRelayName</span></span>
 <span data-ttu-id="2ce82-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2ce82-141">System.String</span></span> 

### <span data-ttu-id="2ce82-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ce82-142">-Name</span></span>
 <span data-ttu-id="2ce82-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2ce82-143">System.String</span></span>

## <span data-ttu-id="2ce82-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ce82-144">OUTPUTS</span></span>

### <span data-ttu-id="2ce82-145">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2ce82-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2ce82-146">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2ce82-146">Example 1 - Namespace</span></span>
<span data-ttu-id="2ce82-147">Rights: {Listen, Send} Name: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span><span class="sxs-lookup"><span data-stu-id="2ce82-147">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span></span>

### <span data-ttu-id="2ce82-148">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2ce82-148">Example 2 - WcfRelay</span></span>
<span data-ttu-id="2ce82-149">Rights: {Listen, Send} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="2ce82-149">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="2ce82-150">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2ce82-150">Example 3 - HybridConnection</span></span>
<span data-ttu-id="2ce82-151">Rights: {Listen, Send} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="2ce82-151">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="2ce82-152">Note</span><span class="sxs-lookup"><span data-stu-id="2ce82-152">NOTES</span></span>

## <span data-ttu-id="2ce82-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ce82-153">RELATED LINKS</span></span>

