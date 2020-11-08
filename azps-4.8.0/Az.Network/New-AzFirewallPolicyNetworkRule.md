---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188481"
---
# <span data-ttu-id="a2694-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a2694-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="a2694-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2694-102">SYNOPSIS</span></span>
<span data-ttu-id="a2694-103">Creare una nuova regola di rete dei criteri di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="a2694-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="a2694-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2694-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2694-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2694-105">DESCRIPTION</span></span>
<span data-ttu-id="a2694-106">Il cmdlet **New-AzFirewallPolicyNetworkRule** crea una regola di rete per un criterio di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="a2694-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="a2694-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2694-107">EXAMPLES</span></span>

### <span data-ttu-id="a2694-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2694-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="a2694-109">Questo esempio crea una regola di rete con l'indirizzo di origine, il protocollo, l'indirizzo di destinazione e la porta di destinazione</span><span class="sxs-lookup"><span data-stu-id="a2694-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="a2694-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2694-110">PARAMETERS</span></span>

### <span data-ttu-id="a2694-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2694-111">-DefaultProfile</span></span>
<span data-ttu-id="a2694-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2694-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2694-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2694-113">-Description</span></span>
<span data-ttu-id="a2694-114">Descrizione della regola</span><span class="sxs-lookup"><span data-stu-id="a2694-114">The description of the rule</span></span>

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

### <span data-ttu-id="a2694-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a2694-115">-DestinationAddress</span></span>
<span data-ttu-id="a2694-116">Indirizzi di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="a2694-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="a2694-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="a2694-117">-DestinationFqdn</span></span>
<span data-ttu-id="a2694-118">Nome di dominio completo di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="a2694-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="a2694-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="a2694-119">-DestinationIpGroup</span></span>
<span data-ttu-id="a2694-120">Ipgroups di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="a2694-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="a2694-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a2694-121">-DestinationPort</span></span>
<span data-ttu-id="a2694-122">Porte di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="a2694-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="a2694-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2694-123">-Name</span></span>
<span data-ttu-id="a2694-124">Nome della regola di rete</span><span class="sxs-lookup"><span data-stu-id="a2694-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="a2694-125">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="a2694-125">-Protocol</span></span>
<span data-ttu-id="a2694-126">Protocolli della regola</span><span class="sxs-lookup"><span data-stu-id="a2694-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="a2694-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="a2694-127">-SourceAddress</span></span>
<span data-ttu-id="a2694-128">Gli indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="a2694-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="a2694-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="a2694-129">-SourceIpGroup</span></span>
<span data-ttu-id="a2694-130">Ipgroups di origine della regola</span><span class="sxs-lookup"><span data-stu-id="a2694-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="a2694-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a2694-131">-Confirm</span></span>
<span data-ttu-id="a2694-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2694-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2694-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2694-133">-WhatIf</span></span>
<span data-ttu-id="a2694-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2694-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2694-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2694-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2694-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2694-136">CommonParameters</span></span>
<span data-ttu-id="a2694-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2694-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2694-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2694-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2694-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2694-139">INPUTS</span></span>

### <span data-ttu-id="a2694-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a2694-140">None</span></span>

## <span data-ttu-id="a2694-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2694-141">OUTPUTS</span></span>

### <span data-ttu-id="a2694-142">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a2694-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="a2694-143">Note</span><span class="sxs-lookup"><span data-stu-id="a2694-143">NOTES</span></span>

## <span data-ttu-id="a2694-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2694-144">RELATED LINKS</span></span>