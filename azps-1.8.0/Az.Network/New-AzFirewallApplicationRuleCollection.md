---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 2c88e38bba0b4242ff0b268936fbe246214d1921
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678300"
---
# <span data-ttu-id="0ecb5-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0ecb5-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="0ecb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ecb5-102">SYNOPSIS</span></span>
<span data-ttu-id="0ecb5-103">Crea una raccolta di regole dell'applicazione firewall.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="0ecb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ecb5-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ecb5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ecb5-105">DESCRIPTION</span></span>
<span data-ttu-id="0ecb5-106">Il cmdlet **New-AzFirewallApplicationRuleCollection** crea una raccolta di regole dell'applicazione firewall.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="0ecb5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ecb5-107">EXAMPLES</span></span>

### <span data-ttu-id="0ecb5-108">1: creare una raccolta con una sola regola</span><span class="sxs-lookup"><span data-stu-id="0ecb5-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="0ecb5-109">Questo esempio crea una raccolta con una regola.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="0ecb5-110">Tutto il traffico che corrisponde alle condizioni identificate in $rule 1 sarà consentito.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="0ecb5-111">La prima regola è per tutto il traffico HTTPS sulla porta 443 da 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="0ecb5-112">Se è presente un'altra raccolta di regole dell'applicazione con priorità più alta (numero più piccolo) che corrisponde anche al traffico identificato in $rule 1, l'azione della raccolta regole con priorità più alta verrà applicata al suo posto.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="0ecb5-113">2: aggiungere una regola a una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="0ecb5-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="0ecb5-114">Questo esempio crea una nuova raccolta di regole applicazione con una regola e quindi aggiunge una seconda regola alla raccolta di regole usando il Metodo AddRule sull'oggetto della raccolta regole.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="0ecb5-115">Ogni nome di regola in una determinata raccolta di regole deve avere un nome univoco e la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="0ecb5-116">3: ottenere una regola da una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="0ecb5-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="0ecb5-117">Questo esempio crea una nuova raccolta di regole applicazione con una regola e quindi ottiene la regola in base al nome, chiamando il metodo GetRuleByName sull'oggetto della raccolta regole.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="0ecb5-118">Il nome della regola per il metodo GetRuleByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="0ecb5-119">4: rimuovere una regola da una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="0ecb5-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="0ecb5-120">Questo esempio crea una nuova raccolta di regole applicazione con due regole e quindi rimuove la prima regola dalla raccolta di regole chiamando il metodo RemoveRuleByName sull'oggetto della raccolta regole.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="0ecb5-121">Il nome della regola per il metodo RemoveRuleByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="0ecb5-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ecb5-122">PARAMETERS</span></span>

### <span data-ttu-id="0ecb5-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="0ecb5-123">-ActionType</span></span>
<span data-ttu-id="0ecb5-124">Azione della raccolta regole</span><span class="sxs-lookup"><span data-stu-id="0ecb5-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="0ecb5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ecb5-125">-DefaultProfile</span></span>
<span data-ttu-id="0ecb5-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ecb5-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ecb5-127">-Name</span></span>
<span data-ttu-id="0ecb5-128">Specifica il nome della regola dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="0ecb5-129">Il nome deve essere univoco all'interno di una raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="0ecb5-130">-Priorità</span><span class="sxs-lookup"><span data-stu-id="0ecb5-130">-Priority</span></span>
<span data-ttu-id="0ecb5-131">Specifica la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="0ecb5-132">Priority è un numero compreso tra 100 e 65000.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="0ecb5-133">Più piccolo è il numero, maggiore è la priorità.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="0ecb5-134">-Regola</span><span class="sxs-lookup"><span data-stu-id="0ecb5-134">-Rule</span></span>
<span data-ttu-id="0ecb5-135">Specifica l'elenco di regole da raggruppare in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-135">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="0ecb5-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ecb5-136">-Confirm</span></span>
<span data-ttu-id="0ecb5-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ecb5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ecb5-138">-WhatIf</span></span>
<span data-ttu-id="0ecb5-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ecb5-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ecb5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ecb5-141">CommonParameters</span></span>
<span data-ttu-id="0ecb5-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ecb5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ecb5-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ecb5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ecb5-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ecb5-144">INPUTS</span></span>

### <span data-ttu-id="0ecb5-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0ecb5-145">None</span></span>

## <span data-ttu-id="0ecb5-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ecb5-146">OUTPUTS</span></span>

### <span data-ttu-id="0ecb5-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0ecb5-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="0ecb5-148">Note</span><span class="sxs-lookup"><span data-stu-id="0ecb5-148">NOTES</span></span>

## <span data-ttu-id="0ecb5-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ecb5-149">RELATED LINKS</span></span>

[<span data-ttu-id="0ecb5-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="0ecb5-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="0ecb5-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0ecb5-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="0ecb5-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0ecb5-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
