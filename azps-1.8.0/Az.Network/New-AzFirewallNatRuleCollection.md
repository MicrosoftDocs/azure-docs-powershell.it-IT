---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 171431e02627177bbb62f64c9a170c02234e0c61
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678296"
---
# <span data-ttu-id="c86f1-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c86f1-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="c86f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c86f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c86f1-103">Crea una raccolta di regole NAT del firewall.</span><span class="sxs-lookup"><span data-stu-id="c86f1-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="c86f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c86f1-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c86f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c86f1-105">DESCRIPTION</span></span>
<span data-ttu-id="c86f1-106">Il cmdlet **New-AzFirewallNatRuleCollection** crea una raccolta di regole NAT del firewall.</span><span class="sxs-lookup"><span data-stu-id="c86f1-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="c86f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c86f1-107">EXAMPLES</span></span>

### <span data-ttu-id="c86f1-108">1: creare una raccolta con una sola regola</span><span class="sxs-lookup"><span data-stu-id="c86f1-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="c86f1-109">Questo esempio crea una raccolta con una regola.</span><span class="sxs-lookup"><span data-stu-id="c86f1-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="c86f1-110">Tutto il traffico che corrisponde alle condizioni identificate in $rule 1 sarà DNAT'ed per l'indirizzo e la porta tradotti.</span><span class="sxs-lookup"><span data-stu-id="c86f1-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="c86f1-111">2: aggiungere una regola a una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="c86f1-111">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="c86f1-112">Questo esempio crea una nuova raccolta di regole NAT con una regola e quindi aggiunge una seconda regola alla raccolta di regole usando il Metodo AddRule sull'oggetto della raccolta regole.</span><span class="sxs-lookup"><span data-stu-id="c86f1-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="c86f1-113">Ogni nome di regola in una determinata raccolta di regole deve avere un nome univoco e la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c86f1-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="c86f1-114">3: ottenere una regola da una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="c86f1-114">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="c86f1-115">Questo esempio crea una nuova raccolta di regole NAT con una regola e quindi ottiene la regola in base al nome, chiamando il metodo GetRuleByName sull'oggetto della raccolta regole.</span><span class="sxs-lookup"><span data-stu-id="c86f1-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="c86f1-116">Il nome della regola per il metodo GetRuleByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c86f1-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="c86f1-117">4: rimuovere una regola da una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="c86f1-117">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="c86f1-118">Questo esempio crea una nuova raccolta di regole NAT con due regole e quindi rimuove la prima regola dalla raccolta di regole chiamando il metodo RemoveRuleByName sull'oggetto della raccolta regole.</span><span class="sxs-lookup"><span data-stu-id="c86f1-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="c86f1-119">Il nome della regola per il metodo RemoveRuleByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c86f1-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="c86f1-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c86f1-120">PARAMETERS</span></span>

### <span data-ttu-id="c86f1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c86f1-121">-DefaultProfile</span></span>
<span data-ttu-id="c86f1-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c86f1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c86f1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c86f1-123">-Name</span></span>
<span data-ttu-id="c86f1-124">Specifica il nome della regola NAT.</span><span class="sxs-lookup"><span data-stu-id="c86f1-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="c86f1-125">Il nome deve essere univoco all'interno di una raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="c86f1-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="c86f1-126">-Priorità</span><span class="sxs-lookup"><span data-stu-id="c86f1-126">-Priority</span></span>
<span data-ttu-id="c86f1-127">Specifica la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="c86f1-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="c86f1-128">Priority è un numero compreso tra 100 e 65000.</span><span class="sxs-lookup"><span data-stu-id="c86f1-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="c86f1-129">Più piccolo è il numero, maggiore è la priorità.</span><span class="sxs-lookup"><span data-stu-id="c86f1-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="c86f1-130">-Regola</span><span class="sxs-lookup"><span data-stu-id="c86f1-130">-Rule</span></span>
<span data-ttu-id="c86f1-131">Specifica l'elenco di regole da raggruppare in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="c86f1-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86f1-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c86f1-132">-Confirm</span></span>
<span data-ttu-id="c86f1-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c86f1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c86f1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c86f1-134">-WhatIf</span></span>
<span data-ttu-id="c86f1-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c86f1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c86f1-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c86f1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c86f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c86f1-137">CommonParameters</span></span>
<span data-ttu-id="c86f1-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c86f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c86f1-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c86f1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c86f1-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c86f1-140">INPUTS</span></span>

### <span data-ttu-id="c86f1-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c86f1-141">None</span></span>

## <span data-ttu-id="c86f1-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c86f1-142">OUTPUTS</span></span>

### <span data-ttu-id="c86f1-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c86f1-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="c86f1-144">Note</span><span class="sxs-lookup"><span data-stu-id="c86f1-144">NOTES</span></span>

## <span data-ttu-id="c86f1-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c86f1-145">RELATED LINKS</span></span>

[<span data-ttu-id="c86f1-146">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="c86f1-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="c86f1-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c86f1-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="c86f1-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c86f1-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)