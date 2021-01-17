---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: c3cf6ce07ab746806181af917f656d27c6ffbbaa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475928"
---
# <span data-ttu-id="b9e4b-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b9e4b-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="b9e4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e4b-103">Crea una regola di rete firewall.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="b9e4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9e4b-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e4b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9e4b-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e4b-106">Il cmdlet **New-AzFirewallNetworkRule** crea una regola di rete per Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="b9e4b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9e4b-107">EXAMPLES</span></span>

### <span data-ttu-id="b9e4b-108">Esempio 1: creare una regola per tutto il traffico TCP</span><span class="sxs-lookup"><span data-stu-id="b9e4b-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="b9e4b-109">Questo esempio crea una regola per tutto il traffico TCP.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="b9e4b-110">L'utente impone se il traffico sarà consentito o negato per una regola in base alla raccolta di regole a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="b9e4b-111">Esempio 2: creare una regola per tutto il traffico TCP da 10.0.0.0 a 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="b9e4b-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="b9e4b-112">Questo esempio crea una regola per tutto il traffico TCP da 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="b9e4b-113">L'utente impone se il traffico sarà consentito o negato per una regola in base alla raccolta di regole a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="b9e4b-114">Esempio 3: creare una regola per tutto il traffico TCP e ICMP da qualsiasi origine a 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="b9e4b-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="b9e4b-115">Questo esempio crea una regola per tutto il traffico TCP da qualsiasi origine a 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="b9e4b-116">L'utente impone se il traffico sarà consentito o negato per una regola in base alla raccolta di regole a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="b9e4b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9e4b-117">PARAMETERS</span></span>

### <span data-ttu-id="b9e4b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e4b-118">-DefaultProfile</span></span>
<span data-ttu-id="b9e4b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9e4b-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9e4b-120">-Description</span></span>
<span data-ttu-id="b9e4b-121">Specifica una descrizione facoltativa della regola.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e4b-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b9e4b-122">-DestinationAddress</span></span>
<span data-ttu-id="b9e4b-123">Indirizzi di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="b9e4b-123">The destination addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e4b-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="b9e4b-124">-DestinationFqdn</span></span>
<span data-ttu-id="b9e4b-125">Nome di dominio completo di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="b9e4b-125">The destination FQDN of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e4b-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="b9e4b-126">-DestinationIpGroup</span></span>
<span data-ttu-id="b9e4b-127">Ipgroup di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="b9e4b-127">The destination ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e4b-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b9e4b-128">-DestinationPort</span></span>
<span data-ttu-id="b9e4b-129">Porte di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="b9e4b-129">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e4b-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9e4b-130">-Name</span></span>
<span data-ttu-id="b9e4b-131">Specifica il nome della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="b9e4b-132">Il nome deve essere univoco all'interno di una raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="b9e4b-133">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="b9e4b-133">-Protocol</span></span>
<span data-ttu-id="b9e4b-134">Specifica il tipo di traffico che deve essere filtrato dalla regola.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="b9e4b-135">I valori possibili sono TCP, UDP, ICMP e any.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e4b-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="b9e4b-136">-SourceAddress</span></span>
<span data-ttu-id="b9e4b-137">Gli indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="b9e4b-137">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e4b-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="b9e4b-138">-SourceIpGroup</span></span>
<span data-ttu-id="b9e4b-139">Ipgroup di origine della regola</span><span class="sxs-lookup"><span data-stu-id="b9e4b-139">The source ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e4b-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9e4b-140">-Confirm</span></span>
<span data-ttu-id="b9e4b-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e4b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e4b-142">-WhatIf</span></span>
<span data-ttu-id="b9e4b-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e4b-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e4b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e4b-145">CommonParameters</span></span>
<span data-ttu-id="b9e4b-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e4b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e4b-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e4b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e4b-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9e4b-148">INPUTS</span></span>

### <span data-ttu-id="b9e4b-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b9e4b-149">None</span></span>

## <span data-ttu-id="b9e4b-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9e4b-150">OUTPUTS</span></span>

### <span data-ttu-id="b9e4b-151">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b9e4b-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="b9e4b-152">Note</span><span class="sxs-lookup"><span data-stu-id="b9e4b-152">NOTES</span></span>

## <span data-ttu-id="b9e4b-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9e4b-153">RELATED LINKS</span></span>

[<span data-ttu-id="b9e4b-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b9e4b-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="b9e4b-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b9e4b-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b9e4b-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b9e4b-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
