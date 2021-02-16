---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: efe8821ee1ec0978c42aa59fc856b4d6e07fa7dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206747"
---
# <span data-ttu-id="4b2aa-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="4b2aa-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="4b2aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="4b2aa-103">Crea una regola NAT del firewall.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="4b2aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b2aa-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b2aa-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4b2aa-105">DESCRIPTION</span></span>
<span data-ttu-id="4b2aa-106">Il cmdlet **New-AzFirewallNatRule** crea una regola NAT per Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="4b2aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b2aa-107">EXAMPLES</span></span>

### <span data-ttu-id="4b2aa-108">Esempio 1: Creare una regola per LA GESTIONE DI TUTTO il traffico TCP da 10.0.0.0/24 con destinazione 10.1.2.3:80 alla destinazione 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="4b2aa-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="4b2aa-109">In questo esempio viene creata una regola in base alla quale PIÙ.0.0.0/24 di destinazione 10.1.2.3:80 verrà creato tutto il traffico proveniente da 10.0.0.0/24 con destinazione 10.1.2.3:80 fino a 10.4.5.6:8080.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="4b2aa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b2aa-110">PARAMETERS</span></span>

### <span data-ttu-id="4b2aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b2aa-111">-DefaultProfile</span></span>
<span data-ttu-id="4b2aa-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b2aa-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b2aa-113">-Description</span></span>
<span data-ttu-id="4b2aa-114">Specifica una descrizione facoltativa della regola.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="4b2aa-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="4b2aa-115">-DestinationAddress</span></span>
<span data-ttu-id="4b2aa-116">Indirizzi di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="4b2aa-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="4b2aa-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="4b2aa-117">-DestinationPort</span></span>
<span data-ttu-id="4b2aa-118">Porte di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="4b2aa-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="4b2aa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4b2aa-119">-Name</span></span>
<span data-ttu-id="4b2aa-120">Specifica il nome di questa regola NAT.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="4b2aa-121">Il nome deve essere univoco all'interno di una raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="4b2aa-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4b2aa-122">-Protocol</span></span>
<span data-ttu-id="4b2aa-123">Specifica il tipo di traffico da filtrare in base alla regola.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="4b2aa-124">I protocolli supportati sono TCP e UDP.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="4b2aa-125">È consentito un valore speciale "Any", che indica che corrisponderà sia a TCP che a UDP, ma non ad altri protocolli.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="4b2aa-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="4b2aa-126">-SourceAddress</span></span>
<span data-ttu-id="4b2aa-127">Indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="4b2aa-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="4b2aa-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="4b2aa-128">-SourceIpGroup</span></span>
<span data-ttu-id="4b2aa-129">Ipgroup di origine della regola</span><span class="sxs-lookup"><span data-stu-id="4b2aa-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="4b2aa-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="4b2aa-130">-TranslatedAddress</span></span>
<span data-ttu-id="4b2aa-131">Specifica il risultato desiderato della conversione dell'indirizzo</span><span class="sxs-lookup"><span data-stu-id="4b2aa-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="4b2aa-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="4b2aa-132">-TranslatedFqdn</span></span>
<span data-ttu-id="4b2aa-133">FQDN tradotti per questa regola NAT</span><span class="sxs-lookup"><span data-stu-id="4b2aa-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="4b2aa-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="4b2aa-134">-TranslatedPort</span></span>
<span data-ttu-id="4b2aa-135">Specifica il risultato desiderato della traduzione delle porte</span><span class="sxs-lookup"><span data-stu-id="4b2aa-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="4b2aa-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b2aa-136">-Confirm</span></span>
<span data-ttu-id="4b2aa-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b2aa-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b2aa-138">-WhatIf</span></span>
<span data-ttu-id="4b2aa-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b2aa-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b2aa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b2aa-141">CommonParameters</span></span>
<span data-ttu-id="4b2aa-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b2aa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b2aa-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b2aa-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b2aa-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="4b2aa-144">INPUTS</span></span>

### <span data-ttu-id="4b2aa-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4b2aa-145">None</span></span>

## <span data-ttu-id="4b2aa-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b2aa-146">OUTPUTS</span></span>

### <span data-ttu-id="4b2aa-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="4b2aa-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="4b2aa-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="4b2aa-148">NOTES</span></span>

## <span data-ttu-id="4b2aa-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b2aa-149">RELATED LINKS</span></span>

[<span data-ttu-id="4b2aa-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4b2aa-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="4b2aa-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4b2aa-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="4b2aa-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4b2aa-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
