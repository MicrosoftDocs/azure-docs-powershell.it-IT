---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: f6a989a206c6fabf8e64cc82fb07741983f144c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032365"
---
# <span data-ttu-id="59dba-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="59dba-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="59dba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59dba-102">SYNOPSIS</span></span>
<span data-ttu-id="59dba-103">Creare una nuova regola NAT per i criteri di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="59dba-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="59dba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59dba-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]>
 -Protocols <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59dba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59dba-105">DESCRIPTION</span></span>
<span data-ttu-id="59dba-106">Il cmdlet **New-AzFirewallPolicyNatRule** crea una regola NAT per un criterio di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="59dba-106">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="59dba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59dba-107">EXAMPLES</span></span>

### <span data-ttu-id="59dba-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59dba-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="59dba-109">Questo esempio crea una regola NAT con l'indirizzo di origine, il protocollo, l'indirizzo di destinazione, la porta di destinazione, l'indirizzo tradotto e la porta tradotta.</span><span class="sxs-lookup"><span data-stu-id="59dba-109">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

## <span data-ttu-id="59dba-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59dba-110">PARAMETERS</span></span>

### <span data-ttu-id="59dba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59dba-111">-DefaultProfile</span></span>
<span data-ttu-id="59dba-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59dba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59dba-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="59dba-113">-Name</span></span>
<span data-ttu-id="59dba-114">Nome della raccolta di regole NAT</span><span class="sxs-lookup"><span data-stu-id="59dba-114">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="59dba-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="59dba-115">-Description</span></span>
<span data-ttu-id="59dba-116">Descrizione della regola</span><span class="sxs-lookup"><span data-stu-id="59dba-116">The description of the rule</span></span>

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

### <span data-ttu-id="59dba-117">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="59dba-117">-DestinationAddress</span></span>
<span data-ttu-id="59dba-118">Gli indirizzi di destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="59dba-118">The destination addresses of the rule.</span></span> <span data-ttu-id="59dba-119">Questo deve essere IP pubblico del firewall.</span><span class="sxs-lookup"><span data-stu-id="59dba-119">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="59dba-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="59dba-120">-DestinationPort</span></span>
<span data-ttu-id="59dba-121">Porte di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="59dba-121">The destination ports of the rule</span></span>

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

### <span data-ttu-id="59dba-122">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="59dba-122">-Protocols</span></span>
<span data-ttu-id="59dba-123">Protocolli della regola</span><span class="sxs-lookup"><span data-stu-id="59dba-123">The protocols of the rule</span></span>

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

### <span data-ttu-id="59dba-124">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="59dba-124">-SourceAddress</span></span>
<span data-ttu-id="59dba-125">Gli indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="59dba-125">The source addresses of the rule</span></span>

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

### <span data-ttu-id="59dba-126">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="59dba-126">-SourceIpGroup</span></span>
<span data-ttu-id="59dba-127">Ipgroups di origine della regola</span><span class="sxs-lookup"><span data-stu-id="59dba-127">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="59dba-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="59dba-128">-TranslatedAddress</span></span>
<span data-ttu-id="59dba-129">Indirizzo tradotto per la regola NAT</span><span class="sxs-lookup"><span data-stu-id="59dba-129">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="59dba-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="59dba-130">-TranslatedPort</span></span>
<span data-ttu-id="59dba-131">Porta tradotta per la regola NAT</span><span class="sxs-lookup"><span data-stu-id="59dba-131">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="59dba-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59dba-132">-Confirm</span></span>
<span data-ttu-id="59dba-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59dba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59dba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59dba-134">-WhatIf</span></span>
<span data-ttu-id="59dba-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59dba-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59dba-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59dba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59dba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59dba-137">CommonParameters</span></span>
<span data-ttu-id="59dba-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59dba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59dba-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59dba-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59dba-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59dba-140">INPUTS</span></span>

### <span data-ttu-id="59dba-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="59dba-141">None</span></span>

## <span data-ttu-id="59dba-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59dba-142">OUTPUTS</span></span>

### <span data-ttu-id="59dba-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="59dba-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="59dba-144">Note</span><span class="sxs-lookup"><span data-stu-id="59dba-144">NOTES</span></span>

## <span data-ttu-id="59dba-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59dba-145">RELATED LINKS</span></span>
