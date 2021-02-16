---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 3e70aa93db8a230308687ce8b03d05d80ab3ab1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206755"
---
# <span data-ttu-id="b6168-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b6168-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="b6168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6168-102">SYNOPSIS</span></span>
<span data-ttu-id="b6168-103">Crea una raccolta di regole dell'applicazione firewall.</span><span class="sxs-lookup"><span data-stu-id="b6168-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="b6168-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6168-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6168-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6168-105">DESCRIPTION</span></span>
<span data-ttu-id="b6168-106">Il cmdlet **New-AzFirewallApplicationRuleCollection** crea una raccolta di regole applicazione firewall.</span><span class="sxs-lookup"><span data-stu-id="b6168-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="b6168-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6168-107">EXAMPLES</span></span>

### <span data-ttu-id="b6168-108">Esempio 1: Creare una raccolta con una regola</span><span class="sxs-lookup"><span data-stu-id="b6168-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="b6168-109">Questo esempio crea una raccolta con una regola.</span><span class="sxs-lookup"><span data-stu-id="b6168-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="b6168-110">Tutto il traffico che soddisfa le condizioni identificate in $rule 1 sarà consentito.</span><span class="sxs-lookup"><span data-stu-id="b6168-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="b6168-111">La prima regola è per tutto il traffico HTTPS sulla porta 443 da 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="b6168-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="b6168-112">Se esiste un'altra raccolta di regole dell'applicazione con priorità più alta (numero minore) che corrisponde anche al traffico identificato in $rule 1, verrà invece applicata l'azione della raccolta di regole con priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="b6168-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="b6168-113">Esempio 2: Aggiungere una regola a una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="b6168-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="b6168-114">Questo esempio crea una nuova raccolta di regole dell'applicazione con una regola e quindi aggiunge una seconda regola alla raccolta di regole usando il metodo AddRule nell'oggetto raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="b6168-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="b6168-115">Ogni nome di regola in una determinata raccolta di regole deve avere un nome univoco senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b6168-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="b6168-116">Esempio 3: Ottenere una regola da una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="b6168-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="b6168-117">Questo esempio crea una nuova raccolta di regole dell'applicazione con una regola e quindi ottiene la regola per nome, richiamando il metodo GetRuleByName sull'oggetto raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="b6168-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="b6168-118">Il nome della regola per il metodo GetRuleByName non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b6168-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="b6168-119">Esempio 4: Rimuovere una regola da una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="b6168-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="b6168-120">Questo esempio crea una nuova raccolta di regole dell'applicazione con due regole e quindi rimuove la prima regola dalla raccolta di regole chiamando il metodo RemoveRuleByName sull'oggetto raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="b6168-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="b6168-121">Il nome della regola per il metodo RemoveRuleByName non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b6168-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="b6168-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6168-122">PARAMETERS</span></span>

### <span data-ttu-id="b6168-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="b6168-123">-ActionType</span></span>
<span data-ttu-id="b6168-124">Azione della raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="b6168-124">The action of the rule collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6168-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6168-125">-DefaultProfile</span></span>
<span data-ttu-id="b6168-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6168-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6168-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b6168-127">-Name</span></span>
<span data-ttu-id="b6168-128">Specifica il nome della regola dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b6168-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="b6168-129">Il nome deve essere univoco all'interno di una raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="b6168-129">The name must be unique inside a rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6168-130">-Priority</span><span class="sxs-lookup"><span data-stu-id="b6168-130">-Priority</span></span>
<span data-ttu-id="b6168-131">Specifica la priorità di questa regola.</span><span class="sxs-lookup"><span data-stu-id="b6168-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="b6168-132">Priorità è un numero compreso tra 100 e 65000.</span><span class="sxs-lookup"><span data-stu-id="b6168-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="b6168-133">Più piccolo è il numero, maggiore sarà la priorità.</span><span class="sxs-lookup"><span data-stu-id="b6168-133">The smaller the number, the bigger the priority.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6168-134">-Rule</span><span class="sxs-lookup"><span data-stu-id="b6168-134">-Rule</span></span>
<span data-ttu-id="b6168-135">Specifica l'elenco di regole da raggruppare in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="b6168-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6168-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6168-136">-Confirm</span></span>
<span data-ttu-id="b6168-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6168-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6168-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6168-138">-WhatIf</span></span>
<span data-ttu-id="b6168-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6168-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6168-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6168-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6168-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6168-141">CommonParameters</span></span>
<span data-ttu-id="b6168-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6168-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6168-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6168-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6168-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6168-144">INPUTS</span></span>

### <span data-ttu-id="b6168-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b6168-145">None</span></span>

## <span data-ttu-id="b6168-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6168-146">OUTPUTS</span></span>

### <span data-ttu-id="b6168-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b6168-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="b6168-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6168-148">NOTES</span></span>

## <span data-ttu-id="b6168-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6168-149">RELATED LINKS</span></span>

[<span data-ttu-id="b6168-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="b6168-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="b6168-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b6168-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b6168-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b6168-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
