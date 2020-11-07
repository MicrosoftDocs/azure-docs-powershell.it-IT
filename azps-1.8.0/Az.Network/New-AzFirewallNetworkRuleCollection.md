---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: af0a81cf915cd853bfc8ca957d706cdb45d96180
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678292"
---
# <span data-ttu-id="46156-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="46156-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="46156-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46156-102">SYNOPSIS</span></span>
<span data-ttu-id="46156-103">Crea una raccolta di regole di rete di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="46156-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="46156-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46156-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46156-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46156-105">DESCRIPTION</span></span>
<span data-ttu-id="46156-106">Il cmdlet **New-AzFirewallNetworkRuleCollection** crea una raccolta di regole di rete firewall.</span><span class="sxs-lookup"><span data-stu-id="46156-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="46156-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46156-107">EXAMPLES</span></span>

### <span data-ttu-id="46156-108">1: creare una raccolta di rete con due regole</span><span class="sxs-lookup"><span data-stu-id="46156-108">1:  Create a network collection with two rules</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="46156-109">Questo esempio crea una raccolta che consentirà a tutto il traffico che corrisponde a una delle due regole.</span><span class="sxs-lookup"><span data-stu-id="46156-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="46156-110">La prima regola è per tutto il traffico UDP.</span><span class="sxs-lookup"><span data-stu-id="46156-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="46156-111">La seconda regola è per il traffico TCP da 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="46156-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="46156-112">Se esiste un'altra raccolta di regole di rete con priorità più alta (numero più piccolo) che corrisponde anche al traffico identificato in $rule 1 o $rule 2, l'azione della raccolta regole con priorità più alta verrà applicata al suo posto.</span><span class="sxs-lookup"><span data-stu-id="46156-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="46156-113">2: aggiungere una regola a una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="46156-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="46156-114">Questo esempio crea una nuova raccolta di regole di rete con una regola e quindi aggiunge una seconda regola alla raccolta di regole usando il Metodo AddRule sull'oggetto della raccolta regole.</span><span class="sxs-lookup"><span data-stu-id="46156-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="46156-115">Ogni nome di regola in una determinata raccolta di regole deve avere un nome univoco e la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="46156-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="46156-116">3: ottenere una regola da una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="46156-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="46156-117">Questo esempio crea una nuova raccolta di regole di rete con una regola e quindi ottiene la regola in base al nome, chiamando il metodo GetRuleByName sull'oggetto della raccolta regole.</span><span class="sxs-lookup"><span data-stu-id="46156-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="46156-118">Il nome della regola per il metodo GetRuleByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="46156-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="46156-119">4: rimuovere una regola da una raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="46156-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="46156-120">Questo esempio crea una nuova raccolta di regole di rete con due regole e quindi rimuove la prima regola dalla raccolta di regole chiamando il metodo RemoveRuleByName sull'oggetto della raccolta regole.</span><span class="sxs-lookup"><span data-stu-id="46156-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="46156-121">Il nome della regola per il metodo RemoveRuleByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="46156-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="46156-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46156-122">PARAMETERS</span></span>

### <span data-ttu-id="46156-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="46156-123">-ActionType</span></span>
<span data-ttu-id="46156-124">Specifica l'azione da intraprendere per le condizioni di corrispondenza del traffico della regola.</span><span class="sxs-lookup"><span data-stu-id="46156-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="46156-125">Le azioni accettate sono "Allow" o "Deny".</span><span class="sxs-lookup"><span data-stu-id="46156-125">Accepted actions are "Allow" or "Deny".</span></span>

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

### <span data-ttu-id="46156-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46156-126">-DefaultProfile</span></span>
<span data-ttu-id="46156-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46156-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46156-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="46156-128">-Name</span></span>
<span data-ttu-id="46156-129">Specifica il nome della raccolta di regole di rete.</span><span class="sxs-lookup"><span data-stu-id="46156-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="46156-130">Il nome deve essere univoco in tutte le raccolte di regole di rete.</span><span class="sxs-lookup"><span data-stu-id="46156-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="46156-131">-Priorità</span><span class="sxs-lookup"><span data-stu-id="46156-131">-Priority</span></span>
<span data-ttu-id="46156-132">Specifica la priorità della raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="46156-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="46156-133">Priority è un numero compreso tra 100 e 65000.</span><span class="sxs-lookup"><span data-stu-id="46156-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="46156-134">Minore è il numero, maggiore è la priorità.</span><span class="sxs-lookup"><span data-stu-id="46156-134">The smaller the number, the higher the priority.</span></span>

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

### <span data-ttu-id="46156-135">-Regola</span><span class="sxs-lookup"><span data-stu-id="46156-135">-Rule</span></span>
<span data-ttu-id="46156-136">Specifica l'elenco di regole da raggruppare in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="46156-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46156-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="46156-137">-Confirm</span></span>
<span data-ttu-id="46156-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46156-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46156-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46156-139">-WhatIf</span></span>
<span data-ttu-id="46156-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46156-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46156-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46156-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46156-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46156-142">CommonParameters</span></span>
<span data-ttu-id="46156-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46156-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46156-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46156-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46156-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46156-145">INPUTS</span></span>

### <span data-ttu-id="46156-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="46156-146">None</span></span>

## <span data-ttu-id="46156-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46156-147">OUTPUTS</span></span>

### <span data-ttu-id="46156-148">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="46156-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="46156-149">Note</span><span class="sxs-lookup"><span data-stu-id="46156-149">NOTES</span></span>

## <span data-ttu-id="46156-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46156-150">RELATED LINKS</span></span>

[<span data-ttu-id="46156-151">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="46156-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="46156-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="46156-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="46156-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="46156-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
