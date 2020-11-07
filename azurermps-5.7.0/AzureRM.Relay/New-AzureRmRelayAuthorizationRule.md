---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: daa2d1539a97b7aff7348fe8e603179c857c73db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687471"
---
# <span data-ttu-id="046d4-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="046d4-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="046d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="046d4-102">SYNOPSIS</span></span>
<span data-ttu-id="046d4-103">Crea una nuova regola di autorizzazione per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="046d4-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="046d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="046d4-104">SYNTAX</span></span>

### <span data-ttu-id="046d4-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="046d4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046d4-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="046d4-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="046d4-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="046d4-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="046d4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="046d4-108">DESCRIPTION</span></span>
<span data-ttu-id="046d4-109">Il cmdlet **New-AzureRmRelayAuthorizationRule** crea una nuova regola di autorizzazione per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="046d4-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="046d4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="046d4-110">EXAMPLES</span></span>

### <span data-ttu-id="046d4-111">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="046d4-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="046d4-112">Crea `AuthoRule1` con i diritti di **ascolto** per lo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="046d4-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="046d4-113">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="046d4-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="046d4-114">Crea una regola `AuthoRule1` di autorizzazione con i diritti di **ascolto** per WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="046d4-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="046d4-115">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="046d4-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="046d4-116">Crea `AuthoRule1` con i diritti di **ascolto** per lo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="046d4-116">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="046d4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="046d4-117">PARAMETERS</span></span>

### <span data-ttu-id="046d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046d4-118">-DefaultProfile</span></span>
<span data-ttu-id="046d4-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="046d4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="046d4-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="046d4-120">-HybridConnection</span></span>
<span data-ttu-id="046d4-121">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="046d4-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="046d4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="046d4-122">-Name</span></span>
<span data-ttu-id="046d4-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="046d4-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="046d4-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="046d4-124">-Namespace</span></span>
<span data-ttu-id="046d4-125">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="046d4-125">Namespace Name.</span></span>

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

### <span data-ttu-id="046d4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046d4-126">-ResourceGroupName</span></span>
<span data-ttu-id="046d4-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="046d4-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="046d4-128">-Diritti</span><span class="sxs-lookup"><span data-stu-id="046d4-128">-Rights</span></span>
<span data-ttu-id="046d4-129">Diritti, ad esempio "ascolta", "Invia", "Gestisci"</span><span class="sxs-lookup"><span data-stu-id="046d4-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046d4-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="046d4-130">-WcfRelay</span></span>
<span data-ttu-id="046d4-131">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="046d4-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="046d4-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="046d4-132">-Confirm</span></span>
<span data-ttu-id="046d4-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="046d4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="046d4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046d4-134">-WhatIf</span></span>
<span data-ttu-id="046d4-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="046d4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="046d4-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="046d4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="046d4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046d4-137">CommonParameters</span></span>
<span data-ttu-id="046d4-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="046d4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046d4-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="046d4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046d4-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="046d4-140">INPUTS</span></span>

### <span data-ttu-id="046d4-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046d4-141">-ResourceGroupName</span></span>
 <span data-ttu-id="046d4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="046d4-142">System.String</span></span> 

### <span data-ttu-id="046d4-143">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="046d4-143">-Namespace</span></span>
 <span data-ttu-id="046d4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="046d4-144">System.String</span></span> 
 

### <span data-ttu-id="046d4-145">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="046d4-145">-WcfRelay</span></span>
 <span data-ttu-id="046d4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="046d4-146">System.String</span></span> 

### <span data-ttu-id="046d4-147">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="046d4-147">-HybridConnection</span></span>
 <span data-ttu-id="046d4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="046d4-148">System.String</span></span> 
 

### <span data-ttu-id="046d4-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="046d4-149">-Name</span></span>
 <span data-ttu-id="046d4-150">System. String</span><span class="sxs-lookup"><span data-stu-id="046d4-150">System.String</span></span>
 

### <span data-ttu-id="046d4-151">-Diritti</span><span class="sxs-lookup"><span data-stu-id="046d4-151">-Rights</span></span>
 <span data-ttu-id="046d4-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="046d4-152">System.String []</span></span>

## <span data-ttu-id="046d4-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="046d4-153">OUTPUTS</span></span>

### <span data-ttu-id="046d4-154">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="046d4-154">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="046d4-155">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="046d4-155">Example 1 - Namespace</span></span>
<span data-ttu-id="046d4-156">Rights: {Listen} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="046d4-156">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="046d4-157">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="046d4-157">Example 2 - WcfRelay</span></span>
<span data-ttu-id="046d4-158">Rights: {Listen} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="046d4-158">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="046d4-159">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="046d4-159">Example 3 - HybridConnection</span></span>
<span data-ttu-id="046d4-160">Rights: {Listen} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="046d4-160">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="046d4-161">Note</span><span class="sxs-lookup"><span data-stu-id="046d4-161">NOTES</span></span>

## <span data-ttu-id="046d4-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="046d4-162">RELATED LINKS</span></span>

