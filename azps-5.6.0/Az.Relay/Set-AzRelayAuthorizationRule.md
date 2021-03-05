---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 3165905cc86d2255670127cd90c015ce20096c14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000429"
---
# <span data-ttu-id="141ce-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="141ce-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="141ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="141ce-102">SYNOPSIS</span></span>
<span data-ttu-id="141ce-103">Aggiorna la descrizione della regola di autorizzazione specificata per le entità di inoltro specificate (Spazio dei nomi/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="141ce-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="141ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="141ce-104">SYNTAX</span></span>

### <span data-ttu-id="141ce-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="141ce-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="141ce-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="141ce-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="141ce-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="141ce-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="141ce-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="141ce-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="141ce-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="141ce-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="141ce-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="141ce-110">DESCRIPTION</span></span>
<span data-ttu-id="141ce-111">Il cmdlet **Set-AzRelayAuthorizationRule** aggiorna la descrizione della regola di autorizzazione specificata per le entità di inoltro (Spazio dei nomi/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="141ce-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="141ce-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="141ce-112">EXAMPLES</span></span>

### <span data-ttu-id="141ce-113">Esempio 1.1 - Spazio dei nomi con InputObject</span><span class="sxs-lookup"><span data-stu-id="141ce-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="141ce-114">Aggiunge **Invia dai** diritti di accesso della regola di autorizzazione nello spazio dei `AuthoRule1` `TestNameSpace-Relay1` nomi.</span><span class="sxs-lookup"><span data-stu-id="141ce-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="141ce-115">Esempio 1.2 - Spazio dei nomi con parametro Rights</span><span class="sxs-lookup"><span data-stu-id="141ce-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="141ce-116">Aggiunge **Invia dai** diritti di accesso della regola di autorizzazione nello spazio dei `AuthoRule1` `TestNameSpace-Relay1` nomi.</span><span class="sxs-lookup"><span data-stu-id="141ce-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="141ce-117">Esempio 2.1 - WcfRelay con InputObject</span><span class="sxs-lookup"><span data-stu-id="141ce-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="141ce-118">Aggiunge **Invia** ai diritti di accesso della regola di autorizzazione `AuthoRule1` di WcfRelay. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="141ce-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="141ce-119">Esempio 2.2 - WcfRelay con parametro Rights</span><span class="sxs-lookup"><span data-stu-id="141ce-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="141ce-120">Aggiunge **Invia** ai diritti di accesso della regola di autorizzazione `AuthoRule1` di WcfRelay. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="141ce-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="141ce-121">Esempio 3.1 - HybridConnection con InputObject</span><span class="sxs-lookup"><span data-stu-id="141ce-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="141ce-122">Aggiunge **Invia ai** diritti di accesso della regola di autorizzazione di `AuthoRule1` `TestHybridConnection` HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="141ce-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="141ce-123">Esempio 3.2 - Parametro HybridConnection with Rights</span><span class="sxs-lookup"><span data-stu-id="141ce-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="141ce-124">Aggiunge **Invia ai** diritti di accesso della regola di autorizzazione di `AuthoRule1` `TestHybridConnection` HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="141ce-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="141ce-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="141ce-125">PARAMETERS</span></span>

### <span data-ttu-id="141ce-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="141ce-126">-DefaultProfile</span></span>
<span data-ttu-id="141ce-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="141ce-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="141ce-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="141ce-128">-HybridConnection</span></span>
<span data-ttu-id="141ce-129">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="141ce-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="141ce-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="141ce-130">-InputObject</span></span>
<span data-ttu-id="141ce-131">Oggetto AuthorizationRule di inoltro.</span><span class="sxs-lookup"><span data-stu-id="141ce-131">Relay AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141ce-132">-Name</span><span class="sxs-lookup"><span data-stu-id="141ce-132">-Name</span></span>
<span data-ttu-id="141ce-133">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="141ce-133">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="141ce-134">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="141ce-134">-Namespace</span></span>
<span data-ttu-id="141ce-135">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="141ce-135">Namespace Name.</span></span>

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

### <span data-ttu-id="141ce-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="141ce-136">-ResourceGroupName</span></span>
<span data-ttu-id="141ce-137">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="141ce-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="141ce-138">-Rights</span><span class="sxs-lookup"><span data-stu-id="141ce-138">-Rights</span></span>
<span data-ttu-id="141ce-139">Diritti, ad esempio @("Ascoltare","Invia","Gestisci")</span><span class="sxs-lookup"><span data-stu-id="141ce-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141ce-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="141ce-140">-WcfRelay</span></span>
<span data-ttu-id="141ce-141">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="141ce-141">WcfRelay Name.</span></span>

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

### <span data-ttu-id="141ce-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="141ce-142">-Confirm</span></span>
<span data-ttu-id="141ce-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="141ce-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141ce-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="141ce-144">-WhatIf</span></span>
<span data-ttu-id="141ce-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="141ce-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="141ce-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="141ce-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141ce-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141ce-147">CommonParameters</span></span>
<span data-ttu-id="141ce-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="141ce-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141ce-149">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="141ce-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141ce-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="141ce-150">INPUTS</span></span>

### <span data-ttu-id="141ce-151">System.String</span><span class="sxs-lookup"><span data-stu-id="141ce-151">System.String</span></span>

### <span data-ttu-id="141ce-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="141ce-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="141ce-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="141ce-153">System.String[]</span></span>

## <span data-ttu-id="141ce-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="141ce-154">OUTPUTS</span></span>

### <span data-ttu-id="141ce-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="141ce-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="141ce-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="141ce-156">NOTES</span></span>

## <span data-ttu-id="141ce-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="141ce-157">RELATED LINKS</span></span>
