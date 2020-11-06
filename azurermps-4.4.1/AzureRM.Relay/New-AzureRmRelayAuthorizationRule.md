---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 9e4eecad543346efa60dfb0b9a20e31c47a59036
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513028"
---
# <span data-ttu-id="89303-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="89303-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="89303-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89303-102">SYNOPSIS</span></span>
<span data-ttu-id="89303-103">Crea una nuova regola di autorizzazione per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="89303-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89303-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89303-104">SYNTAX</span></span>

### <span data-ttu-id="89303-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89303-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89303-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="89303-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89303-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="89303-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89303-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89303-108">DESCRIPTION</span></span>
<span data-ttu-id="89303-109">Il cmdlet **New-AzureRmRelayAuthorizationRule** crea una nuova regola di autorizzazione per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="89303-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="89303-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89303-110">EXAMPLES</span></span>

### <span data-ttu-id="89303-111">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89303-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="89303-112">Crea `AuthoRule1` con i diritti di **ascolto** per lo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="89303-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="89303-113">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="89303-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="89303-114">Crea una regola `AuthoRule1` di autorizzazione con i diritti di **ascolto** per WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="89303-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="89303-115">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="89303-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="89303-116">Crea `AuthoRule1` con i diritti di **ascolto** per lo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="89303-116">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="89303-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89303-117">PARAMETERS</span></span>

### <span data-ttu-id="89303-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="89303-118">-Confirm</span></span>
<span data-ttu-id="89303-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89303-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89303-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="89303-120">-HybridConnection</span></span>
<span data-ttu-id="89303-121">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="89303-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="89303-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="89303-122">-Name</span></span>
<span data-ttu-id="89303-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="89303-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="89303-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89303-124">-Namespace</span></span>
<span data-ttu-id="89303-125">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="89303-125">Namespace Name.</span></span>

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

### <span data-ttu-id="89303-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89303-126">-ResourceGroupName</span></span>
<span data-ttu-id="89303-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89303-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="89303-128">-Diritti</span><span class="sxs-lookup"><span data-stu-id="89303-128">-Rights</span></span>
<span data-ttu-id="89303-129">Diritti, ad esempio "ascolta", "Invia", "Gestisci"</span><span class="sxs-lookup"><span data-stu-id="89303-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89303-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="89303-130">-WcfRelay</span></span>
<span data-ttu-id="89303-131">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="89303-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="89303-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89303-132">-WhatIf</span></span>
<span data-ttu-id="89303-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89303-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89303-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89303-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89303-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89303-135">-DefaultProfile</span></span>
<span data-ttu-id="89303-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89303-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89303-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89303-137">CommonParameters</span></span>
<span data-ttu-id="89303-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89303-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89303-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89303-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89303-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89303-140">INPUTS</span></span>

### <span data-ttu-id="89303-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89303-141">-ResourceGroupName</span></span>
 <span data-ttu-id="89303-142">System. String</span><span class="sxs-lookup"><span data-stu-id="89303-142">System.String</span></span> 

### <span data-ttu-id="89303-143">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89303-143">-Namespace</span></span>
 <span data-ttu-id="89303-144">System. String</span><span class="sxs-lookup"><span data-stu-id="89303-144">System.String</span></span> 
 

### <span data-ttu-id="89303-145">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="89303-145">-WcfRelay</span></span>
 <span data-ttu-id="89303-146">System. String</span><span class="sxs-lookup"><span data-stu-id="89303-146">System.String</span></span> 

### <span data-ttu-id="89303-147">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="89303-147">-HybridConnection</span></span>
 <span data-ttu-id="89303-148">System. String</span><span class="sxs-lookup"><span data-stu-id="89303-148">System.String</span></span> 
 

### <span data-ttu-id="89303-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="89303-149">-Name</span></span>
 <span data-ttu-id="89303-150">System. String</span><span class="sxs-lookup"><span data-stu-id="89303-150">System.String</span></span>
 

### <span data-ttu-id="89303-151">-Diritti</span><span class="sxs-lookup"><span data-stu-id="89303-151">-Rights</span></span>
 <span data-ttu-id="89303-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="89303-152">System.String []</span></span>

## <span data-ttu-id="89303-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89303-153">OUTPUTS</span></span>

### <span data-ttu-id="89303-154">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="89303-154">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="89303-155">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89303-155">Example 1 - Namespace</span></span>
<span data-ttu-id="89303-156">Rights: {Listen} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="89303-156">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="89303-157">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="89303-157">Example 2 - WcfRelay</span></span>
<span data-ttu-id="89303-158">Rights: {Listen} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="89303-158">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="89303-159">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="89303-159">Example 3 - HybridConnection</span></span>
<span data-ttu-id="89303-160">Rights: {Listen} nome: AuthoRule1 tipo: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="89303-160">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="89303-161">Note</span><span class="sxs-lookup"><span data-stu-id="89303-161">NOTES</span></span>

## <span data-ttu-id="89303-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89303-162">RELATED LINKS</span></span>

