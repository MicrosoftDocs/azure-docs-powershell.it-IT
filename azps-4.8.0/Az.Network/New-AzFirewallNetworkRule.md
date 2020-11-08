---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: c3cf6ce07ab746806181af917f656d27c6ffbbaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192804"
---
# <span data-ttu-id="b2d32-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b2d32-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="b2d32-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2d32-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d32-103">Crea una regola di rete firewall.</span><span class="sxs-lookup"><span data-stu-id="b2d32-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="b2d32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2d32-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2d32-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2d32-105">DESCRIPTION</span></span>
<span data-ttu-id="b2d32-106">Il cmdlet **New-AzFirewallNetworkRule** crea una regola di rete per Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="b2d32-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="b2d32-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2d32-107">EXAMPLES</span></span>

### <span data-ttu-id="b2d32-108">Esempio 1: creare una regola per tutto il traffico TCP</span><span class="sxs-lookup"><span data-stu-id="b2d32-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="b2d32-109">Questo esempio crea una regola per tutto il traffico TCP.</span><span class="sxs-lookup"><span data-stu-id="b2d32-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="b2d32-110">L'utente impone se il traffico sarà consentito o negato per una regola in base alla raccolta di regole a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="b2d32-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="b2d32-111">Esempio 2: creare una regola per tutto il traffico TCP da 10.0.0.0 a 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="b2d32-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="b2d32-112">Questo esempio crea una regola per tutto il traffico TCP da 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="b2d32-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="b2d32-113">L'utente impone se il traffico sarà consentito o negato per una regola in base alla raccolta di regole a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="b2d32-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="b2d32-114">Esempio 3: creare una regola per tutto il traffico TCP e ICMP da qualsiasi origine a 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="b2d32-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="b2d32-115">Questo esempio crea una regola per tutto il traffico TCP da qualsiasi origine a 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="b2d32-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="b2d32-116">L'utente impone se il traffico sarà consentito o negato per una regola in base alla raccolta di regole a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="b2d32-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="b2d32-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2d32-117">PARAMETERS</span></span>

### <span data-ttu-id="b2d32-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d32-118">-DefaultProfile</span></span>
<span data-ttu-id="b2d32-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2d32-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2d32-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2d32-120">-Description</span></span>
<span data-ttu-id="b2d32-121">Specifica una descrizione facoltativa della regola.</span><span class="sxs-lookup"><span data-stu-id="b2d32-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="b2d32-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b2d32-122">-DestinationAddress</span></span>
<span data-ttu-id="b2d32-123">Indirizzi di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="b2d32-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="b2d32-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="b2d32-124">-DestinationFqdn</span></span>
<span data-ttu-id="b2d32-125">Nome di dominio completo di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="b2d32-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="b2d32-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="b2d32-126">-DestinationIpGroup</span></span>
<span data-ttu-id="b2d32-127">Ipgroup di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="b2d32-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="b2d32-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b2d32-128">-DestinationPort</span></span>
<span data-ttu-id="b2d32-129">Porte di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="b2d32-129">The destination ports of the rule</span></span>

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

### <span data-ttu-id="b2d32-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2d32-130">-Name</span></span>
<span data-ttu-id="b2d32-131">Specifica il nome della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="b2d32-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="b2d32-132">Il nome deve essere univoco all'interno di una raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="b2d32-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="b2d32-133">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="b2d32-133">-Protocol</span></span>
<span data-ttu-id="b2d32-134">Specifica il tipo di traffico che deve essere filtrato dalla regola.</span><span class="sxs-lookup"><span data-stu-id="b2d32-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="b2d32-135">I valori possibili sono TCP, UDP, ICMP e any.</span><span class="sxs-lookup"><span data-stu-id="b2d32-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="b2d32-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="b2d32-136">-SourceAddress</span></span>
<span data-ttu-id="b2d32-137">Gli indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="b2d32-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="b2d32-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="b2d32-138">-SourceIpGroup</span></span>
<span data-ttu-id="b2d32-139">Ipgroup di origine della regola</span><span class="sxs-lookup"><span data-stu-id="b2d32-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="b2d32-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2d32-140">-Confirm</span></span>
<span data-ttu-id="b2d32-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2d32-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2d32-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2d32-142">-WhatIf</span></span>
<span data-ttu-id="b2d32-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2d32-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2d32-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2d32-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2d32-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d32-145">CommonParameters</span></span>
<span data-ttu-id="b2d32-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2d32-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d32-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2d32-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d32-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2d32-148">INPUTS</span></span>

### <span data-ttu-id="b2d32-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b2d32-149">None</span></span>

## <span data-ttu-id="b2d32-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2d32-150">OUTPUTS</span></span>

### <span data-ttu-id="b2d32-151">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b2d32-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="b2d32-152">Note</span><span class="sxs-lookup"><span data-stu-id="b2d32-152">NOTES</span></span>

## <span data-ttu-id="b2d32-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2d32-153">RELATED LINKS</span></span>

[<span data-ttu-id="b2d32-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b2d32-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="b2d32-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b2d32-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b2d32-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b2d32-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)