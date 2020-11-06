---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 64c839140907b10d62b4f71025afab985d5ba736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519550"
---
# <span data-ttu-id="83445-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="83445-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="83445-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83445-102">SYNOPSIS</span></span>
<span data-ttu-id="83445-103">Aggiorna la descrizione della regola di autorizzazione specificata per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="83445-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83445-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83445-104">SYNTAX</span></span>

### <span data-ttu-id="83445-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83445-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83445-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="83445-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83445-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="83445-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-InputObject <AuthorizationRuleAttributes>]
 [-Rights <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83445-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="83445-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 -InputObject <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83445-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="83445-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> -Rights <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83445-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83445-110">DESCRIPTION</span></span>
<span data-ttu-id="83445-111">Il cmdlet **set-AzureRmRelayAuthorizationRule** aggiorna la descrizione per la regola di autorizzazione specificata delle entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="83445-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="83445-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83445-112">EXAMPLES</span></span>

### <span data-ttu-id="83445-113">Esempio 1,1-spazio dei nomi con InputObject</span><span class="sxs-lookup"><span data-stu-id="83445-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="83445-114">Aggiunge l' **invio** dei diritti di accesso della regola di autorizzazione `AuthoRule1` nello spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="83445-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="83445-115">Esempio 1,2-spazio dei nomi con Rights Parameter</span><span class="sxs-lookup"><span data-stu-id="83445-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="83445-116">Aggiunge l' **invio** dei diritti di accesso della regola di autorizzazione `AuthoRule1` nello spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="83445-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="83445-117">Esempio 2,1-WcfRelay con InputObject</span><span class="sxs-lookup"><span data-stu-id="83445-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="83445-118">Aggiunge l' **invio** ai diritti di accesso della regola `AuthoRule1` di autorizzazione di WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="83445-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="83445-119">Esempio 2,2-WcfRelay con Rights Parameter</span><span class="sxs-lookup"><span data-stu-id="83445-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="83445-120">Aggiunge l' **invio** ai diritti di accesso della regola `AuthoRule1` di autorizzazione di WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="83445-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="83445-121">Esempio 3,1-HybridConnection con InputObject</span><span class="sxs-lookup"><span data-stu-id="83445-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="83445-122">Aggiunge l' **invio** ai diritti di accesso della regola `AuthoRule1` di autorizzazione di HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="83445-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="83445-123">Esempio 3,2-HybridConnection con Rights Parameter</span><span class="sxs-lookup"><span data-stu-id="83445-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="83445-124">Aggiunge l' **invio** ai diritti di accesso della regola `AuthoRule1` di autorizzazione di HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="83445-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="83445-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83445-125">PARAMETERS</span></span>

### <span data-ttu-id="83445-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83445-126">-Confirm</span></span>
<span data-ttu-id="83445-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83445-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83445-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="83445-128">-HybridConnection</span></span>
<span data-ttu-id="83445-129">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="83445-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="83445-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="83445-130">-Name</span></span>
<span data-ttu-id="83445-131">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="83445-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="83445-132">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="83445-132">-Namespace</span></span>
<span data-ttu-id="83445-133">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="83445-133">Namespace Name.</span></span>

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

### <span data-ttu-id="83445-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83445-134">-ResourceGroupName</span></span>
<span data-ttu-id="83445-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="83445-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="83445-136">-Diritti</span><span class="sxs-lookup"><span data-stu-id="83445-136">-Rights</span></span>
<span data-ttu-id="83445-137">Diritti, ad esempio @ ("ascolta", "Invia", "Gestisci")</span><span class="sxs-lookup"><span data-stu-id="83445-137">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83445-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="83445-138">-WcfRelay</span></span>
<span data-ttu-id="83445-139">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="83445-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="83445-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83445-140">-WhatIf</span></span>
<span data-ttu-id="83445-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83445-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83445-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83445-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83445-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83445-143">-DefaultProfile</span></span>
<span data-ttu-id="83445-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83445-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83445-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83445-145">-InputObject</span></span>
<span data-ttu-id="83445-146">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="83445-146">{{Fill InputObject Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83445-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83445-147">CommonParameters</span></span>
<span data-ttu-id="83445-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83445-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83445-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83445-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83445-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83445-150">INPUTS</span></span>

### <span data-ttu-id="83445-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83445-151">-ResourceGroupName</span></span>
 <span data-ttu-id="83445-152">System. String</span><span class="sxs-lookup"><span data-stu-id="83445-152">System.String</span></span> 

### <span data-ttu-id="83445-153">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="83445-153">-Namespace</span></span>
 <span data-ttu-id="83445-154">System. String</span><span class="sxs-lookup"><span data-stu-id="83445-154">System.String</span></span> 
 

### <span data-ttu-id="83445-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="83445-155">-WcfRelay</span></span>
 <span data-ttu-id="83445-156">System. String</span><span class="sxs-lookup"><span data-stu-id="83445-156">System.String</span></span> 

### <span data-ttu-id="83445-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="83445-157">-HybridConnection</span></span>
 <span data-ttu-id="83445-158">System. String</span><span class="sxs-lookup"><span data-stu-id="83445-158">System.String</span></span> 
 

### <span data-ttu-id="83445-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="83445-159">-Name</span></span>
 <span data-ttu-id="83445-160">System. String</span><span class="sxs-lookup"><span data-stu-id="83445-160">System.String</span></span>

### <span data-ttu-id="83445-161">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83445-161">-InputObject</span></span>
 <span data-ttu-id="83445-162">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="83445-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="83445-163">-Diritti</span><span class="sxs-lookup"><span data-stu-id="83445-163">-Rights</span></span>
 <span data-ttu-id="83445-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="83445-164">System.String []</span></span>

## <span data-ttu-id="83445-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83445-165">OUTPUTS</span></span>

### <span data-ttu-id="83445-166">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="83445-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="83445-167">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="83445-167">Example 1 - Namespace</span></span>
<span data-ttu-id="83445-168">Rights: {Listen, Send} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="83445-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="83445-169">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="83445-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="83445-170">Rights: {Listen, Send} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="83445-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="83445-171">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="83445-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="83445-172">Rights: {Listen, Send} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="83445-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="83445-173">Note</span><span class="sxs-lookup"><span data-stu-id="83445-173">NOTES</span></span>

## <span data-ttu-id="83445-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83445-174">RELATED LINKS</span></span>

