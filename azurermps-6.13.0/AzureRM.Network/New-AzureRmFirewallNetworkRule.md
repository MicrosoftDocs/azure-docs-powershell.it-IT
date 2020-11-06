---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
ms.openlocfilehash: 1100e42934c493bf8aea30e7372acc683b46b60b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511688"
---
# <span data-ttu-id="dd05f-101">New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dd05f-101">New-AzureRmFirewallNetworkRule</span></span>

## <span data-ttu-id="dd05f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd05f-102">SYNOPSIS</span></span>
<span data-ttu-id="dd05f-103">Crea una regola di rete firewall.</span><span class="sxs-lookup"><span data-stu-id="dd05f-103">Creates a Firewall Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd05f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd05f-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd05f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd05f-105">DESCRIPTION</span></span>
<span data-ttu-id="dd05f-106">Il cmdlet **New-AzureRmFirewallNetworkRule** crea una regola di rete per Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="dd05f-106">The **New-AzureRmFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="dd05f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd05f-107">EXAMPLES</span></span>

### <span data-ttu-id="dd05f-108">1: creare una regola per tutto il traffico TCP</span><span class="sxs-lookup"><span data-stu-id="dd05f-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="dd05f-109">Questo esempio crea una regola per tutto il traffico TCP.</span><span class="sxs-lookup"><span data-stu-id="dd05f-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="dd05f-110">L'utente impone se il traffico sarà consentito o negato per una regola in base alla raccolta di regole a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="dd05f-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="dd05f-111">2: creare una regola per tutto il traffico TCP da 10.0.0.0 a 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="dd05f-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="dd05f-112">Questo esempio crea una regola per tutto il traffico TCP da 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="dd05f-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="dd05f-113">L'utente impone se il traffico sarà consentito o negato per una regola in base alla raccolta di regole a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="dd05f-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="dd05f-114">3: creare una regola per tutto il traffico TCP e ICMP da qualsiasi origine a 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="dd05f-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="dd05f-115">Questo esempio crea una regola per tutto il traffico TCP da 10.0.0.0 a 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="dd05f-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="dd05f-116">L'utente impone se il traffico sarà consentito o negato per una regola in base alla raccolta di regole a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="dd05f-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="dd05f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd05f-117">PARAMETERS</span></span>

### <span data-ttu-id="dd05f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd05f-118">-DefaultProfile</span></span>
<span data-ttu-id="dd05f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd05f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd05f-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd05f-120">-Description</span></span>
<span data-ttu-id="dd05f-121">Specifica una descrizione facoltativa della regola.</span><span class="sxs-lookup"><span data-stu-id="dd05f-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd05f-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="dd05f-122">-DestinationAddress</span></span>
<span data-ttu-id="dd05f-123">Indirizzi di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="dd05f-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="dd05f-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="dd05f-124">-DestinationPort</span></span>
<span data-ttu-id="dd05f-125">Porte di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="dd05f-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="dd05f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd05f-126">-Name</span></span>
<span data-ttu-id="dd05f-127">Specifica il nome della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="dd05f-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="dd05f-128">Il nome deve essere univoco all'interno di una raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="dd05f-128">The name must be unique inside a rule collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd05f-129">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="dd05f-129">-Protocol</span></span>
<span data-ttu-id="dd05f-130">Specifica il tipo di traffico che deve essere filtrato dalla regola.</span><span class="sxs-lookup"><span data-stu-id="dd05f-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="dd05f-131">I valori possibili sono TCP, UDP, ICMP e any.</span><span class="sxs-lookup"><span data-stu-id="dd05f-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="dd05f-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="dd05f-132">-SourceAddress</span></span>
<span data-ttu-id="dd05f-133">Gli indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="dd05f-133">The source addresses of the rule</span></span>

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

### <span data-ttu-id="dd05f-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd05f-134">-Confirm</span></span>
<span data-ttu-id="dd05f-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd05f-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd05f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd05f-136">-WhatIf</span></span>
<span data-ttu-id="dd05f-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd05f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd05f-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd05f-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd05f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd05f-139">CommonParameters</span></span>
<span data-ttu-id="dd05f-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd05f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd05f-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd05f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd05f-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd05f-142">INPUTS</span></span>

### <span data-ttu-id="dd05f-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dd05f-143">None</span></span>
<span data-ttu-id="dd05f-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="dd05f-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dd05f-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd05f-145">OUTPUTS</span></span>

### <span data-ttu-id="dd05f-146">Microsoft. Azure. Commands. Network. Models. PSFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dd05f-146">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRule</span></span>

## <span data-ttu-id="dd05f-147">Note</span><span class="sxs-lookup"><span data-stu-id="dd05f-147">NOTES</span></span>

## <span data-ttu-id="dd05f-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd05f-148">RELATED LINKS</span></span>

[<span data-ttu-id="dd05f-149">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="dd05f-149">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)

[<span data-ttu-id="dd05f-150">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="dd05f-150">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="dd05f-151">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="dd05f-151">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
