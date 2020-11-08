---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: 39bba687e355b1742210fb0c37fc8f1a65d957a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192652"
---
# <span data-ttu-id="3e430-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3e430-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="3e430-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e430-102">SYNOPSIS</span></span>
<span data-ttu-id="3e430-103">Crea una nuova regola di autorizzazione per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3e430-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3e430-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e430-104">SYNTAX</span></span>

### <span data-ttu-id="3e430-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e430-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e430-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e430-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e430-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e430-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e430-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e430-108">DESCRIPTION</span></span>
<span data-ttu-id="3e430-109">Il cmdlet **New-AzRelayAuthorizationRule** crea una nuova regola di autorizzazione per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3e430-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3e430-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e430-110">EXAMPLES</span></span>

### <span data-ttu-id="3e430-111">Esempio 1: spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3e430-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="3e430-112">Crea `AuthoRule1` con i diritti di **ascolto** per lo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="3e430-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="3e430-113">Esempio 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3e430-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="3e430-114">Crea una regola `AuthoRule1` di autorizzazione con i diritti di **ascolto** per WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="3e430-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="3e430-115">Esempio 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3e430-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="3e430-116">Crea `AuthoRule1` con i diritti di **ascolto** per la connessione ibrida `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="3e430-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="3e430-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e430-117">PARAMETERS</span></span>

### <span data-ttu-id="3e430-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e430-118">-DefaultProfile</span></span>
<span data-ttu-id="3e430-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e430-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e430-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3e430-120">-HybridConnection</span></span>
<span data-ttu-id="3e430-121">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="3e430-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="3e430-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e430-122">-Name</span></span>
<span data-ttu-id="3e430-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="3e430-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="3e430-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3e430-124">-Namespace</span></span>
<span data-ttu-id="3e430-125">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3e430-125">Namespace Name.</span></span>

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

### <span data-ttu-id="3e430-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e430-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e430-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3e430-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="3e430-128">-Diritti</span><span class="sxs-lookup"><span data-stu-id="3e430-128">-Rights</span></span>
<span data-ttu-id="3e430-129">Diritti, ad esempio "ascolta", "Invia", "Gestisci"</span><span class="sxs-lookup"><span data-stu-id="3e430-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e430-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3e430-130">-WcfRelay</span></span>
<span data-ttu-id="3e430-131">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="3e430-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="3e430-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e430-132">-Confirm</span></span>
<span data-ttu-id="3e430-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e430-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e430-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e430-134">-WhatIf</span></span>
<span data-ttu-id="3e430-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e430-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e430-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e430-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e430-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e430-137">CommonParameters</span></span>
<span data-ttu-id="3e430-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e430-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e430-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e430-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e430-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e430-140">INPUTS</span></span>

### <span data-ttu-id="3e430-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3e430-141">System.String</span></span>

### <span data-ttu-id="3e430-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="3e430-142">System.String[]</span></span>

## <span data-ttu-id="3e430-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e430-143">OUTPUTS</span></span>

### <span data-ttu-id="3e430-144">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3e430-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="3e430-145">Note</span><span class="sxs-lookup"><span data-stu-id="3e430-145">NOTES</span></span>

## <span data-ttu-id="3e430-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e430-146">RELATED LINKS</span></span>
