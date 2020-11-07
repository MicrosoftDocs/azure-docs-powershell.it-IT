---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: c0c6a1b3d868bb3189dc040baac9618e60130033
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864246"
---
# <span data-ttu-id="e138c-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="e138c-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="e138c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e138c-102">SYNOPSIS</span></span>
<span data-ttu-id="e138c-103">Crea una regola NAT del firewall.</span><span class="sxs-lookup"><span data-stu-id="e138c-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="e138c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e138c-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e138c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e138c-105">DESCRIPTION</span></span>
<span data-ttu-id="e138c-106">Il cmdlet **New-AzFirewallNatRule** crea una regola NAT per Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="e138c-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="e138c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e138c-107">EXAMPLES</span></span>

### <span data-ttu-id="e138c-108">1: creare una regola per DNAT tutto il traffico TCP da 10.0.0.0/24 con destinazione 10.1.2.3:80 a destinazione 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="e138c-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="e138c-109">Questo esempio crea una regola che consente di DNAT tutto il traffico originario di 10.0.0.0/24 con destinazione 10.1.2.3:80 a 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="e138c-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="e138c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e138c-110">PARAMETERS</span></span>

### <span data-ttu-id="e138c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e138c-111">-DefaultProfile</span></span>
<span data-ttu-id="e138c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e138c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e138c-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e138c-113">-Description</span></span>
<span data-ttu-id="e138c-114">Specifica una descrizione facoltativa della regola.</span><span class="sxs-lookup"><span data-stu-id="e138c-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="e138c-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e138c-115">-DestinationAddress</span></span>
<span data-ttu-id="e138c-116">Indirizzi di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="e138c-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="e138c-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e138c-117">-DestinationPort</span></span>
<span data-ttu-id="e138c-118">Porte di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="e138c-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="e138c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e138c-119">-Name</span></span>
<span data-ttu-id="e138c-120">Specifica il nome della regola NAT.</span><span class="sxs-lookup"><span data-stu-id="e138c-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="e138c-121">Il nome deve essere univoco all'interno di una raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="e138c-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="e138c-122">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="e138c-122">-Protocol</span></span>
<span data-ttu-id="e138c-123">Specifica il tipo di traffico che deve essere filtrato dalla regola.</span><span class="sxs-lookup"><span data-stu-id="e138c-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="e138c-124">I protocolli supportati sono TCP e UDP.</span><span class="sxs-lookup"><span data-stu-id="e138c-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="e138c-125">È consentito un valore speciale "qualsiasi", che significa che corrisponde sia a TCP che a UDP, ma nessun altro protocollo.</span><span class="sxs-lookup"><span data-stu-id="e138c-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e138c-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e138c-126">-SourceAddress</span></span>
<span data-ttu-id="e138c-127">Gli indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="e138c-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="e138c-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="e138c-128">-SourceIpGroup</span></span>
<span data-ttu-id="e138c-129">Ipgroup di origine della regola</span><span class="sxs-lookup"><span data-stu-id="e138c-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="e138c-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="e138c-130">-TranslatedAddress</span></span>
<span data-ttu-id="e138c-131">Specifica il risultato desiderato della traduzione degli indirizzi</span><span class="sxs-lookup"><span data-stu-id="e138c-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="e138c-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="e138c-132">-TranslatedFqdn</span></span>
<span data-ttu-id="e138c-133">Nome di dominio completo tradotto per la regola NAT</span><span class="sxs-lookup"><span data-stu-id="e138c-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="e138c-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="e138c-134">-TranslatedPort</span></span>
<span data-ttu-id="e138c-135">Specifica il risultato desiderato della traduzione della porta</span><span class="sxs-lookup"><span data-stu-id="e138c-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="e138c-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e138c-136">-Confirm</span></span>
<span data-ttu-id="e138c-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e138c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e138c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e138c-138">-WhatIf</span></span>
<span data-ttu-id="e138c-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e138c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e138c-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e138c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e138c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e138c-141">CommonParameters</span></span>
<span data-ttu-id="e138c-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e138c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e138c-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e138c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e138c-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e138c-144">INPUTS</span></span>

### <span data-ttu-id="e138c-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e138c-145">None</span></span>

## <span data-ttu-id="e138c-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e138c-146">OUTPUTS</span></span>

### <span data-ttu-id="e138c-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="e138c-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="e138c-148">Note</span><span class="sxs-lookup"><span data-stu-id="e138c-148">NOTES</span></span>

## <span data-ttu-id="e138c-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e138c-149">RELATED LINKS</span></span>

[<span data-ttu-id="e138c-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e138c-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="e138c-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e138c-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="e138c-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e138c-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
