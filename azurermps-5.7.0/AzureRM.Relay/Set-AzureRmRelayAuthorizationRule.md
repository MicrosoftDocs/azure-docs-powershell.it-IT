---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 91f37ad2ed49b4c1bd39306be803776ddce9ecff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520408"
---
# <span data-ttu-id="7d2c2-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7d2c2-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="7d2c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2c2-103">Aggiorna la descrizione della regola di autorizzazione specificata per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="7d2c2-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d2c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d2c2-104">SYNTAX</span></span>

### <span data-ttu-id="7d2c2-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d2c2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d2c2-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d2c2-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d2c2-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d2c2-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>]
 [[-Rights] <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d2c2-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7d2c2-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d2c2-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="7d2c2-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d2c2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d2c2-110">DESCRIPTION</span></span>
<span data-ttu-id="7d2c2-111">Il cmdlet **set-AzureRmRelayAuthorizationRule** aggiorna la descrizione per la regola di autorizzazione specificata delle entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="7d2c2-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="7d2c2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d2c2-112">EXAMPLES</span></span>

### <span data-ttu-id="7d2c2-113">Esempio 1,1-spazio dei nomi con InputObject</span><span class="sxs-lookup"><span data-stu-id="7d2c2-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="7d2c2-114">Aggiunge l' **invio** dei diritti di accesso della regola di autorizzazione `AuthoRule1` nello spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="7d2c2-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="7d2c2-115">Esempio 1,2-spazio dei nomi con Rights Parameter</span><span class="sxs-lookup"><span data-stu-id="7d2c2-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="7d2c2-116">Aggiunge l' **invio** dei diritti di accesso della regola di autorizzazione `AuthoRule1` nello spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="7d2c2-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="7d2c2-117">Esempio 2,1-WcfRelay con InputObject</span><span class="sxs-lookup"><span data-stu-id="7d2c2-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="7d2c2-118">Aggiunge l' **invio** ai diritti di accesso della regola `AuthoRule1` di autorizzazione di WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="7d2c2-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="7d2c2-119">Esempio 2,2-WcfRelay con Rights Parameter</span><span class="sxs-lookup"><span data-stu-id="7d2c2-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="7d2c2-120">Aggiunge l' **invio** ai diritti di accesso della regola `AuthoRule1` di autorizzazione di WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="7d2c2-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="7d2c2-121">Esempio 3,1-HybridConnection con InputObject</span><span class="sxs-lookup"><span data-stu-id="7d2c2-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="7d2c2-122">Aggiunge l' **invio** ai diritti di accesso della regola `AuthoRule1` di autorizzazione di HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="7d2c2-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="7d2c2-123">Esempio 3,2-HybridConnection con Rights Parameter</span><span class="sxs-lookup"><span data-stu-id="7d2c2-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="7d2c2-124">Aggiunge l' **invio** ai diritti di accesso della regola `AuthoRule1` di autorizzazione di HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="7d2c2-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="7d2c2-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d2c2-125">PARAMETERS</span></span>

### <span data-ttu-id="7d2c2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2c2-126">-DefaultProfile</span></span>
<span data-ttu-id="7d2c2-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d2c2-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="7d2c2-128">-HybridConnection</span></span>
<span data-ttu-id="7d2c2-129">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-129">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2c2-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d2c2-130">-InputObject</span></span>
<span data-ttu-id="7d2c2-131">Oggetto AuthorizationRule di inoltro</span><span class="sxs-lookup"><span data-stu-id="7d2c2-131">Relay AuthorizationRule Object</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d2c2-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d2c2-132">-Name</span></span>
<span data-ttu-id="7d2c2-133">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-133">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2c2-134">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7d2c2-134">-Namespace</span></span>
<span data-ttu-id="7d2c2-135">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-135">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2c2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d2c2-136">-ResourceGroupName</span></span>
<span data-ttu-id="7d2c2-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="7d2c2-138">-Diritti</span><span class="sxs-lookup"><span data-stu-id="7d2c2-138">-Rights</span></span>
<span data-ttu-id="7d2c2-139">Diritti, ad esempio @ ("ascolta", "Invia", "Gestisci")</span><span class="sxs-lookup"><span data-stu-id="7d2c2-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d2c2-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7d2c2-140">-WcfRelay</span></span>
<span data-ttu-id="7d2c2-141">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-141">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2c2-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d2c2-142">-Confirm</span></span>
<span data-ttu-id="7d2c2-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d2c2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d2c2-144">-WhatIf</span></span>
<span data-ttu-id="7d2c2-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d2c2-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d2c2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2c2-147">CommonParameters</span></span>
<span data-ttu-id="7d2c2-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2c2-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d2c2-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2c2-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d2c2-150">INPUTS</span></span>

### <span data-ttu-id="7d2c2-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d2c2-151">-ResourceGroupName</span></span>
 <span data-ttu-id="7d2c2-152">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2c2-152">System.String</span></span> 

### <span data-ttu-id="7d2c2-153">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7d2c2-153">-Namespace</span></span>
 <span data-ttu-id="7d2c2-154">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2c2-154">System.String</span></span> 
 

### <span data-ttu-id="7d2c2-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7d2c2-155">-WcfRelay</span></span>
 <span data-ttu-id="7d2c2-156">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2c2-156">System.String</span></span> 

### <span data-ttu-id="7d2c2-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="7d2c2-157">-HybridConnection</span></span>
 <span data-ttu-id="7d2c2-158">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2c2-158">System.String</span></span> 
 

### <span data-ttu-id="7d2c2-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d2c2-159">-Name</span></span>
 <span data-ttu-id="7d2c2-160">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2c2-160">System.String</span></span>

### <span data-ttu-id="7d2c2-161">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d2c2-161">-InputObject</span></span>
 <span data-ttu-id="7d2c2-162">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7d2c2-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="7d2c2-163">-Diritti</span><span class="sxs-lookup"><span data-stu-id="7d2c2-163">-Rights</span></span>
 <span data-ttu-id="7d2c2-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="7d2c2-164">System.String []</span></span>

## <span data-ttu-id="7d2c2-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d2c2-165">OUTPUTS</span></span>

### <span data-ttu-id="7d2c2-166">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7d2c2-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="7d2c2-167">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7d2c2-167">Example 1 - Namespace</span></span>
<span data-ttu-id="7d2c2-168">Rights: {Listen, Send} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="7d2c2-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="7d2c2-169">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7d2c2-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="7d2c2-170">Rights: {Listen, Send} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="7d2c2-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="7d2c2-171">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="7d2c2-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="7d2c2-172">Rights: {Listen, Send} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="7d2c2-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="7d2c2-173">Note</span><span class="sxs-lookup"><span data-stu-id="7d2c2-173">NOTES</span></span>

## <span data-ttu-id="7d2c2-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d2c2-174">RELATED LINKS</span></span>

