---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020938"
---
# <span data-ttu-id="50456-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="50456-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="50456-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50456-102">SYNOPSIS</span></span>
<span data-ttu-id="50456-103">Creare una nuova raccolta di regole NAT per i criteri di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="50456-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="50456-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50456-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50456-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50456-105">DESCRIPTION</span></span>
<span data-ttu-id="50456-106">Il cmdlet **New-AzFirewallPolicyNatRuleCollection** crea una raccolta di regole NAT per un criterio di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="50456-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="50456-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50456-107">EXAMPLES</span></span>

### <span data-ttu-id="50456-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50456-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="50456-109">Questo esempio crea una raccolta di regole NAT con una regola di rete</span><span class="sxs-lookup"><span data-stu-id="50456-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="50456-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50456-110">PARAMETERS</span></span>

### <span data-ttu-id="50456-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="50456-111">-ActionType</span></span>
<span data-ttu-id="50456-112">Tipo di azione della regola</span><span class="sxs-lookup"><span data-stu-id="50456-112">The type of the rule action</span></span>

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

### <span data-ttu-id="50456-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50456-113">-DefaultProfile</span></span>
<span data-ttu-id="50456-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50456-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50456-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="50456-115">-Name</span></span>
<span data-ttu-id="50456-116">Nome della raccolta regole di rete</span><span class="sxs-lookup"><span data-stu-id="50456-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="50456-117">-Priorità</span><span class="sxs-lookup"><span data-stu-id="50456-117">-Priority</span></span>
<span data-ttu-id="50456-118">Priorità della raccolta regole</span><span class="sxs-lookup"><span data-stu-id="50456-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="50456-119">-Regola</span><span class="sxs-lookup"><span data-stu-id="50456-119">-Rule</span></span>
<span data-ttu-id="50456-120">Elenco delle regole di rete</span><span class="sxs-lookup"><span data-stu-id="50456-120">The list of network rules</span></span>

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

### <span data-ttu-id="50456-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="50456-121">-TranslatedAddress</span></span>
<span data-ttu-id="50456-122">Indirizzo tradotto per la regola NAT</span><span class="sxs-lookup"><span data-stu-id="50456-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="50456-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="50456-123">-TranslatedPort</span></span>
<span data-ttu-id="50456-124">Porta tradotta per la regola NAT</span><span class="sxs-lookup"><span data-stu-id="50456-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="50456-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50456-125">-Confirm</span></span>
<span data-ttu-id="50456-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50456-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50456-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50456-127">-WhatIf</span></span>
<span data-ttu-id="50456-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50456-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50456-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50456-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50456-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50456-130">CommonParameters</span></span>
<span data-ttu-id="50456-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50456-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50456-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50456-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50456-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50456-133">INPUTS</span></span>

### <span data-ttu-id="50456-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="50456-134">None</span></span>

## <span data-ttu-id="50456-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50456-135">OUTPUTS</span></span>

### <span data-ttu-id="50456-136">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="50456-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="50456-137">Note</span><span class="sxs-lookup"><span data-stu-id="50456-137">NOTES</span></span>

## <span data-ttu-id="50456-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50456-138">RELATED LINKS</span></span>
