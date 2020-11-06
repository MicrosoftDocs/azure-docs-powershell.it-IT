---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
ms.openlocfilehash: 0bad5133dd57ec0bee88949fbc9536a6389d6112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517463"
---
# <span data-ttu-id="d5564-101">New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="d5564-101">New-AzureRmFirewallNatRule</span></span>

## <span data-ttu-id="d5564-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5564-102">SYNOPSIS</span></span>
<span data-ttu-id="d5564-103">Crea una regola NAT del firewall.</span><span class="sxs-lookup"><span data-stu-id="d5564-103">Creates a Firewall NAT Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5564-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5564-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5564-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5564-105">DESCRIPTION</span></span>
<span data-ttu-id="d5564-106">Il cmdlet **New-AzureRmFirewallNatRule** crea una regola NAT per Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="d5564-106">The **New-AzureRmFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="d5564-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5564-107">EXAMPLES</span></span>

### <span data-ttu-id="d5564-108">1: creare una regola per DNAT tutto il traffico TCP da 10.0.0.0/24 con destinazione 10.1.2.3:80 a destinazione 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="d5564-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzureRmFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="d5564-109">Questo esempio crea una regola che consente di DNAT tutto il traffico originario di 10.0.0.0/24 con destinazione 10.1.2.3:80 a 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="d5564-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="d5564-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5564-110">PARAMETERS</span></span>

### <span data-ttu-id="d5564-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5564-111">-DefaultProfile</span></span>
<span data-ttu-id="d5564-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5564-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5564-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5564-113">-Description</span></span>
<span data-ttu-id="d5564-114">Specifica una descrizione facoltativa della regola.</span><span class="sxs-lookup"><span data-stu-id="d5564-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="d5564-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d5564-115">-DestinationAddress</span></span>
<span data-ttu-id="d5564-116">Gli indirizzi di destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="d5564-116">The destination addresses of the rule.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5564-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d5564-117">-DestinationPort</span></span>
<span data-ttu-id="d5564-118">Porte di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="d5564-118">The destination ports of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5564-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5564-119">-Name</span></span>
<span data-ttu-id="d5564-120">Specifica il nome della regola NAT.</span><span class="sxs-lookup"><span data-stu-id="d5564-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="d5564-121">Il nome deve essere univoco all'interno di una raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="d5564-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="d5564-122">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="d5564-122">-Protocol</span></span>
<span data-ttu-id="d5564-123">Specifica il tipo di traffico che deve essere filtrato dalla regola.</span><span class="sxs-lookup"><span data-stu-id="d5564-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="d5564-124">I protocolli supportati sono TCP e UDP.</span><span class="sxs-lookup"><span data-stu-id="d5564-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="d5564-125">È consentito un valore speciale "qualsiasi", che significa che corrisponde sia a TCP che a UDP, ma nessun altro protocollo.</span><span class="sxs-lookup"><span data-stu-id="d5564-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5564-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="d5564-126">-SourceAddress</span></span>
<span data-ttu-id="d5564-127">Gli indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="d5564-127">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5564-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="d5564-128">-TranslatedAddress</span></span>
<span data-ttu-id="d5564-129">Specifica il risultato desiderato della traduzione degli indirizzi</span><span class="sxs-lookup"><span data-stu-id="d5564-129">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="d5564-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="d5564-130">-TranslatedPort</span></span>
<span data-ttu-id="d5564-131">Specifica il risultato desiderato della traduzione della porta</span><span class="sxs-lookup"><span data-stu-id="d5564-131">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="d5564-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d5564-132">-Confirm</span></span>
<span data-ttu-id="d5564-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5564-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5564-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5564-134">-WhatIf</span></span>
<span data-ttu-id="d5564-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5564-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5564-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5564-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5564-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5564-137">CommonParameters</span></span>
<span data-ttu-id="d5564-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5564-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5564-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5564-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5564-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5564-140">INPUTS</span></span>

### <span data-ttu-id="d5564-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d5564-141">None</span></span>
<span data-ttu-id="d5564-142">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d5564-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d5564-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5564-143">OUTPUTS</span></span>

### <span data-ttu-id="d5564-144">Microsoft. Azure. Commands. Network. Models. PSFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="d5564-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRule</span></span>

## <span data-ttu-id="d5564-145">Note</span><span class="sxs-lookup"><span data-stu-id="d5564-145">NOTES</span></span>

## <span data-ttu-id="d5564-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5564-146">RELATED LINKS</span></span>

[<span data-ttu-id="d5564-147">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d5564-147">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="d5564-148">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d5564-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="d5564-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d5564-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
