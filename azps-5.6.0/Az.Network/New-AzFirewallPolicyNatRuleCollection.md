---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 4dd93dec5aad6fe0e77e92e44884c687d5841e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960413"
---
# <span data-ttu-id="089e5-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="089e5-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="089e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="089e5-102">SYNOPSIS</span></span>
<span data-ttu-id="089e5-103">Creare una nuova raccolta di regole NAT per i criteri del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="089e5-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="089e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="089e5-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="089e5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="089e5-105">DESCRIPTION</span></span>
<span data-ttu-id="089e5-106">Il cmdlet **New-AzFirewallPolicyNatRuleCollection crea** una raccolta di regole Nat per un criterio firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="089e5-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="089e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="089e5-107">EXAMPLES</span></span>

### <span data-ttu-id="089e5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="089e5-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="089e5-109">Questo esempio crea una raccolta di regole NAT con una regola di rete</span><span class="sxs-lookup"><span data-stu-id="089e5-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="089e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="089e5-110">PARAMETERS</span></span>

### <span data-ttu-id="089e5-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="089e5-111">-ActionType</span></span>
<span data-ttu-id="089e5-112">Tipo di azione della regola</span><span class="sxs-lookup"><span data-stu-id="089e5-112">The type of the rule action</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Dnat

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089e5-113">-DefaultProfile</span></span>
<span data-ttu-id="089e5-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="089e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="089e5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="089e5-115">-Name</span></span>
<span data-ttu-id="089e5-116">Nome della raccolta di regole di rete</span><span class="sxs-lookup"><span data-stu-id="089e5-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="089e5-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="089e5-117">-Priority</span></span>
<span data-ttu-id="089e5-118">Priorità della raccolta di regole</span><span class="sxs-lookup"><span data-stu-id="089e5-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089e5-119">-Rule</span><span class="sxs-lookup"><span data-stu-id="089e5-119">-Rule</span></span>
<span data-ttu-id="089e5-120">Elenco delle regole di rete</span><span class="sxs-lookup"><span data-stu-id="089e5-120">The list of network rules</span></span>

```yaml
Type: PSAzureFirewallPolicyNetworkRule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089e5-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="089e5-121">-TranslatedAddress</span></span>
<span data-ttu-id="089e5-122">Indirizzo tradotto per questa regola NAT</span><span class="sxs-lookup"><span data-stu-id="089e5-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="089e5-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="089e5-123">-TranslatedPort</span></span>
<span data-ttu-id="089e5-124">La porta tradotta per questa regola NAT</span><span class="sxs-lookup"><span data-stu-id="089e5-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="089e5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="089e5-125">-Confirm</span></span>
<span data-ttu-id="089e5-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="089e5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="089e5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="089e5-127">-WhatIf</span></span>
<span data-ttu-id="089e5-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="089e5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="089e5-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="089e5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="089e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089e5-130">CommonParameters</span></span>
<span data-ttu-id="089e5-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="089e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089e5-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="089e5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089e5-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="089e5-133">INPUTS</span></span>

### <span data-ttu-id="089e5-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="089e5-134">None</span></span>

## <span data-ttu-id="089e5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="089e5-135">OUTPUTS</span></span>

### <span data-ttu-id="089e5-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="089e5-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="089e5-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="089e5-137">NOTES</span></span>

## <span data-ttu-id="089e5-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="089e5-138">RELATED LINKS</span></span>
