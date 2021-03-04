---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 86e15e54a0091839bdce6a66f891c12e6c0376f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007741"
---
# <span data-ttu-id="635d2-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="635d2-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="635d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="635d2-102">SYNOPSIS</span></span>
<span data-ttu-id="635d2-103">Creare una nuova regola di Rete per i criteri del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="635d2-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="635d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="635d2-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="635d2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="635d2-105">DESCRIPTION</span></span>
<span data-ttu-id="635d2-106">Il cmdlet **New-AzFirewallPolicyNetworkRule** crea una regola di rete per un criterio del firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="635d2-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="635d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="635d2-107">EXAMPLES</span></span>

### <span data-ttu-id="635d2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="635d2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="635d2-109">Questo esempio crea una regola di rete con l'indirizzo di origine, il protocollo, l'indirizzo di destinazione e la porta di destinazione</span><span class="sxs-lookup"><span data-stu-id="635d2-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="635d2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="635d2-110">PARAMETERS</span></span>

### <span data-ttu-id="635d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="635d2-111">-DefaultProfile</span></span>
<span data-ttu-id="635d2-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="635d2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635d2-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="635d2-113">-Description</span></span>
<span data-ttu-id="635d2-114">Descrizione della regola</span><span class="sxs-lookup"><span data-stu-id="635d2-114">The description of the rule</span></span>

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

### <span data-ttu-id="635d2-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="635d2-115">-DestinationAddress</span></span>
<span data-ttu-id="635d2-116">Indirizzi di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="635d2-116">The destination addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635d2-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="635d2-117">-DestinationFqdn</span></span>
<span data-ttu-id="635d2-118">FQDN di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="635d2-118">The destination FQDN of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635d2-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="635d2-119">-DestinationIpGroup</span></span>
<span data-ttu-id="635d2-120">Gli ipgroup di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="635d2-120">The destination ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635d2-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="635d2-121">-DestinationPort</span></span>
<span data-ttu-id="635d2-122">Porte di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="635d2-122">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635d2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="635d2-123">-Name</span></span>
<span data-ttu-id="635d2-124">Nome della regola di rete</span><span class="sxs-lookup"><span data-stu-id="635d2-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="635d2-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="635d2-125">-Protocol</span></span>
<span data-ttu-id="635d2-126">Protocolli della regola</span><span class="sxs-lookup"><span data-stu-id="635d2-126">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635d2-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="635d2-127">-SourceAddress</span></span>
<span data-ttu-id="635d2-128">Indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="635d2-128">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635d2-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="635d2-129">-SourceIpGroup</span></span>
<span data-ttu-id="635d2-130">Ipgroup di origine della regola</span><span class="sxs-lookup"><span data-stu-id="635d2-130">The source ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635d2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="635d2-131">-Confirm</span></span>
<span data-ttu-id="635d2-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="635d2-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635d2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="635d2-133">-WhatIf</span></span>
<span data-ttu-id="635d2-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="635d2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="635d2-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="635d2-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635d2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="635d2-136">CommonParameters</span></span>
<span data-ttu-id="635d2-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="635d2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="635d2-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="635d2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="635d2-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="635d2-139">INPUTS</span></span>

### <span data-ttu-id="635d2-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="635d2-140">None</span></span>

## <span data-ttu-id="635d2-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="635d2-141">OUTPUTS</span></span>

### <span data-ttu-id="635d2-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="635d2-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="635d2-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="635d2-143">NOTES</span></span>

## <span data-ttu-id="635d2-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="635d2-144">RELATED LINKS</span></span>
