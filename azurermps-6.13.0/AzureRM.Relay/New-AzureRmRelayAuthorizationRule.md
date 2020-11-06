---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 825c6060a77df4adf59465e372ee2511fec80803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509132"
---
# <span data-ttu-id="756d2-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="756d2-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="756d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="756d2-102">SYNOPSIS</span></span>
<span data-ttu-id="756d2-103">Crea una nuova regola di autorizzazione per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="756d2-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="756d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="756d2-104">SYNTAX</span></span>

### <span data-ttu-id="756d2-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="756d2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="756d2-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="756d2-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="756d2-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="756d2-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="756d2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="756d2-108">DESCRIPTION</span></span>
<span data-ttu-id="756d2-109">Il cmdlet **New-AzureRmRelayAuthorizationRule** crea una nuova regola di autorizzazione per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="756d2-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="756d2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="756d2-110">EXAMPLES</span></span>

### <span data-ttu-id="756d2-111">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="756d2-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="756d2-112">Crea `AuthoRule1` con i diritti di **ascolto** per lo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="756d2-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="756d2-113">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="756d2-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="756d2-114">Crea una regola `AuthoRule1` di autorizzazione con i diritti di **ascolto** per WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="756d2-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="756d2-115">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="756d2-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="756d2-116">Crea `AuthoRule1` con i diritti di **ascolto** per la connessione ibrida `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="756d2-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="756d2-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="756d2-117">PARAMETERS</span></span>

### <span data-ttu-id="756d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="756d2-118">-DefaultProfile</span></span>
<span data-ttu-id="756d2-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="756d2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="756d2-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="756d2-120">-HybridConnection</span></span>
<span data-ttu-id="756d2-121">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="756d2-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="756d2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="756d2-122">-Name</span></span>
<span data-ttu-id="756d2-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="756d2-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="756d2-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="756d2-124">-Namespace</span></span>
<span data-ttu-id="756d2-125">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="756d2-125">Namespace Name.</span></span>

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

### <span data-ttu-id="756d2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="756d2-126">-ResourceGroupName</span></span>
<span data-ttu-id="756d2-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="756d2-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="756d2-128">-Diritti</span><span class="sxs-lookup"><span data-stu-id="756d2-128">-Rights</span></span>
<span data-ttu-id="756d2-129">Diritti, ad esempio "ascolta", "Invia", "Gestisci"</span><span class="sxs-lookup"><span data-stu-id="756d2-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="756d2-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="756d2-130">-WcfRelay</span></span>
<span data-ttu-id="756d2-131">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="756d2-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="756d2-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="756d2-132">-Confirm</span></span>
<span data-ttu-id="756d2-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="756d2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="756d2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="756d2-134">-WhatIf</span></span>
<span data-ttu-id="756d2-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="756d2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="756d2-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="756d2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="756d2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="756d2-137">CommonParameters</span></span>
<span data-ttu-id="756d2-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="756d2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="756d2-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="756d2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="756d2-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="756d2-140">INPUTS</span></span>

### <span data-ttu-id="756d2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="756d2-141">System.String</span></span>
<span data-ttu-id="756d2-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="756d2-142">System.String[]</span></span>


## <span data-ttu-id="756d2-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="756d2-143">OUTPUTS</span></span>

### <span data-ttu-id="756d2-144">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="756d2-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="756d2-145">Note</span><span class="sxs-lookup"><span data-stu-id="756d2-145">NOTES</span></span>

## <span data-ttu-id="756d2-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="756d2-146">RELATED LINKS</span></span>
